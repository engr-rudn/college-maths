---
layout: default
---

# 7-5 Applications of Integrals

## Learning Targets

You will be able to
- [ ] Convert between work and force and back again
- [ ] Be able to utilize both metric and imperial units
- [ ] Find the work done by a variable force
- [ ] Apply your knowledge of integrals to problems involving pumping fluids

## Concepts / Definitions

**Mass** is a property of an object. This property happens to be a measurement of its _resistance to acceleration_.

**Force** is an interaction between objects equivalent to _mass times acceleration_. In other words, $\vec{F} = m\vec{a}$.

### Work, Revisited

**Work** is the total amount of effort required to perform a task, equivalent to _force times displacement_. $W = \vec{F}*s = m\vec{a}*s$

#### The Metric System

Measurement | Label | Units
--|--|--
Mass    | Kilograms | $kg$
Force   | Newtons   | $kg * \frac{m}{sec^2}$
Work    | Joules    | $kg * \frac{m}{sec^2} * m$

#### Freedom Units

Measurement | Label | Units
--|--|--
Mass    | Slugs         | $32 * lb$
Force   | Pounds        | $lb$
Work    | Foot-Pounds   | $ft*lb$

Imperial units make no sense.

As far as comparisons go, a Newton is about a quarter of a pound $(1\ N = 0.225\ lbs)$. <br>
A foot-pound is about 1.36 Joules $(1\ ft\ lb = 1.36\ J)$.

### Work Done by a Force

If the force, $F(x)$, is not constant, then we can calculate the work over a tiny integral an infinite amount of times to get the total work.

#### Hooke's Law and the Spring Constant

Hooke's Law states that the force required to maintain a spring stretched $x$ units _beyond its natural length_ is proportional to $x$, provided $x$ is not too large.

$$F(x) = kx$$

### Work Done Lifting

Consider a stone block attached to the end of a heavy rope. How much work is done in pulling this block to the top of a building? <br>
This problem can be considered as two separate functions: the work done by pulling the stone block to the top, and the work done pulling the heavy rope up.

The stone block is straightforward - you need to exert force equal to its _weight_ throughout the interval.

$$w = \int_a^b (weight)(distance\ travelled)\ dx$$

The rope is a little more complicated.

$$w = \int_a^b \frac{weight\ of\ rope\ /\ unit}{distance\ travelled}\ dx$$

Put our two equations together, and we get **Work Done Lifting as an Integral**.

$$w = \int_a^b \frac{m_r\vec{a}}{b-a} + (m_s\vec{a})(b-a)\ dx = $$

Note that $b-a$ is both the length of the rope and the distance travelled. $m_r$ is the mass of the rope, and $m_s$ is the mass of the stone block.

### Work Done Pumping

In a typical pumping problem, you will encounter a tank, a distance needed to travel, and a weight of the fluid.

$$w = \int_a^b (density)\ v(x)\Delta x\ dx$$

Note that $r$ must be adapted for the proper
