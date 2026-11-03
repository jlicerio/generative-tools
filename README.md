# Generative tools

Small web tools built for design work. Each instrument takes a process that is awkward to draw by hand,
gives it a seed, a panel and an export, and stops there.

Live: **<https://jlicerio.github.io/generative-tools/>**

| # | Tool | What it does |
|---|---|---|
| 01 | [Growth instrument](growth-instrument/) | Five organic growth systems, ramp dithering, volume export |

## 01 · Growth instrument

Eight natural-growth formulas exist; five are built. Each one grows from a typed integer seed. The same seed, system and shape settings always draw the
same form.

| System | Method |
|---|---|
| DLA | Biased random walk with a hash-grid contact test, 80 walkers in flight |
| Physarum | 5 000 agents, three sensors, deposit and decay on a trail map |
| Reaction-diffusion | Gray-Scott on a 180 × 240 grid |
| Differential growth | Repulsion, edge attraction and insertion on a closed loop |
| Space colonisation | Attractor-driven branching |

Controls: system, play and restart, speed, growth amount, seed, per-system shape parameters, render mode,
dither mode, cell size, contrast, bands, ramp, volume contours, particle count.

Exports:

- **PNG** at 2×.
- **SVG** for the vector systems, with the ramp as a real gradient.
- **GLB** — a voxel mesh with vertex colours, opens in Blender.
- **PLY** — a particle cloud, 25k to 400k points, with colour, size, glyph, contour band and density per
  particle.
- **ASCII** — 44 × 58 × 14 volume slices, Bayer-dithered.

Volume exports unlock when the form is paused or finished, because a running form makes a different mesh
every frame.

### Use

Open the link. Everything runs in the page; there is no build step and no network access after load.
The state is in the URL, so a form is addressable:

```
growth-instrument/?s=dla&seed=3574968473&g=90&pal=acid&bands=6&contours=6&points=100000&step=1500
```

## Credit

Built after a reel by [@rohannewman](https://www.instagram.com/rohannewman/), who demonstrated a similar
instrument. The algorithms are standard published methods; the panel, the ramp compositor, the volume
pipeline and the exports are mine. No asset from that account is included.

## Licence

MIT. See [LICENSE](LICENSE).
