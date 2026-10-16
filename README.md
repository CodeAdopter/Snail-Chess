# Snail Chess

A UCI chess engine written in Snail.

Snail Chess evaluates material only. No piece-square tables, no NNUE.

## Versions

| Version | Rating | Speed | Size | Snail Rating |
|---|---|---|---|---|
| 1.0.0 | ~1340 | 30.5 Mnps | 298 KB | ~2011 |

Snail Rating = Rating + 100 × log2(Mnps) + 100 × log2(1 MB / Size)

Every doubling of speed adds 100, and every halving of the executable adds 100.

## License

Copyright 2026 Angelo Wolff. Snail Chess is free software under the GNU General Public License v3, see LICENSE.
