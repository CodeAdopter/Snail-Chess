# Snail Chess 2.0 (draft)

Not released yet. Changes are uncommitted.

Human Mode: with `UCI_LimitStrength` on, Snail Chess plays like a Lichess player of the chosen
rating. It no longer searches with added noise. A neural net (Ganglia), trained on Lichess games,
chooses the move a person of that rating would play, how long they would think, and when they
would resign. Full strength is unchanged.

## Human Mode

How often the move matches the one a person actually played.

The net is v3 small: 9 layers x 192 with smolgen, 8.7M weights, trained by Ganglia on 400M
positions of bullet, blitz, rapid and classical games in five and a half hours on one RTX 5080.
The engine carries it with 8-bit weights, 9.5 MB (`src/v3-small-9x192.gnet`), which plays the same moves:

| All held-out positions | Bullet | Blitz | Rapid | Classical |
|---|---|---|---|---|
| August 25–31, the last week of the training month (2.69M) | 54.7% | 56.3% | 55.8% | 55.1% |
| October 25–31, a month it never saw (2.77M) | 54.6% | 56.2% | 55.4% | 54.8% |

Top-3 is about 83% on blitz and rapid and 82% on bullet. The first net of this size, trained
without bullet games, had 47.0%, 56.0%, 55.6% and 54.8% on the August positions.

The engines over UCI, on the same 8,000 August positions, each sent as the real game, measured
with that first net. No clock is given, so Human Mode assumes rapid:

| | Bullet | Blitz | Rapid |
|---|---|---|---|
| Snail Chess 2.0 Human Mode, as it plays (sampled) | 42.0% | 41.9% | 42.6% |
| Snail Chess 2.0 Human Mode, `HumanTemperature 0` | 51.3% | 54.9% | 54.5% |
| Snail Chess 1.19, full search | 35.5% | 39.8% | 38.1% |
| Snail Chess 1.19, `UCI_LimitStrength` | 32.5% | 34.5% | 34.1% |

The value head is calibrated. At step 40,000 its average expected score was about 0.05 too low,
and by step 90,000 that had gone.

Nine self-play games with real clocks, three each at 1200 3+0,
1600 5+0 and 2000 10+0:

- Seven ended by resignation and two by checkmate.
- The openings were typical of each rating, for example a Nimzo-Indian at 2000.
- Openings took 1–2 s a move, middlegame thinks up to about a minute, recaptures about a second.
- The games ended with realistic time left on the clocks.

- **Ratings.** `UCI_Elo` is a Lichess rating, from 400 to 2800, in the time control of the game.
  The time control comes from the clock in `go`; without a clock it is rapid.
- **Think times.** For each move the net draws a think time from its think-time head, then the
  move given that time. Recaptures and obvious moves come quickly, and hard positions take longer.
  The time is capped at an eighth of the clock.
- **Resignation.** A model fitted to how 400,000 Lichess games ended gives the chance that a player
  resigns at each move.
  - The chance comes from the net's expected score, material, what the last two plies cost, the
    rating, the time control, the clock and the move number.
  - A 1500 who has just lost the queen for nothing resigns about 40% of the time on that move, and
    otherwise plays on for a while.
  - In a lost endgame the chance is about 1% a move.
- **Style.** `Style` (Aggressive, Passive) tilts the net's move probabilities toward or away from
  checks, approaching the king and even trades.

## UCI

The options GUIs show, with the Human ones grouped and named for what they do:

| Option | Default | |
|---|---|---|
| `UCI_LimitStrength` | false | play like a human: the standard UCI strength switch |
| `UCI_Elo` | 1500 | the Lichess rating to play like, 400–2800: the standard UCI strength value |
| `Human Resign` | true | whether the engine may resign |
| `Human Timing` | false | wait the drawn think time before answering. For GUIs that don't read it from the info line. |
| `Human Pace` | 100 | percent of the human think time (a slow or fast player) |
| `Human Premove` | true | let it premove, mostly recaptures and moves in a time scramble: a premove's think time is 0 and the info line ends with `premove`, for the GUI to play it with no wait and take no time off the engine's clock |
| `Human Temperature` | 100 | 100 samples like a person, 0 always plays the net's most likely move |
| `Human Net` | `<embedded>` | a net file to use instead of the built-in one: the engine's own format, a Ganglia `.gnet`, or either quantized. `<none>` plays without a move net: the engine's search chooses the move, weakened to the rating |
| `Human Time Net` | `<none>` | a think-time net (a Ganglia `.tnet`, or one quantized) to draw think times from, instead of the move net's own think-time head. Without a move net it times the search's moves |
| `UCI_Opponent` | | standard UCI (`none 1650 human name`): the opponent's rating; without it the opponent counts as the same rating |

Human Mode has one switch, the standard pair, which GUIs set from their own strength setting.
`Human Playstyle` and `Human Elo`, a second spelling of the pair, are no longer listed; the engine
still understands them. The Human options also accept their one-word spellings (`HumanResign`).
In Human Mode, `go infinite` reports the move
and waits for `stop` before `bestmove`.

Each Human Mode move reports, for example at 1500 from the start of a 5+0 game:

```
info depth 1 seldepth 1 score cp 42 wdl 543 33 424 nodes 1 time 45 pv d2d4
info string human move d2d4 prob 0.241 think 1.00 expected 0.560 resign 0.0004 check 1.00 penalty 1.3 kept 5 of 5
bestmove d2d4
```

When the player gives up, `info string human resign` comes before the `bestmove`. `prob` is the
chosen move's probability. The README's UCI guide walks a GUI through a whole game.

- `score` and `wdl` are the net's expected result for a player of this rating, not an engine
  evaluation.
- `think` is the human think time in seconds. A GUI shows the move after that long.
- `resign` is that move's resignation chance.
- `info string human resign` means the player resigns instead of playing `bestmove`. The
  `bestmove` is still sent because UCI requires an answer. GUIs that don't know the line just see
  a move.

## Engine

| Change | |
|---|---|
| Human Mode (`src/ganglia.snail`, `src/human.snail`, `src/resign.snail`) | 35 MB with the embedded net. About 40 ms a move: two passes of the net. |
| Snail 0.1: `Bitboard` and `Square` come from `src/bitboard.snail` and `src/square.snail` | `bench` is unchanged: 3,869,083 nodes |

## Testing

- **The net in Snail against PyTorch.** On 2,000 positions, legal-move logits agree within 5e-5
  and the top move is the same in 100%. This holds with and without a think time.
- **The inputs the engine builds.** On 2,000 Lichess positions sent through UCI as the real games,
  the inputs equal the training records exactly.
- **Resignation model.** On held-out games, predicted and actual resignation rates agree in every
  range, for example 2.2% against 2.3%, and 8.7% against 8.6%.
- **Full strength.** `bench` at depth 12 gives the same 3,869,083 nodes as 1.19.
