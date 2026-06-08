# slitscan demo

Static demo site for [slitscan-cli](https://github.com/zakhap/slitscan-cli), a Python CLI toolkit for time-displacement slit-scan rendering of video.

## Viewing

Open `index.html` directly in a browser. All media is local — no server needed.

```
open index.html
```

## What's here

Each section of the site demonstrates one technique independently, with the CLI command that produced it.

| Technique | What it shows |
|-----------|---------------|
| Profiles | `ramp`, `tent`, `reverse` delay surfaces |
| Axis | `--axis x` (column bands) vs `--axis y` (row bands) |
| Temporal spread | `--max-delay 300`, `900`, and full-width (default) |
| Slice width | `--slice-width 1` smooth gradient vs wider banded mode |
| Fill & looping | `--fill black` vs `--fill wrap` for seamless infinite loops |
| Modulation | LFO oscillators on `vanguard`, `max_delay`, or both simultaneously |
| Collapse | `slitscan collapse` — strip photography / photofinish images |
| GIF | `.gif` output with palette quantization and dithering |
| Trumbull | `--slit-source` fixed-slit gather (2001: A Space Odyssey effect) |

## Source footage

All examples use a single 1280×720 30fps clip (992 frames, ~33 seconds).

## Tool

Source and full documentation: [github.com/zakhap/slitscan-cli](https://github.com/zakhap/slitscan-cli)

```
pip install -e ../slitscan-cli
slitscan render input.mp4 output.mp4 --profile ramp --fill wrap
slitscan collapse input.mp4 photofinish.png --slit-position 0.5
```
