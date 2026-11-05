# Cloud underlighting at sunset

A to-scale, interactive animation showing how Earth's shadow rises past cloud bases after sunset, and when a cloud is lit from below.

**Live page:** https://cramshorn2.github.io/cloud-underlighting/

## What it shows

- A 68 km wide cross-section at 1 px = 0.1 km on both axes, west on the left.
- An observer under a cloud, with two further clouds 29 km west and east. All cloud bases are at 6 km.
- t = 0 is the observer's sunset: the sun is on the observer's horizon and the sunset point is at the observer.
- The grazing ray (edge of Earth's shadow), parallel sun rays at 1 km intervals, the shadow itself, and the parts of each cloud base lit from below.
- The distance from the observer to the sunset point, where the grazing ray touches the Earth.

Frames are 0.25 min apart. The window depends on the rate selected, and each covers sun elevations at the observer from +2.75° to −1.125°:

| Rate | Window | Frames |
|---|---|---|
| Equator, equinox | −11 to +4.5 min | 63 |
| Basel, equinox | −16.5 to +6.75 min | 94 |
| Basel, solstice | −20.25 to +8.5 min | 116 |

Changing the rate keeps the current sun elevation and jumps to the matching frame. In every window the shadow edge stays below the 6 km cloud bases.

## Controls

| Control | Effect |
|---|---|
| Play / Pause | Starts or stops the loop (250 ms per frame) |
| Slider | Steps to a single frame |
| Rate selector | Rate of solar descent: equator at equinox (15.0°/h), Basel at equinox (10.1°/h), Basel at solstice (8.2°/h) |

The readout below the controls gives the time, the sun's elevation at the observer, the height of the shadow edge above the observer, the distance to the sunset point and the state of each cloud base.

## Model

Spherical Earth (R = 6371 km), no refraction, constant rate of solar descent. See [docs/geometry.md](docs/geometry.md) for the derivations, the reference tables and the model's limitations.

## Running locally

The page is a single self-contained HTML file with no dependencies or build step. Open `index.html` in a browser.

`index.html` wraps the animation code in a page shell with explanatory text. The shell supplies the colours and the 680 px width that the original chat widget took from its host; the system sans-serif font stands in for the original interface font.

## Deployment

The site is served by GitHub Pages from the root of the `gh-pages` branch, which mirrors `main`. To publish changes, push `main` and then update `gh-pages`:

```
git push origin main
git push origin main:gh-pages
```

## Licence

MIT. See [LICENSE](LICENSE).
