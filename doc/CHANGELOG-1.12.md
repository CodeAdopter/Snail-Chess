# Snail Chess 1.12

| Rating | Search Speed | Size | Snail Rating |
|---|---|---|---|
| ~2886 | 26.8 Mnps | 52 KB | ~3618 |

## Engine

| Change | Rating | SPRT | Search Speed | Size |
|---|---|---|---|---|
| Texel-tuned evaluation weights | +97 | +129 ± 39 | +4% | ±0 KB |
| Search bookkeeping | ±0 | - | ±0% | ±0 KB |
| Fixed 2 MB hash table | - | +17 ± 25 | ±0% | -0.5 KB |

## Compiler

- No changes

## Testing

| Opponent | Games | Score |
|---|---|---|
| Stash 16 | 50 | +49 =1 -0 |
| Stash 22 | 50 | +28 =10 -12 |
| Stash 26 | 50 | +10 =13 -27 |
| Snail Chess 1.11 (SPRT) | 208 | +109 =64 -35 |
