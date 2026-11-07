# Snail Chess 1.18

| Rating | Search Speed | Size | Snail Rating |
|---|---|---|---|
| ~3288 | 20.9 Mnps | 95 KB | ~3933 |

## Engine

| Change | Rating | SPRT | Search Speed | Size |
|---|---|---|---|---|
| Code cleanup | ±0 | - | ±0% | -3.5 KB |
| Late move reduction terms | +23 | +23 ± 13 | -4% | ±0 KB |
| Shell weights from 200k-node self-play | +66 | +23 ± 11 | +1% | ±0 KB |
| 64 Shell lanes | -31 | +47 ± 14 | -7% | +17 KB |
| Shell sum with pmaddwd | ±0 | - | +2% | -2 KB |

## Compiler

- Widened i16 vector sums compile to pmaddwd

## Testing

| Opponent | Games | Score |
|---|---|---|
| Stash 16 | 50 | +49 =1 -0 |
| Stash 22 | 50 | +45 =5 -0 |
| Stash 26 | 50 | +39 =7 -4 |
| Snail Chess 1.17 (SPRT) | 208 | +76 =94 -38 |
