# Snail Chess

A UCI chess engine written in Snail.

Snail Chess evaluates material only. No piece-square tables, no NNUE.

## Versions

| Version | Rating | Speed | Size | Snail Rating |
|---|---|---|---|---|
| 1.0.0 | ~1340 | 29.6 Mnps | 298 KB | ~2007 |

Snail Rating = Rating + 100 × log2(Mnps) + 100 × log2(1 MB / Size)

Every doubling of speed adds 100, and every halving of the executable adds 100.

## Snail Ratings List

| # | Engine | Rating | Speed | Size | Snail Rating |
|---|---|---|---|---|---|
| 1 | c4ke 3.0 | 3307 | 3.03 Mnps | 4 KB | 4267 |
| 2 | 4ku 5.1 | 3058 | 3.15 Mnps | 4 KB | 4024 |
| 3 | Stockfish 11 | 3563 | 3.70 Mnps | 1.1 MB | 3737 |
| 4 | Stash 37.0 | 3417 | 3.73 Mnps | 541 KB | 3699 |
| 5 | Stash 26 | 3000* | 6.59 Mnps | 200 KB | 3508 |
| 6 | Stormphrax 5.0.0 | 3616 | 2.70 Mnps | 9.7 MB | 3432 |
| 7 | Berserk 14 | 3739 | 2.85 Mnps | 25 MB | 3424 |
| 8 | Clockwork 20261010 | 3451* | 2.35 Mnps | 3.4 MB | 3399 |
| 9 | Obsidian 16.0 | 3747 | 2.11 Mnps | 31 MB | 3361 |
| 10 | PlentyChess 8.0.0 | 3774 | 1.93 Mnps | 51 MB | 3300 |
| 11 | Zoomies 5.2 | 3600* | 2.23 Mnps | 18 MB | 3297 |
| 12 | pawnocchio 2.0.1 | 3757 | 2.11 Mnps | 67 MB | 3258 |
| 13 | Reckless 0.9.0 | 3767 | 1.57 Mnps | 62 MB | 3237 |
| 14 | Stockfish 17.1 | 3771 | 1.67 Mnps | 76 MB | 3220 |
| 15 | Stockfish 19 | 3793 | 1.82 Mnps | 98 MB | 3218 |
| 16 | Stormphrax 8.0.0 | 3746 | 1.31 Mnps | 54 MB | 3209 |
| 17 | Hobbes 3.0 | 3744 | 1.43 Mnps | 63 MB | 3199 |
| 18 | Lizard 10.2 | 3580 | 1.15 Mnps | 18 MB | 3180 |
| 19 | Stockfish 18 | 3772 | 1.68 Mnps | 109 MB | 3170 |
| 20 | Stash 22 | 2770* | 7.37 Mnps | 641 KB | 3126 |
| 21 | Stash 16.2 | 2220* | 5.54 Mnps | 446 KB | 2587 |
| 22 | Stash 14 | 2059 | 9.14 Mnps | 437 KB | 2501 |
| 23 | Stash 12 | 1883 | 11.38 Mnps | 430 KB | 2359 |
| 24 | Stash 10 | 1620* | 11.26 Mnps | 425 KB | 2096 |
| 25 | **Snail Chess 1.0.0** | ~1340 | 29.57 Mnps | 298 KB | **~2007** |
| 26 | Stash 8 | 1090* | 7.74 Mnps | 394 KB | 1523 |

## License

Copyright 2026 Angelo Wolff. Snail Chess is free software under the GNU General Public License v3, see LICENSE.
