# Cloud underlighting at sunset

A to-scale, interactive animation showing how Earth's shadow rises past cloud bases after sunset, and when a cloud is lit from below.

**Live page:** https://cramshorn2.github.io/cloud-underlighting/

## What it shows

- A 68 km wide cross-section at 1 px = 0.1 km on both axes, west on the left.
- An observer under a cloud, with two further clouds 29 km west and east. All cloud bases are at 6 km.
- At t = 0 the sun is 2.27° below the observer's horizon, so the edge of Earth's shadow passes 5 km above the observer. This reference point is the same for every rate.
- The grazing ray (edge of Earth's shadow), parallel sun rays at 1 km intervals, the shadow itself, and the parts of each cloud base lit from below.
- The distance from the observer to the sunset point, where the grazing ray touches the Earth.

Frames run from t = −11 min to t = +4.5 min in 0.25 min steps (63 frames) for every rate. Changing the rate keeps the current frame.

What happens within the window depends on the rate:

| Rate | Observer's sunset | Sun elevation at observer, start → end | Sunset point at start |
|---|---|---|---|
| Equator, equinox | t ≈ −9.1 min | +0.48° → −3.39° | 53.5 km east |
| Basel, equinox | t ≈ −13.4 min (before window) | −0.41° → −3.03° | 45.8 km west |
| Basel, solstice | t ≈ −16.6 min (before window) | −0.77° → −2.88° | 85.6 km west |

So the sunset point is east of the observer only at the equator rate, before t ≈ −9.1 min. At the equator rate the cloud bases go dark between about t = −0.3 min (east end of the east cloud) and t = +2.2 min (west end of the west cloud).

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

`index.html` wraps the animation code, unchanged from the final chat version, in a page shell with explanatory text. The shell supplies the colours and the 680 px width that the original chat widget took from its host; the system sans-serif font stands in for the original interface font.

## Deployment

The site is served by GitHub Pages from the root of the `gh-pages` branch, which mirrors `main`. To publish changes, push `main` and then update `gh-pages`:

```
git push origin main
git push origin main:gh-pages
```

## Licence

MIT. See [LICENSE](LICENSE).
