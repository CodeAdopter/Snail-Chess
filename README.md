# Snail Chess

A UCI chess engine written in Snail.

Snail Chess evaluates material only. No piece-square tables, no NNUE.

## Versions

| Version | Rating | Search Speed | Size | Snail Rating |
|---|---|---|---|---|
| [1.0](https://github.com/CodeAdopter/Snail-Chess/releases/tag/v1.0) | ~1340 | 30.3 Mnps | 46 KB | ~2102 |
| [1.1](https://github.com/CodeAdopter/Snail-Chess/releases/tag/v1.1) | ~1546 | 30.3 Mnps | 45 KB | ~2309 |
| [1.2](https://github.com/CodeAdopter/Snail-Chess/releases/tag/v1.2) | ~1524 | 30.6 Mnps | 45 KB | ~2289 |
| [1.3](https://github.com/CodeAdopter/Snail-Chess/releases/tag/v1.3) | ~1623 | 41.1 Mnps | 46 KB | ~2428 |
| [1.4](https://github.com/CodeAdopter/Snail-Chess/releases/tag/v1.4) | ~1788 | 35.8 Mnps | 48 KB | ~2569 |
| [1.5](https://github.com/CodeAdopter/Snail-Chess/releases/tag/v1.5) | ~1812 | 34.6 Mnps | 49 KB | ~2587 |

Start with the engine's Elo, then:

- **+100** for every doubling of speed above 1 Mnps
- **+60** for every halving of size below 1 MB

Slower or bigger engines lose points at the same rates.

$$\text{Snail Rating} = \text{Elo} + 100 \log_2(\text{Mnps}) + 60 \log_2\left(\frac{1\ \text{MB}}{\text{Size}}\right)$$

## Snail Ratings List

| # | Engine | Rating | Search Speed | Size | Snail Rating |
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
| 36 | **Snail Chess 1.5** | ~1812 | 34.6 Mnps | 49 KB | **~2587** |
| 37 | Stash 16.2 | 2220* | 5.54 Mnps | 446 KB | 2539 |
| 38 | Stash 14 | 2059 | 9.14 Mnps | 437 KB | 2452 |
| 39 | Stash 12 | 1883 | 11.38 Mnps | 430 KB | 2309 |
| 40 | MinimalChess 0.6 | 2439 | 1.66 Mnps | 19 MB | 2259 |
| 41 | Stash 10 | 1620* | 11.26 Mnps | 425 KB | 2045 |
| 42 | Stash 8 | 1090* | 7.74 Mnps | 394 KB | 1468 |

Weights are based on my personal preference, and engines were picked by hand. Search speed comes from each engine's own bench, or a timed search if it doesn't have one. Ratings are from CCRL Blitz, unless marked with * or ~, which means they're estimates.

Want your engine to join the snail race? Open an issue or discussion on GitHub with a link to a release and let me know! 🐌

## License

Copyright 2026 Angelo Wolff. Snail Chess is free software under the GNU General Public License v3, see LICENSE.
