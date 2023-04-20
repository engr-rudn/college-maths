---
title:  Finding the Length of a Curve

questions:
- "How to find the length of a smooth curve?"
objectives:
- Find the length of a smooth curve
- Find the length of a segment of a smooth curve
---

# Finding the Length of a Curve

## Concepts / Definitions

### Deriving Arc Length

We want to determine the length of the continuous function $$f(x)$$ on the interval $$[a, b]$$.
This can be done by dividing the interval up into $$n$$ equal subintervals, each of width $$\Delta x$$.
Each point on the curve at each x-value can be denoted with $$P_i$$.
We can then approximate the curve by a series of straight lines connecting the points.

Here's a sketch of this situation.

![Arc Length](../assets/calculus/7-4_length-of-a-curve.gif)

The length of each segment is $$\lvert P_{i-1} P_i \rvert$$.

The length of the curve is approximately

$$L \approx \sum_{i=1}^9\ \lvert P_{i-1} P_i \rvert$$

Exact length would be

$$L = \lim_{n\to\infty} \sum_{i=1}^n \lvert P_{i-1} P_i \rvert$$

This exact length can be expressed as an integral.

### Definition of Arc Length


Given $$f(x)$$ is a _smooth curve_ (differentiable) on the interval $$[a, b]$$, the arc length of $$f$$ between $$a$$ and $$b$$ can be found by

$$Length = \int_a^b \sqrt{1+(f'(x))^2}\ dx$$

![Arc Length](../assets/calculus/7-4_quarter-circle.png)

The curve's length can be integrated in terms of $$x$$ or $$y$$.

$$ds = \sqrt{1+(\frac{dy}{dx})^2}\ dx = \sqrt{1+(\frac{dx}{dy})^2}\ dy$$

### Surface Area of a Solid of Revolution

Building off the previous lesson, we can apply this concept of arc length to find the surface area of a solid of revolution.

$$Surface\ Area = \int_a^b 2\pi f(x) \sqrt{1+f'(x)^2}\ dx$$

![Surface Area](../assets/calculus/7-4_surface-area.png)

Again, the surface area can be integrated in terms of $$x$$ or $$y$$, depending on the rotation axis.

$$dA = 2\pi\ f(x) \sqrt{1+(\frac{dy}{dx})^2} = 2\pi\ x\ \sqrt{1+(\frac{dx}{dy})^2}$$

When using the surface area formula, don't forget to add the area of the bottom and top bases, if necessary.

> ## 6.7.2 Exercise 1 - The upper unit semicircle is the curve $$y=\sqrt(1-x^2)$$ for $$-1< x < 1$$. Write the integral for the arc length from $$x = 0$$ to $$x = c$$, where $$0 < c < 1$$.
> > 
> > ## Solution
> >
> > The integral for the arc length from x = 0 to x=c, where 0 < c < 1 is:\
> > $$\int_{0}^{c} \sqrt{1 + \left(\frac{dy}{dx}\right)^2} dx$$\
> > where \frac{dy}{dx} is the derivative of the upper unit semicircle, given by:\
> > $$\frac{dy}{dx} = -\frac{x}{\sqrt{1-x^2}}$$\
> > Therefore, the integral becomes:\
> > $$\int_{0}^{c} \sqrt{1 + \left(\frac{dy}{dx}\right)^2} dx = \int_{0}^{c} \sqrt{1 + \frac{x^2}{1-x^2}} dx$$\
> > 
> {: .solution}
> ## 6.7.2 Exercise 2 - Compute the following limits by interpreting them as Riemann sums:
> ## (a) $$\lim_{n->\infty} (1/n^2) * \sum_{k=1}^n k$$
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
$$lim_{n->\infty} (n+1)/(2n) = 1/2$$\
> > Therefore, we have:\
> > $$lim_{n->\infty} (1/n^2) * \sum_{k=1}^n k = 1/2$$
> > 
> {: .solution}