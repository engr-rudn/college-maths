---
title: Algebra
questions:
- "What basic?"
- "How can ?"
- "How do ?"
- "Can I ?"
objectives:
- "???"
- "???"
---
# Algebra

* Field automorphisms. $$
\mathbb{Q}
$$ is algebraically rigid, no automorphisms. Any algebraic extension has lots of automorphisms. Add some trascendental and still automorphisms. But, $$
\mathbb{R}
$$ has NO non-trivial field automorphisms. However $$
\mathbb{C}
$$ does. Note that $$
\mathbb{R}
$$ is a mixture of algebraic and transcendental extensions of 
$$\mathbb{Q}
$$.

# Analysis

* Cantor sets. Crazy.

# Complex Dynamics

* Fractals, iterations, newtons method, and cool pictures.

# Linear Algebra

### Google page ranking

Suppose you have a very large stochastic matrix $$M$$. So large you can't decompose it, but you can multiply it against a vector easily. There is a theorem that says there is a one dimensional eigenspace with eigenvalue $$1$$ and the rest have eigenvalues $$
|\lambda_i|<1
$$. How do we find an eigenvector with eigenvalue $$1$$?

Idea: Guess! Pick a vector $$v$$ and write then consider $$M^nv$$. This can be written in a basis of eigenvectors and it will look like $$
\sum \lambda_i^nv_i
$$. Note that $$
\lambda_i^n \to 0
$$ for all except the one with norm $$1$$. So after a while this will be very close to our eigenvector with norm $$1$$.

# Geometry

### n-Balls

* generalize "volume" to $$n$$-dimensions.

* Can compute "volume" of $$n$$-ball, turns out $$5$$-dim is largest! ([link](http://en.wikipedia.org/wiki/Deriving_the_volume_of_an_n-ball))

### Dimension

##### Fractional Dimension

* Double a line, get double length, i.e. new length is $$2^1$$ times. Then $$1$$ dimensional

* Double a square get $$2^2$$ the area. So $$2$$ dimensional.

* Double a cube, get $$2^3$$ the volume. So $$3$$ dimensional.

* Double a Sierpinski triangle, get $$
3=2^{\log_2(3)}
$$ times the stuff. So $$
\log_2(3)\approx 1.58
$$ dimensional?

# Real Numbers

### 
$$
x^y=y^x
$$ with $$x<y$$

* The only integer solution with is $$
x=2, y=4
$$. Proof: calculus + guess and check.

* Question: is there rational solutions?

### Density of Rationals/Irrationals

* Question: Is there rational between every two real numbers?

* Easy from definition of reals by Cauchy Sequences?

* Easier/starting point: how about rational between 2 rationals. Solution: average is rational

### Archimedes Principle

* axiom: there is an $$
N\in\mathbb{N}
$$ bigger than any real number (or $$x$$ and $$x+1$$ both real numbers and integer in between), really the only assumption/axiom is the reals are what you think they are

* then $$1/N$$ is smaller then any real number

* Now take any two real numbers. Take their difference. Then find small rational in between. Now add integer multiples of that until it lies in between the original two real numbers. You have fit a rational in between.

* How about density of irrationals?

* first step: $$
\sqrt{2}
$$ is irrational. next step: rational linear combinations are irrational (just solve for root 2).

* Now write two reals. Take difference. divide by $$
\sqrt{2}
$$, get $$
(x_1-x_2)/\sqrt{2}>1/N \Rightarrow x_1-x_2 > \sqrt{2}/N
$$ then do same as before. Add integers, to get $$
x_1>\sqrt{2}/N+k>x_2
$$ which is rational linear combination of $$
\sqrt{2}
$$ which we showed was irrational. Done!

# Cardinality

### Infinity

* infinite number of primes

* definition same size as subset

* even numbers same size all numbers

### Hilbert's Hotel

* Countable is large

### Reals Are Large

* alphabet finite (countable) $$
\Rightarrow
$$ all language ever has or will be countable

* reals uncountable

* there's real numbers that will never have names ever never ever

# Infinite Sums

### Zeno's Paradox

* $$
\sum_{i\geq 1}\frac{1}{2^i} = 1
$$

###  $$\zeta$$

* $$
\zeta(2) = \frac{\pi^2}{6}$$

* $$
\zeta(-1) = -\frac{1}{12}
$$

# Logic

### Paradoxes

* Russel's paradox: Let $$
R = \{$$x$$ \midx\notin $$x$$\}
$$, then $$
R\in R \Leftrightarrow R\notin R
$$

### Puzzles

* prisoners and hats, etc.

TODO: examples?

# Curvature

* [Pizza](http://en.wikipedia.org/wiki/Theorema_Egregium)

* Curve it slightly and then it stays straight

* Curvature of plane is zero so curve along y means no curve along x

* Principal Curvature constantly 0

### Cylinders are Flat

* A 2d being living on a cylinder can't distuingish it from a plane

* spheres are not flat, we know we aren't living on a plane. every map will be distorted! It is impossible to have accurate maps, because maps are flat.

# Stats

### Estimating units

* [Tanks](http://en.wikipedia.org/wiki/German_tank_problem)

### Estimating Pi

* Buffon's needle/noodle

* Bouncing blocks: [link](http://math.stackexchange.com/questions/138289/intuitive-reasoning-behind-pis-appearance-in-bouncing-balls)

### Benfords Law

*  the number 1 is the leading digit 30% of the time

### Fermi Approximations

* Estimation from 0 knowledge, more convoluted more accurate

* Piano Tuners in Chicago:

* Cows eaten per year:

# Combinatorics

### Euler Characteristic

* $$
v-e+f = 2
$$ <-- for planar graphs

* works for polyhedra

* general version: counts holes (torus, etc)

* algebraic/topological invariant used to distinguish spaces

### Aztec Diamonds

* Random patterns/circle/things

### Dominoes

* Get grid. Take off two corners. Can cover with 2x1's? Soultion: no bcs color"

* Fibonacci

# Number Theory

### Probability

* Probability that an integer $$n$$ is square free is $$
\frac{6}{\pi^2}
$$ (see [mathworld](http://mathworld.wolfram.com/Squarefree.html)).

### Golden Ratio

* [Conway Solider](http://en.wikipedia.org/wiki/Conway's_Soldiers)

* Nice description, closed form, also shows up in pentagons/nature/etc

* Nice continued fraction

### Pi

* Everything.

* All finite strings of numbers appear in pi. Extrapolate using any encoding for arbitrary text.

### Riemann Zeta function

* Million dollar prize for hypothesis? [link](http://en.wikipedia.org/wiki/Riemann_hypothesis)

* Universal, similar to finite strings in pi in a way, but bigger. [link](http://en.wikipedia.org/wiki/Zeta_function_universality)