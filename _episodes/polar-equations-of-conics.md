---
layout: default
---

# Polar Equations of Conics

## Learning Targets

You should be able to
- [ ] Identify Conics
- [ ] Graph Conics from polar form
- [ ] Write polar to / from rectangular

## Concepts / Definitions

Any conic section can be defined as the locus of points whose distances to a point (the focus) and a line (the directrix) have a *constant ratio*. That ratio is the eccentricity, denoted as $e$.<br>
if $0 < e < 1$, the conic is an ellipse<br>
if $e = 1$, the conic is a parabola<br>
if $e > 1$, the conic is a hyperbola

![Conic Sections](../assets/precalculus/polar_equations_of_conics_1.png)

### Derivation

For any point $P(x, y)$ on the curve $D(x, y)$ on the directrix and $F(x, y)$ the focus at pole, the ratio of $PF/PD$ equals the eccentricity. $k$ is the distance between the focus and directrix.

$$e = \frac{PF}{PD} \Rightarrow PF = e * PD$$

![Derivation](../assets/precalculus/polar_equations_of_conics_2.jpg)

### Polar form of Conic Definition

The graph of a conic in polar form, with *focus at pole*, is given by
$$r = \frac{ek}{1 \pm e \cos{\theta}}\ or\ r = \frac{ek}{1 \pm e \sin{\theta}}$$
where $e$ = eccentricity, and $k$ is the distance between the focus and directrix.<br>
The directrix is perpendicular to the major axis, the axis of symmetry, and the transverse axis.

$$e = \frac{distance\ to\ focus}{distance\ to\ directrix} = \frac{PF}{PD} = \frac{c}{a}$$

$\cos{\theta}$ has polar axis symmetry and $\sin{\theta}$ has $\theta = \frac{\pi}{2}$ symmetry.

$r = \frac{ek}{1 + e\cos{\theta}}$ vertical directrix right of the pole<br>
$r = \frac{ek}{1 - e\cos{\theta}}$ vertical directrix left of the pole<br>
$r = \frac{ek}{1 + e\sin{\theta}}$ horizontal directrix above the pole<br>
$r = \frac{ek}{1 - e\sin{\theta}}$ horizontal directrix below the pole

### Examples
Given $r=\frac{16}{5-3\cos\theta}$, identify the conic, graph (including directrix), and write it in rectangular standard form.

## Exercises
  1. Find a polar equation for the conic with focus at the pole and eccentricity $e=7/3$ and directrix $y=-1$
  2. Determine the type of conic and graph. $r=\frac{24}{4+2\sin\theta}$
  3. Determine the type of conic and graph. $r=\frac{16}{3+5\cos\theta}$
  4. Determine the type of conic and graph. $r=\frac{2}{1-\cos\theta}$
  5. Determine the Cartesian equation (rectangular form) for the given conic. $r=\frac{4}{2-\sin\theta}$
  6. Determine the Cartesian equation (rectangular form) for the given conic. $r=\frac{6}{1+2\cos\theta}$
  7. Determine the Cartesian equation (rectangular form) for the given conic. $r=\frac{2}{1-\cos\theta}$
  8. Determine the Cartesian equation (rectangular form) for the given conic. $r=\frac{4}{2-2\cos\theta}$
  9. Write an equation for an ellipse in polar form with focus at pole and given the polar coordinates $(1.5,0),(6,\pi)$ that are on the major axis.
  10. Write an equation for a hyperbola in polar form with focus at pole and given the polar coordinates $(-6,\frac \pi 2),(2,\frac{3\pi}{2})$ as endpoints of its transverse axis.
  11. Write the following in polar form. $\frac{(x-4)^2}{25}+\frac{y^2}{9}=1$
