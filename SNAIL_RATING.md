# Snail Ratings List

Start with the engine's Elo, then:

- **+5% of Elo** for every doubling of depth above 20
- **+100** for every doubling of speed above 1 Mnps
- **+60** for every halving of size below 1 MB

Shallower, slower or bigger engines lose points at the same rates. Depth is how deep the engine searches in 10 million nodes on one thread, so it rewards pruning, not speed.

$$\text{Snail Rating} = \text{Elo}\left(1 + \frac{1}{20}\log_2\frac{\text{Depth}}{20}\right) + 100 \log_2(\text{Mnps}) + 60 \log_2\left(\frac{1\ \text{MB}}{\text{Size}}\right)$$

| # | Engine | Rating | Search Speed | Depth | Size | Snail Rating |
|---|---|---|---|---|---|---|
| 1 | c4ke 3.0 | 3307 | 3.03 Mnps | 22.9 | 4 KB | 3979 |
| 2 | **Snail Chess 1.19** | ~3283 | 20.8 Mnps | 22.2 | 95 KB | **~3952** |
| 3 | ice4 6.1 | 3173 | 2.98 Mnps | 31.9 | 4 KB | 3918 |
| 4 | Sirius 9.0 | 3529 | 2.84 Mnps | 27.1 | 537 KB | 3812 |
| 5 | Stockfish 11 | 3563 | 3.70 Mnps | 24.9 | 1.1 MB | 3800 |
| 6 | 4k.c 9.0 | 3085 | 3.01 Mnps | 24.1 | 4 KB | 3770 |
| 7 | 4ku 5.1 | 3058 | 3.15 Mnps | 25.7 | 4 KB | 3759 |
| 8 | Stash 37.0 | 3417 | 3.73 Mnps | 24.2 | 541 KB | 3709 |
| 9 | Berserk 14 | 3739 | 2.85 Mnps | 28.5 | 25 MB | 3705 |
| 10 | Koivisto 9.0 | 3632 | 4.29 Mnps | 27.3 | 15 MB | 3689 |
| 11 | Halogen 16.0.0 | 3721 | 2.54 Mnps | 25.0 | 21 MB | 3651 |
| 12 | Weiss 2.0 | 3319 | 4.32 Mnps | 24.1 | 438 KB | 3649 |
| 13 | Stormphrax 5.0.0 | 3616 | 2.70 Mnps | 27.4 | 9.7 MB | 3645 |
| 14 | Obsidian 16.0 | 3747 | 2.11 Mnps | 26.9 | 31 MB | 3638 |
| 15 | PlentyChess 8.0.0 | 3774 | 1.93 Mnps | 29.8 | 51 MB | 3636 |
| 16 | Caissa 2.0 | 3765 | 2.82 Mnps | 28.3 | 76 MB | 3634 |
| 17 | RubiChess 20240817 | 3692 | 2.69 Mnps | 23.9 | 21 MB | 3618 |
| 18 | Alexandria 9.1.0 | 3745* | 1.92 Mnps | 27.6 | 39 MB | 3609 |
| 19 | Stockfish 17.1 | 3771 | 1.67 Mnps | 31.9 | 76 MB | 3597 |
| 20 | Stockfish 19 | 3793 | 1.82 Mnps | 30.4 | 98 MB | 3596 |
| 21 | pawnocchio 2.0.1 | 3757 | 2.11 Mnps | 26.1 | 67 MB | 3573 |
| 22 | Integral 8 | 3754 | 1.53 Mnps | 29.3 | 62 MB | 3561 |
| 23 | Reckless 0.9.0 | 3767 | 1.57 Mnps | 27.4 | 62 MB | 3560 |
| 24 | Clockwork 20261010 | 3451* | 2.35 Mnps | 27.5 | 3.4 MB | 3548 |
| 25 | Stockfish 18 | 3772 | 1.68 Mnps | 29.4 | 109 MB | 3546 |
| 26 | Zoomies 5.2 | 3600* | 2.23 Mnps | 26.0 | 18 MB | 3532 |
| 27 | Hobbes 3.0 | 3744 | 1.43 Mnps | 27.6 | 63 MB | 3525 |
| 28 | Viridithas 20.0.0 | 3748 | 1.08 Mnps | 29.6 | 54 MB | 3520 |
| 29 | Stormphrax 8.0.0 | 3746 | 1.31 Mnps | 27.0 | 54 MB | 3520 |
| 30 | Arasan 26.1 | 3658* | 1.47 Mnps | 25.6 | 25 MB | 3501 |
| 31 | Stash 26 | 3000* | 6.59 Mnps | 23.0 | 200 KB | 3444 |
| 32 | Seer 2.8.0 | 3640 | 2.25 Mnps | 25.3 | 78 MB | 3442 |
| 33 | Leorik 3.2 | 3492 | 2.75 Mnps | 23.3 | 17 MB | 3430 |
| 34 | Igel 3.7.0 | 3694 | 1.35 Mnps | 27.3 | 107 MB | 3415 |
| 35 | Lizard 10.2 | 3580 | 1.15 Mnps | 21.3 | 18 MB | 3364 |
| 36 | Stash 22 | 2770* | 7.37 Mnps | 19.4 | 641 KB | 3093 |
| 37 | Stash 16.2 | 2220* | 5.54 Mnps | 17.5 | 446 KB | 2518 |
| 38 | Stash 14 | 2059 | 9.14 Mnps | 13.1 | 437 KB | 2389 |
| 39 | MinimalChess 0.6 | 2439 | 1.66 Mnps | 17.0 | 19 MB | 2231 |
| 40 | Stash 12 | 1883 | 11.38 Mnps | 10.8 | 430 KB | 2225 |
| 41 | Stash 10 | 1620* | 11.26 Mnps | 7.8 | 425 KB | 1936 |
| 42 | Stash 8 | 1090* | 7.74 Mnps | 7.8 | 394 KB | 1394 |