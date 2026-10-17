# Snail Chess 1.0

Commit af9ed78

| Rating | Search Speed | Size | Snail Rating |
|---|---|---|---|
| ~1340 | 30.3 Mnps | 46 KB | ~2102 |

## Engine

- Bitboards with PEXT attacks
- Material-only evaluation
- Iterative deepening alpha-beta
- Transposition table
- Quiescence search with delta pruning
- MVV-LVA and killer move ordering
- Lazy SMP multithreading
- Simple time management
- UCI protocol
- Perft, nps and bench commands

## Compiler

- Reduced executable size by 85%

## Testing

| Opponent | Games | Score |
|---|---|---|
| Stash 8 | 150 | +81 =66 -3 |
| Stash 10 | 16 | +4 =5 -7 |
