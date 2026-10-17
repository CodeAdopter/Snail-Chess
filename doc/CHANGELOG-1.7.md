# Snail Chess 1.7

| Rating | Search Speed | Size | Snail Rating |
|---|---|---|---|
| ~2648 | 28.6 Mnps | 52 KB | ~3390 |

## Engine

| Change | Rating | SPRT | Search Speed | Size |
|---|---|---|---|---|
| Min HCE | +613 | +439 ± 101 | -3% | -0.5 KB |
| Pawn structure | +129 | +111 ± 35 | -11% | +0.5 KB |
| Pawn threats, king shield, rook files | +69 | +123 ± 37 | -9% | +2.5 KB |
| Pawn entry reused in quiescence | +64 | +9 ± 26 | +5% | +0.5 KB |

## Compiler

- No changes

## Testing

| Opponent | Games | Score |
|---|---|---|
| Stash 16 | 50 | +45 =2 -3 |
| Stash 22 | 50 | +11 =8 -31 |
| Stash 26 | 50 | +5 =5 -40 |
| Snail Chess 1.6 (SPRT) | 156 | +145 =8 -3 |
