---
layout: default
---

# Dot Product of Vectors in the Plane

## Learning Targets:

You should be able to
- [ ] Find dot products of vectors
- [ ] Find angles between vectors
- [ ] Find work by application

## Concepts / Definitions

### Definition of Dot Product

The **dot product** of $\vec{u} = \langle u_1, u_2 \rangle$ and $\vec{v} = \langle v_1, v_2 \rangle$ is
$$\vec{u} \bullet \vec{v} = u_1 v_1 + u_2 v_2 \qquad \vec{u} \bullet \vec{v} = \lvert\vec{u}\rvert \lvert\vec{v}\rvert \cos{\theta}$$

where $\theta$ is the angle between those vectors.

![Dot Product Definition](../assets/precalculus/dot-product-of-vectors-in-the-plane_1.gif)
![Dot Product Rotation](../assets/precalculus/dot-product-of-vectors-in-the-plane_2.png)

The dot product is the magnitude amount of stretching / shrinking one vector by another vector, in the same direction of the one vector.

### Orthogonal Vectors

The vectors $\vec{u}$ and $\vec{v}$ are **orthogonal** iff $\vec{u} \bullet \vec{v} = 0$.<br>
The dot product formula, in terms of the angle, is
$$\cos{\theta} = \frac{\vec{u} \bullet \vec{v}}{\lvert u\rvert\lvert v\rvert}$$

![Orthogonal Vectors](../assets/precalculus/dot-product-of-vectors-in-the-plane_3.png)

<!--Note: replace Note: with PRO TIP-->

Note: Orthogonal and perpendicular are *not exactly* the same. The zero vector is orthogonal to every vector, but not perpendicular to any vector.

### Projection of Vectors

The projection of vector $\vec{u}$ onto vector $\vec{v}$ is
$$proj_{v}u = (\frac{\vec{u} \bullet \vec{v}}{\lvert\vec{v}\rvert^2}) \vec{v} \qquad proj_vu = (\frac{\lvert\vec{u}\rvert \lvert\vec{v}\rvert \cos{\theta}}{\lvert\vec{v}\rvert^2}) \vec{v}$$

![Projection of Vectors](../assets/precalculus/dot-product-of-vectors-in-the-plane_4.png)

Vector $\vec{u}$ as a sum of two orthogonal vectors.
$$\vec{u} = proj_vu + \vec{s},\ \therefore \vec{s} = \vec{u} - proj_vu$$

### Application

If $\vec{F}$ is a constant force whose direction is the same as the direction of $\overrightarrow{AB}$, then the work $W$ done by $\vec{F}$ in moving an object from $A$ to $B$ is
$$W = \lvert\vec{F}\rvert \lvert\overrightarrow{AB}\rvert$$

![Application](../assets/precalculus/dot-product-of-vectors-in-the-plane_5.png)

$$W = \lvert F\rvert d\cos{\theta}$$
