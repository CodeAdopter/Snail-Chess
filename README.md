# Snail Chess

A UCI chess engine written in Snail.

Snail Chess evaluates material only. No piece-square tables, no NNUE.

## Versions

| Version | Rating | Speed | Size | Snail Rating |
|---|---|---|---|---|
| 1.0.0 | ~1340 | 29.6 Mnps | 298 KB | ~1935 |

Snail Rating = Rating + 100 × log2(Mnps) + 60 × log2(1 MB / Size)

Every doubling of speed adds 100, and every halving of the executable adds 60.

## Snail Ratings List

| # | Engine | Rating | Speed | Size | Snail Rating |
|---|---|---|---|---|---|
| 1 | c4ke 3.0 | 3307 | 3.03 Mnps | 4 KB | 3947 |
| 2 | ice4 6.1 | 3173 | 2.98 Mnps | 4 KB | 3811 |
| 3 | Stockfish 11 | 3563 | 3.70 Mnps | 1.1 MB | 3743 |
| 4 | Sirius 9.0 | 3529 | 2.84 Mnps | 537 KB | 3735 |
| 5 | 4k.c 9.0 | 3085 | 3.01 Mnps | 4 KB | 3728 |
| 6 | 4ku 5.1 | 3058 | 3.15 Mnps | 4 KB | 3704 |
| 7 | Stash 37.0 | 3417 | 3.73 Mnps | 541 KB | 3662 |
| 8 | Berserk 14 | 3739 | 2.85 Mnps | 25 MB | 3610 |
| 9 | Koivisto 9.0 | 3632 | 4.29 Mnps | 15 MB | 3608 |
| 10 | Weiss 2.0 | 3319 | 4.32 Mnps | 438 KB | 3604 |
| 11 | Halogen 16.0.0 | 3721 | 2.54 Mnps | 21 MB | 3591 |
| 12 | RubiChess 20240817 | 3692 | 2.69 Mnps | 21 MB | 3570 |
| 13 | Stormphrax 5.0.0 | 3616 | 2.70 Mnps | 9.7 MB | 3563 |
| 14 | Obsidian 16.0 | 3747 | 2.11 Mnps | 31 MB | 3558 |
| 15 | Caissa 2.0 | 3765 | 2.82 Mnps | 76 MB | 3540 |
| 16 | PlentyChess 8.0.0 | 3774 | 1.93 Mnps | 51 MB | 3528 |
| 17 | Alexandria 9.1.0 | 3745* | 1.92 Mnps | 39 MB | 3522 |
| 18 | pawnocchio 2.0.1 | 3757 | 2.11 Mnps | 67 MB | 3501 |
| 19 | Stockfish 19 | 3793 | 1.82 Mnps | 98 MB | 3482 |
| 20 | Reckless 0.9.0 | 3767 | 1.57 Mnps | 62 MB | 3475 |
| 21 | Stockfish 17.1 | 3771 | 1.67 Mnps | 76 MB | 3470 |
| 22 | Clockwork 20261010 | 3451* | 2.35 Mnps | 3.4 MB | 3469 |
| 23 | Zoomies 5.2 | 3600* | 2.23 Mnps | 18 MB | 3464 |
| 24 | Integral 8 | 3754 | 1.53 Mnps | 62 MB | 3458 |
| 25 | Stockfish 18 | 3772 | 1.68 Mnps | 109 MB | 3441 |
| 26 | Stormphrax 8.0.0 | 3746 | 1.31 Mnps | 54 MB | 3439 |
| 27 | Hobbes 3.0 | 3744 | 1.43 Mnps | 63 MB | 3438 |
| 28 | Arasan 26.1 | 3658* | 1.47 Mnps | 25 MB | 3435 |
| 29 | Viridithas 20.0.0 | 3748 | 1.08 Mnps | 54 MB | 3414 |
| 30 | Stash 26 | 3000* | 6.59 Mnps | 200 KB | 3414 |
| 31 | Leorik 3.2 | 3492 | 2.75 Mnps | 17 MB | 3391 |
| 32 | Seer 2.8.0 | 3640 | 2.25 Mnps | 78 MB | 3380 |
| 33 | Lizard 10.2 | 3580 | 1.15 Mnps | 18 MB | 3348 |
| 34 | Igel 3.7.0 | 3694 | 1.35 Mnps | 107 MB | 3332 |
| 35 | Stash 22 | 2770* | 7.37 Mnps | 641 KB | 3099 |
| 36 | Stash 16.2 | 2220* | 5.54 Mnps | 446 KB | 2539 |
| 37 | Stash 14 | 2059 | 9.14 Mnps | 437 KB | 2452 |
| 38 | Stash 12 | 1883 | 11.38 Mnps | 430 KB | 2309 |
| 39 | MinimalChess 0.6 | 2439 | 1.66 Mnps | 19 MB | 2259 |
| 40 | Stash 10 | 1620* | 11.26 Mnps | 425 KB | 2045 |
| 41 | **Snail Chess 1.0.0** | ~1340 | 29.57 Mnps | 298 KB | **~1935** |
| 42 | Stash 8 | 1090* | 7.74 Mnps | 394 KB | 1468 |

## License

Copyright 2026 Angelo Wolff. Snail Chess is free software under the GNU General Public License v3, see LICENSE.
