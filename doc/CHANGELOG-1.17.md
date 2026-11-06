# Snail Chess 1.17

| Rating | Search Speed | Size | Snail Rating |
|---|---|---|---|
| ~3230 | 22.8 Mnps | 84 KB | ~3898 |

## Engine

| Change | Rating | SPRT | Search Speed | Size |
|---|---|---|---|---|
| Shell weights from 20k-node self-play | +52 | +18 ± 8 | -1% | ±0 KB |
| Shell weights from 50k-node self-play | +55 | +27 ± 13 | +2% | ±0 KB |
| Shell weights from 100k-node self-play | ±0 | +21 ± 11 | +1% | ±0 KB |
| Late move pruning | -34 | +33 ± 13 | -10% | ±0 KB |
| Continuation history | +101 | +34 ± 18 | -1% | +0.5 KB |

## Compiler

- No changes

## Testing

| Opponent | Games | Score |
|---|---|---|
| Stash 16 | 50 | +50 =0 -0 |
| Stash 22 | 50 | +46 =2 -2 |
| Stash 26 | 50 | +34 =10 -6 |
| Snail Chess 1.16 (SPRT) | 208 | +89 =81 -38 |
