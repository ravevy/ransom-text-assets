# ransom-text-assets

Static image assets for the [ransom-text](https://github.com/ravevy/ransom-text) package — a collection of cut-out letter images in the style of classic ransom notes.

## Structure

```
letters/
  A/          # 35 variants
  B/          # 18 variants
  ...
  Z/          # 18 variants
  0–9/        # digit variants
```

Each character has its own directory containing numbered `.webp` files (`0.webp`, `1.webp`, …). The ransom-text package picks randomly among these variants to give each rendered character a unique look.

## Coverage

### Letters

| Letter | Variants | Letter | Variants | Letter | Variants |
| ------ | -------- | ------ | -------- | ------ | -------- |
| A      | 35       | J      | 17       | S      | 38       |
| B      | 18       | K      | 17       | T      | 19       |
| C      | 17       | L      | 20       | U      | 16       |
| D      | 19       | M      | 24       | V      | 17       |
| E      | 25       | N      | 27       | W      | 16       |
| F      | 18       | O      | 21       | X      | 11       |
| G      | 18       | P      | 18       | Y      | 21       |
| H      | 16       | Q      | 15       | Z      | 18       |
| I      | 21       | R      | 25       |        |          |

### Digits

| Digit | Variants |
| ----- | -------- |
| 0     | 9        |
| 1     | 11       |
| 2     | 8        |
| 3     | 14       |
| 4     | 24       |
| 5     | 10       |
| 6     | 11       |
| 7     | 15       |
| 8     | 9        |
| 9     | 9        |

## Asset format

All images are `.webp`, optimized for web delivery.

## File sizes & performance

- **Total assets:** 647 `.webp` files, ~24 MB on disk
- **Per-file range:** ~1.8 KB (smallest) to ~121 KB (largest)
- **Average file size:** ~36 KB per image

## Usage

This repo is consumed as a dependency by the ransom-text package. You do not need to clone it directly unless you are adding new letter variants.
