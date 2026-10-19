# Snail Chess

An HCE UCI chess engine written in Snail.

## Versions

| Version | Rating | Search Speed | Size | Snail Rating |
|---|---|---|---|---|
| [1.0](https://github.com/CodeAdopter/Snail-Chess/releases/tag/v1.0) | ~1340 | 30.3 Mnps | 46 KB | ~2102 |
| [1.1](https://github.com/CodeAdopter/Snail-Chess/releases/tag/v1.1) | ~1546 | 30.3 Mnps | 45 KB | ~2309 |
| [1.2](https://github.com/CodeAdopter/Snail-Chess/releases/tag/v1.2) | ~1524 | 30.6 Mnps | 45 KB | ~2289 |
| [1.3](https://github.com/CodeAdopter/Snail-Chess/releases/tag/v1.3) | ~1623 | 41.1 Mnps | 46 KB | ~2428 |
| [1.4](https://github.com/CodeAdopter/Snail-Chess/releases/tag/v1.4) | ~1788 | 35.8 Mnps | 48 KB | ~2569 |
| [1.5](https://github.com/CodeAdopter/Snail-Chess/releases/tag/v1.5) | ~1812 | 34.6 Mnps | 49 KB | ~2587 |
| [1.6](https://github.com/CodeAdopter/Snail-Chess/releases/tag/v1.6) | ~1773 | 33.9 Mnps | 49 KB | ~2545 |
| [1.7](https://github.com/CodeAdopter/Snail-Chess/releases/tag/v1.7) | ~2648 | 28.6 Mnps | 52 KB | ~3390 |
| [1.8](https://github.com/CodeAdopter/Snail-Chess/releases/tag/v1.8) | ~2658 | 29.5 Mnps | 50 KB | ~3408 |
| [1.9](https://github.com/CodeAdopter/Snail-Chess/releases/tag/v1.9) | ~2657 | 29.7 Mnps | 52 KB | ~3404 |
| [1.10](https://github.com/CodeAdopter/Snail-Chess/releases/tag/v1.10) | ~2735 | 26.9 Mnps | 52 KB | ~3468 |
| [1.11](https://github.com/CodeAdopter/Snail-Chess/releases/tag/v1.11) | ~2789 | 25.7 Mnps | 53 KB | ~3514 |
| [1.12](https://github.com/CodeAdopter/Snail-Chess/releases/tag/v1.12) | ~2886 | 26.8 Mnps | 52 KB | ~3618 |

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
| 8 | **Snail Chess 1.12** | ~2886 | 26.8 Mnps | 52 KB | **~3618** |
| 9 | Berserk 14 | 3739 | 2.85 Mnps | 25 MB | 3610 |
| 10 | Koivisto 9.0 | 3632 | 4.29 Mnps | 15 MB | 3608 |
| 11 | Weiss 2.0 | 3319 | 4.32 Mnps | 438 KB | 3604 |
| 12 | Halogen 16.0.0 | 3721 | 2.54 Mnps | 21 MB | 3591 |
| 13 | RubiChess 20240817 | 3692 | 2.69 Mnps | 21 MB | 3570 |
| 14 | Stormphrax 5.0.0 | 3616 | 2.70 Mnps | 9.7 MB | 3563 |
| 15 | Obsidian 16.0 | 3747 | 2.11 Mnps | 31 MB | 3558 |
| 16 | Caissa 2.0 | 3765 | 2.82 Mnps | 76 MB | 3540 |
| 17 | PlentyChess 8.0.0 | 3774 | 1.93 Mnps | 51 MB | 3528 |
| 18 | Alexandria 9.1.0 | 3745* | 1.92 Mnps | 39 MB | 3522 |
| 19 | pawnocchio 2.0.1 | 3757 | 2.11 Mnps | 67 MB | 3501 |
| 20 | Stockfish 19 | 3793 | 1.82 Mnps | 98 MB | 3482 |
| 21 | Reckless 0.9.0 | 3767 | 1.57 Mnps | 62 MB | 3475 |
| 22 | Stockfish 17.1 | 3771 | 1.67 Mnps | 76 MB | 3470 |
| 23 | Clockwork 20261010 | 3451* | 2.35 Mnps | 3.4 MB | 3469 |
| 24 | Zoomies 5.2 | 3600* | 2.23 Mnps | 18 MB | 3464 |
| 25 | Integral 8 | 3754 | 1.53 Mnps | 62 MB | 3458 |
| 26 | Stockfish 18 | 3772 | 1.68 Mnps | 109 MB | 3441 |
| 27 | Stormphrax 8.0.0 | 3746 | 1.31 Mnps | 54 MB | 3439 |
| 28 | Hobbes 3.0 | 3744 | 1.43 Mnps | 63 MB | 3438 |
| 29 | Arasan 26.1 | 3658* | 1.47 Mnps | 25 MB | 3435 |
| 30 | Viridithas 20.0.0 | 3748 | 1.08 Mnps | 54 MB | 3414 |
| 31 | Stash 26 | 3000* | 6.59 Mnps | 200 KB | 3414 |
| 32 | Leorik 3.2 | 3492 | 2.75 Mnps | 17 MB | 3391 |
| 33 | Seer 2.8.0 | 3640 | 2.25 Mnps | 78 MB | 3380 |
| 34 | Lizard 10.2 | 3580 | 1.15 Mnps | 18 MB | 3348 |
| 35 | Igel 3.7.0 | 3694 | 1.35 Mnps | 107 MB | 3332 |
| 36 | Stash 22 | 2770* | 7.37 Mnps | 641 KB | 3099 |
| 37 | Stash 16.2 | 2220* | 5.54 Mnps | 446 KB | 2539 |
| 38 | Stash 14 | 2059 | 9.14 Mnps | 437 KB | 2452 |
| 39 | Stash 12 | 1883 | 11.38 Mnps | 430 KB | 2309 |
| 40 | MinimalChess 0.6 | 2439 | 1.66 Mnps | 19 MB | 2259 |
| 41 | Stash 10 | 1620* | 11.26 Mnps | 425 KB | 2045 |
| 42 | Stash 8 | 1090* | 7.74 Mnps | 394 KB | 1468 |

Weights are based on my personal preference, and engines were picked by hand. Search speed comes from each engine's own bench, or a timed search if it doesn't have one. Ratings are from CCRL Blitz, unless marked with * or ~, which means they're estimates.

Want your engine to join the snail race? Open an issue or discussion on GitHub with a link to a release and let me know! 🐌


## Snail 
Snail is a high performance personal programming language

| | Snail | C | C++ | C# | Python | Rust | Zig |
|---|---|---|---|---|---|---|---|
| Runs as | Native | Native | Native | JIT | Interpreted | Native | Native |
| Ease of writing | ★★★★★ | ★★☆☆☆ | ★★☆☆☆ | ★★★★☆ | ★★★★★ | ★★☆☆☆ | ★★★☆☆ |
| Maintainability | ★★★★★ | ★★☆☆☆ | ★★☆☆☆ | ★★★★☆ | ★★★☆☆ | ★★★★☆ | ★★★☆☆ |
| Performance | ★★★★★ | ★★★★★ | ★★★★★ | ★★★★☆ | ★☆☆☆☆ | ★★★★★ | ★★★★★ |
| Effort for fast code | Low | High | High | Medium | Very high | Medium | Medium |
| Runs everywhere | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Memory safety | ✗ | ✗ | ✗ | ✓ | ✓ | ✓ | Partial |
| Compile-time code | `[us: Side]` | Macros | Templates | Generics | None | Generics | `comptime` |

| Test | Snail | C | C++ | C# | Python | Rust | Zig |
|---|---|---|---|---|---|---|---|
| N-Queens, boards 1 to 15 | 0.95 s | 0.96 s | 0.96 s | 1.04 s | 42.7 s | 0.96 s | 1.07 s |
| Particles, 1,000 for 200,000 steps | 0.20 s | 0.21 s | 0.21 s | 0.40 s | 124 s | 0.20 s | 0.21 s |
| Knight paths on bitboards | 0.11 s | 0.11 s | 0.11 s | 0.23 s | 50.0 s | 0.11 s | 0.11 s |
| Sort 10 million numbers | 0.58 s | 0.88 s | 0.60 s | 0.61 s | 5.46 s | 0.16 s | 0.85 s |
| Time overall, Snail = 1 | 1.00 | 1.14 | 1.02 | 1.49 | 105 | 0.72 | 1.15 |
| Lines of code, all four tests | 97 | 117 | 106 | 100 | 75 | 145 | 125 |

## License

Copyright 2026 Angelo Wolff. Snail Chess is free software under the GNU General Public License v3, see LICENSE.
