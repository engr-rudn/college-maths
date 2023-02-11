---
layout: default
---

# Vectors in the Plane

## Learning Targets

You should be able to
- [ ] Write 2D vectors and find unit vectors and magnitudes
- [ ] Perform operations of vectors
- [ ] Solve applications including force and direction of objects

## Concepts / Definitions

A **two dimensional vector** is an ordered pair of real numbers, denoted in component form as $\vec{v} = \langle a, b\rangle$. The numbers $a$ and $b$ and the components. If an arrow has initial point $A(x_1, y_1)$ and terminal point $(x_2, y_2)$, it represents the vector in component form $\overrightarrow{AB} = \langle x_2 - x_1, y_2 - y_1 \rangle$

![Vector](../assets/precalculus/vectors-in-the-plane_1.png)
![Terminal Point](../assets/precalculus/vectors-in-the-plane_2.gif)

### Magnitude

The magnitude of $\vec{v}$ is the length of the arrow and the direction of $\vec{v}$ is the direction in which the arrow is pointing.

![Magnitude](../assets/precalculus/vectors-in-the-plane_3.png)

The **magnitude of vector** $\vec{v} = \langle v_1, v_2 \rangle$, represented by $\overrightarrow{AB}$ is
$$\lvert v\rvert = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2} = \sqrt{(v_1)^2 + (v_2)^2}$$

![Magnitude Graph](../assets/precalculus/vectors-in-the-plane_4.png)

### Unit Vector

The **unit vector** $\vec{u}$ is a vector with length $\lvert u\rvert = 1$.

$$\vec{u} = \frac{1}{\lvert v\rvert}\vec{v}$$

![Unit Vector](../assets/precalculus/vectors-in-the-plane_5.png)

### Linear combination of a vector ($\hat{\imath} \hat{\jmath}$ form)

Two component unit vectors are represented by ($\hat{\imath}$ hat and $\hat{\jmath}$ hat). $\hat{\imath} = \langle 1, 0 \rangle$ and $\hat{\jmath} = \langle 0, 1 \rangle$. The linear combination of a vector $\vec{v}$ is
$$\vec{v} = \langle a, b \rangle = ai + bj$$

![Linear Combination](../assets/precalculus/vectors-in-the-plane_6.png)

### Operations (answer is called resultant)

The sum or difference of vectors $\vec{a} \pm \vec{b}$ is $\vec{a} \pm \vec{b} = \langle a_1 \pm b_1, a_2 \pm b_2 \rangle$

![Operations](../assets/precalculus/vectors-in-the-plane_7.png)

The product of the scalar $k$ and the vector $\vec{v}$ is $k\vec{a} = \langle ka_1, ka_2 \rangle$

![Scalar](../assets/precalculus/vectors-in-the-plane_8.svg)

### Trigonometric form and direction angle of vectors

If $\vec{v}$ has direction angle $\theta$, the components of $\vec{v}$ can be computed $\vec{v} = \langle \lvert v\rvert\cos{\theta}, \lvert v\rvert\;\sin{\theta} \rangle$ and the unit vector in the direction of $\vec{v}$ is $\vec{u} = \langle \cos{\theta}, \sin{\theta} \rangle$

![Trigonometric Form](../assets/precalculus/vectors-in-the-plane_9.png)

### Application

Weight force, $F_{g}$ directly downward, can be calculated by multiplying the mass by the acceleration.

![Application](../assets/precalculus/vectors-in-the-plane_10.png)

SI units: $Newtons = kg * 9.8m/s^2$<br>
American units: $Pounds = slugs * 32ft/s^2$

## Exercises
no calc. unless specified
  1. Given $A=(2,-3)$ and $B(5,1)$,
     1. Find the component form of $\overrightarrow{AB}$
     2. Find the mangitude of $\overrightarrow{AB}$
     3. Find the unit vector of $\overrightarrow{AB}$
     4. Write $\overrightarrow{AB}$ as a linear combination.
     5. Find the direction of $\overrightarrow{AB}$ (calculator)
     6. Write $\overrightarrow{AB}$ in its trigonometric form
  2. If $\vec u = \langle4,-3\rangle,\vec v=\langle1,2\rangle$
     1. Find $\vec w=2\vec u-2\vec v$
     2. Write the linear combination of $\vec w$.
     3. Find $\lvert\vec w\rvert$
  3. Given the vector $\vec v$ below,
   ![Image](../assets/precalculus/vectors-in-the-plane_11.png)
     1. Write the exact component form.
     2. Write the exact linear combination form.
  4. For $\vec v = 7(\cos 135°\hat\imath + \sin135°\hat\jmath)$,
     1. Write in component form
     2. Find the magnitude of $\vec v$
  5. Find a vector $\vec v$ that has a magnitude of $\lvert\vec v\rvert = 3$ in the direction of $\langle-5,12\rangle$
  6. An airplane is flying on a compass bearning of 340° at 325 mph. A wind is blowing with the bearing of 320° at 40 mph.
     1. Find the component form for the velocity of the airplane and wind.
     2. Find the ground speed of the resultant.
     3. Find the new bearing of the plane.
  7. The minimum force required to hold up a box on a 20° frictionless inclined plane is 30lbs. What is the weight of the box?
  8. A force of 50lbs acts on an object at an angle of 45°. A second force of 75 lbs acts on the object at an angle of -30°. Find the magnitude of the resultant force and the direction.
