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
  bang/       # ! — 7 variants
  num/        # # — 6 variants
  pct/        # % — 8 variants
  amp/        # & — 9 variants
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

| Char | Folder                          | Variants | Char | Folder                            | Variants | Char | Folder                              | Variants |
| ---- | ------------------------------- | -------- | ---- | --------------------------------- | -------- | ---- | ----------------------------------- | -------- |
| !    | [bang](letters/bang/0.webp)     | 7        | \*   | [star](letters/star/0.webp)       | 6        | ?    | [quest](letters/quest/0.webp)       | 8        |
| #    | [num](letters/num/0.webp)       | 6        | +    | [plus](letters/plus/0.webp)       | 5        | @    | [at](letters/at/0.webp)             | 3        |
| %    | [pct](letters/pct/0.webp)       | 8        | ,    | [comma](letters/comma/0.webp)     | 4        | \[   | [lbracket](letters/lbracket/0.webp) | 3        |
| &    | [amp](letters/amp/0.webp)       | 9        | -    | [dash](letters/dash/0.webp)       | 4        | \]   | [rbracket](letters/rbracket/0.webp) | 3        |
| (    | [lparen](letters/lparen/0.webp) | 5        | :    | [colon](letters/colon/0.webp)     | 3        | ^    | [caret](letters/caret/0.webp)       | 2        |
| )    | [rparen](letters/rparen/0.webp) | 5        |      |                                   |          |      |                                     |          |

## Special character folder naming

Special characters use short symbolic names instead of the literal character as the folder name (e.g. `bang/` for `!`, `quest/` for `?`). This avoids URL encoding problems: characters like `?`, `#`, `%`, `(`, `)`, and `^` are reserved or unsafe in URLs and require percent-encoding when used as path segments — which causes issues in browser URLs, CDN paths, and some tooling. Plain ASCII names have no such restrictions.

Full mapping:

| Character | Folder     | Character | Folder      |
| --------- | ---------- | --------- | ----------- |
| !         | `bang`     | +         | `plus`      |
| #         | `num`      | ,         | `comma`     |
| %         | `pct`      | -         | `dash`      |
| &         | `amp`      | :         | `colon`     |
| (         | `lparen`   | ?         | `quest`     |
| )         | `rparen`   | @         | `at`        |
| *         | `star`     | [         | `lbracket`  |
|           |            | ]         | `rbracket`  |
|           |            | ^         | `caret`     |

## Asset format

All images are `.webp`, optimized for web delivery. Maximum dimensions are 512×512 px.

## File sizes & performance

- **Total assets:** 728 `.webp` files, ~26 MB on disk
- **Per-file range:** ~1.8 KB (smallest) to ~121 KB (largest)
- **Average file size:** ~36 KB per image

## Usage

This repo is consumed as a dependency by the ransom-text package. You do not need to clone it directly unless you are adding new letter variants.
