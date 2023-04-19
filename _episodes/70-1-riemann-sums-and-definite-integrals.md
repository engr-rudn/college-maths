---
title:  Riemann Sums and Definite Integrals

questions:
- "How to calculate integrals using area"
objectives:
- Write a Riemann sum or integral to calculate area
- Converting from Riemann form to integral form and vice versa
- Calculate integrals using area
---

# Riemann Sums and Definite Integrals

## Concepts / Definitions

### Riemann Sums

![Definition of a Riemann Sum](../assets/calculus/5-2-riemann-sums-and-definite-integrals_1.jpg)

![Example of a Riemann Sum](../assets/calculus/5-2-riemann-sums-and-definite-integrals_2.jpg)

Note: The area will be _net area_! Example:

![Net Area under the curve](../assets/calculus/5-2-riemann-sums-and-definite-integrals_3.jpg)

### Definition of the Definite Integral

If $$f$$ is defined on the closed interval $$[a, b]$$ and the limit of a Riemann sum of $$f$$ exists, then we say $$f$$ is integrable on $$[a, b]$$ and we denote the limit by

$$\lim_{\Delta x\to 0} \sum_{i=1}^{n}f(c_i)\Delta x_i = \int_a^b f(x)dx$$

The limit is called the _definite integral_ of $$f$$ from $$a$$ to $$b$$. The number $$a$$ is the _lower limit_ of integration, and the number $$b$$ is the _upper limit_ of integration.

$$\lim_{n\to\infty} \sum_{i=1}^n f(x_i)\Delta x$$

![Parts of the Definite Integral](../assets/calculus/5-2-riemann-sums-and-definite-integrals_4.png)

Note: The answer _must be a number_, e.g. your answer cannot be $$\int_a^b f(x)dx = \infty$$.
Additionally, this means that the variable of integration does not matter (and not $$a$$ or $$b$$.)

$$\int_a^b f(x)dx = \int_a^b f(t)dt = \int_a^b f(u)du$$

### Definitions

#### Displacement

$$Displacement\ = \int_a^b (velocity)\ dt$$

#### Distance

$$Distance\ = \int_a^b \lvert\ velocity\ \rvert\ dt$$

> ## 6.6.2 Exercise 1 - Compute the following limits by interpreting them as Riemann sums:
> > 
> > ## Solution
> >
> > To compute this limit by interpreting it as a Riemann sum, we can approximate the given sum by a definite integral.\
> > First, note that the sum can be written as:\
$$(1/n^2) * \sum_{k=1}^n k = (1/n^2) * (n(n+1))/2 = (n+1)/(2n)$$\
> > Now, we can interpret this sum as a Riemann sum for the function $$f(x) = x $$ over the interval $$[0,1]$$ by partitioning the interval into n equal subintervals, each of length $$1/n$$. We choose the sample points to be the right endpoints of each subinterval. Then, the Riemann sum is:\
> > $$\sum_{k=1}^n f(k/n) * (1/n) = \sum_{k=1}^n k/n^2$$\
which is exactly the sum we started with.\
> > Using this interpretation, we can approximate the sum as the area of rectangles with base length $$1/n$$ and height $$k/n$$.\ 
> > Then, the limit we are trying to compute is:\
$$lim_{n->\infinity} (n+1)/(2n) = 1/2$$\
> > Therefore, we have:\
> > $$lim_{n->\infinity} (1/n^2) * \sum_{k=1}^n k = 1/2$$
> > 
> {: .solution}
{: .challenge}