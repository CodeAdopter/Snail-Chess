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
| 1 | Stockfish 11 | 3563 | 3.70 Mnps | 1.1 MB | 3737 |
| 2 | Stash 37.0 | 3417 | 3.73 Mnps | 541 KB | 3699 |
| 3 | Stash 26 | 3000* | 6.59 Mnps | 200 KB | 3508 |
| 4 | Stormphrax 5.0.0 | 3616 | 2.70 Mnps | 9.7 MB | 3432 |
| 5 | Zoomies 5.2 | 3600* | 2.23 Mnps | 18 MB | 3297 |
| 6 | Stockfish 17.1 | 3771 | 1.67 Mnps | 76 MB | 3220 |
| 7 | Lizard 10.2 | 3580 | 1.15 Mnps | 18 MB | 3180 |
| 8 | Stockfish 18 | 3772 | 1.68 Mnps | 109 MB | 3170 |
| 9 | Stash 22 | 2770* | 7.37 Mnps | 641 KB | 3126 |
| 10 | Stash 16.2 | 2220* | 5.54 Mnps | 446 KB | 2587 |
| 11 | Stash 14 | 2059 | 9.14 Mnps | 437 KB | 2501 |
| 12 | Stash 12 | 1883 | 11.38 Mnps | 430 KB | 2359 |
| 13 | Stash 10 | 1620* | 11.26 Mnps | 425 KB | 2096 |
| 14 | **Snail Chess 1.0.0** | ~1340 | 29.57 Mnps | 298 KB | **~2007** |
| 15 | Stash 8 | 1090* | 7.74 Mnps | 394 KB | 1523 |

## License

Copyright 2026 Angelo Wolff. Snail Chess is free software under the GNU General Public License v3, see LICENSE.
