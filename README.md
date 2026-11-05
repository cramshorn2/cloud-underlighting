# Cloud underlighting at sunset

A to-scale, interactive animation showing how Earth's shadow rises past cloud bases after sunset, and when a cloud is lit from below.

**Live page:** https://cramshorn2.github.io/cloud-underlighting/

## What it shows

- A 68 km wide cross-section at 1 px = 0.1 km on both axes, west on the left.
- An observer under a cloud, with two further clouds 29 km west and east. All cloud bases are at 6 km.
- At t = 0 the sun is 2.27° below the observer's horizon, so the edge of Earth's shadow passes 5 km above the observer.
- The grazing ray (edge of Earth's shadow), parallel sun rays at 1 km intervals, the shadow itself, and the parts of each cloud base lit from below.
- The distance from the observer to the sunset point, where the grazing ray touches the Earth.

Frames run from t = −11 min to t = +4.5 min in 0.25 min steps.

## Controls

| Control | Effect |
|---|---|
| Play / Pause | Starts or stops the loop (250 ms per frame) |
| Slider | Steps to a single frame |
| Rate selector | Rate of solar descent: equator at equinox (15.0°/h), Basel at equinox (10.1°/h), Basel at solstice (8.2°/h) |

The readout below the controls gives the time, the sun's elevation at the observer, the height of the shadow edge above the observer, the distance to the sunset point and the state of each cloud base.

If your system is set to reduce motion, the animation starts paused.

## Model

Spherical Earth (R = 6371 km), no refraction, constant rate of solar descent. See [docs/geometry.md](docs/geometry.md) for the derivations, the reference tables and the model's limitations.

## Running locally

The page is a single self-contained HTML file with no dependencies or build step. Open `index.html` in a browser.

## Deployment

The site is served by GitHub Pages from the root of the `main` branch.

## Licence

MIT. See [LICENSE](LICENSE).
