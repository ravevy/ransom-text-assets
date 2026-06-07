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
  !/          # 7 variants
  #/          # 6 variants
  ...
```

Each character has its own directory containing numbered `.webp` files (`0.webp`, `1.webp`, …). The ransom-text package picks randomly among these variants to give each rendered character a unique look.

## Coverage

### Letters

| Letter                | Variants | Letter                | Variants | Letter                | Variants |
| --------------------- | -------- | --------------------- | -------- | --------------------- | -------- |
| [A](letters/A/0.webp) | 35       | [J](letters/J/0.webp) | 17       | [S](letters/S/0.webp) | 38       |
| [B](letters/B/0.webp) | 18       | [K](letters/K/0.webp) | 17       | [T](letters/T/0.webp) | 19       |
| [C](letters/C/0.webp) | 17       | [L](letters/L/0.webp) | 20       | [U](letters/U/0.webp) | 16       |
| [D](letters/D/0.webp) | 19       | [M](letters/M/0.webp) | 24       | [V](letters/V/0.webp) | 17       |
| [E](letters/E/0.webp) | 25       | [N](letters/N/0.webp) | 27       | [W](letters/W/0.webp) | 16       |
| [F](letters/F/0.webp) | 18       | [O](letters/O/0.webp) | 21       | [X](letters/X/0.webp) | 11       |
| [G](letters/G/0.webp) | 18       | [P](letters/P/0.webp) | 18       | [Y](letters/Y/0.webp) | 21       |
| [H](letters/H/0.webp) | 16       | [Q](letters/Q/0.webp) | 15       | [Z](letters/Z/0.webp) | 18       |
| [I](letters/I/0.webp) | 21       | [R](letters/R/0.webp) | 25       |                       |          |

### Digits

| Digit                 | Variants |
| --------------------- | -------- |
| [0](letters/0/0.webp) | 9        |
| [1](letters/1/0.webp) | 11       |
| [2](letters/2/0.webp) | 8        |
| [3](letters/3/0.webp) | 14       |
| [4](letters/4/0.webp) | 24       |
| [5](letters/5/0.webp) | 10       |
| [6](letters/6/0.webp) | 11       |
| [7](letters/7/0.webp) | 15       |
| [8](letters/8/0.webp) | 9        |
| [9](letters/9/0.webp) | 9        |

### Special Characters

| Char                     | Variants | Char                   | Variants | Char                   | Variants |
| ------------------------ | -------- | ---------------------- | -------- | ---------------------- | -------- |
| [!](letters/!/0.webp)    | 7        | [\*](letters/*/0.webp) | 6        | [?](letters/?/0.webp)  | 8        |
| [#](letters/%23/0.webp)  | 6        | [+](letters/+/0.webp)  | 5        | [@](letters/@/0.webp)  | 3        |
| [%](letters/%25/0.webp)  | 8        | [,](letters/,/0.webp)  | 4        | [\[](letters/[/0.webp) | 3        |
| [&](letters/&/0.webp)    | 9        | [-](letters/-/0.webp)  | 4        | [\]](letters/]/0.webp) | 3        |
| [\(](letters/(/0.webp)   | 5        | [:](letters/:/0.webp)  | 3        | [^](letters/^/0.webp)  | 2        |
| [\)](<letters/)/0.webp>) | 5        |                        |          |                        |          |

## Asset format

All images are `.webp`, optimized for web delivery. Maximum dimensions are 512×512 px.

## File sizes & performance

- **Total assets:** 728 `.webp` files, ~26 MB on disk
- **Per-file range:** ~1.8 KB (smallest) to ~121 KB (largest)
- **Average file size:** ~36 KB per image

## Usage

This repo is consumed as a dependency by the ransom-text package. You do not need to clone it directly unless you are adding new letter variants.
