# Geometry notes

All quantities use a spherical Earth with radius **R = 6371 km**. Atmospheric refraction is ignored throughout.

## 1. Horizon dip

A point at height *h* above the surface sees the geometric horizon below its local horizontal by the dip angle

    δ = arccos(R / (R + h)) ≈ √(2h / R)

| h | δ |
|---|---|
| 2 km | ≈ 1.4° |
| 5 km | ≈ 2.27° |
| 6 km | ≈ 2.49° |
| 10 km | ≈ 3.2° |

A cloud base at height *h* can be lit from below while the sun is between 0° and δ below the base's local horizontal.

## 2. Grazing distance

The ray that just touches the Earth (the *grazing ray*) touches it at the *sunset point*. A point at height *h* on that ray lies at a surface distance

    d ≈ √(2Rh)

from the sunset point, for example d ≈ 252 km for h = 5 km. The central angle between the two local normals is d / R, which equals the dip angle.

## 3. Local horizontals

The local horizontal at the observer and the local horizontal at the cloud directly above are both perpendicular to the same normal, so they are **exactly parallel**, independent of scale or zoom. Clouds displaced along the surface by *x* have local horizontals tilted by *x* / R (0.26° for x = 29 km).

## 4. Shadow edge in the observer's frame

Let *e* be the sun's elevation at the observer (negative after sunset) and *s* = tan(−*e*). With the observer at the origin, *x* positive eastward and the surface approximated as y = −x² / 2R, the grazing ray is the line

    y = s·x + H,   H = s²R / 2

It touches the surface at the sunset point x_T = −sR and bounds Earth's shadow for x > x_T. *H* is the height of the shadow edge above the observer. In the animation t = 0 is the observer's sunset (e = 0, H = 0, sunset point at the observer), and e = −rate × t.

The parabolic approximation of the surface differs from the sphere by well under one pixel in the 68 km window.

## 5. When is a cloud base lit from below?

A point on a cloud base is lit from below if both of the following hold:

1. The sun is below that point's local horizontal (x > x_T).
2. The point lies above the shadow edge (y_base > s·x + H).

Because the shadow edge rises towards the east (away from the sun), the eastern end of a cloud base goes dark first.

## 6. Rate of solar descent

The sun's altitude near the horizon changes at

    dh/dt = 15°/h · cos φ · cos δ_sun · sin H_a

where φ is latitude, δ_sun the solar declination and H_a the hour angle at sunset (cos H_a = −tan φ · tan δ_sun).

| Case | Rate |
|---|---|
| Equator, equinox | 15.0°/h |
| Basel (47.5° N), equinox | ≈ 10.1°/h |
| Basel (47.5° N), either solstice | ≈ 8.2°/h |

The animation holds the rate constant over its window (15.5, 23.25 or 28.75 min for the three cases). The distance from the observer to the sunset point is R·|e| and therefore changes linearly with time: about 27.8, 18.8 and 15.2 km/min for the three cases.

## 7. Time between sunset points

The time for the Earth to rotate from the sunset point to the normal under the cloud is the dip angle divided by the rate of descent. For h = 5 km:

| Case | Time |
|---|---|
| Equator, equinox | ≈ 9.1 min |
| Basel, equinox | ≈ 13.4 min |
| Basel, solstice | ≈ 16.6 min |

Refraction (about 0.5° at the horizon) would lengthen these times by roughly 20%.

## 8. Model limitations

- No atmospheric refraction.
- Constant rate of solar descent over the animation window.
- Cloud size (10 km × 3 km) is illustrative.
- Cloud shadows are not modelled: rays pass behind clouds rather than being blocked.
- Terrain and distant clouds along the ray path are ignored; in reality they often block the lowest rays.
- The Basel rates are calculated, not checked against an ephemeris.
