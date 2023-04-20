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
> > The integral for the arc length from $$x = 0$$ to $$ x = c$$, where $$0 < c < 1$$ is:\
> > $$\int_{0}^{c} \sqrt{1 + \left(\frac{dy}{dx}\right)^2} dx$$\
> > where $$\frac{dy}{dx}$$ is the derivative of the upper unit semicircle, given by:\
> > $$\frac{dy}{dx} = -\frac{x}{\sqrt{1-x^2}}$$\
> > Therefore, the integral becomes:\
> > $$\int_{0}^{c} \sqrt{1 + \left(\frac{dy}{dx}\right)^2} dx = \int_{0}^{c} \sqrt{1 + \frac{x^2}{1-x^2}} dx$$\
> > 
> {: .solution}
> ## 6.7.2 Exercise 2 - The upper arc of the ellipse $$\frac{x^2}{a^2}+\frac{y^2}{b^2}=1$$, with semi-major axis $$a$$ and semi-minor axis $$b$$ is the curve $$y=\frac{b}{a}\sqrt{a^2-x^2}$$, $$-a< x < a$$. It is often convenient to express properties of the ellipse in terms of $$a$$, and the eccentricity $$e$$, defined as $$e=\sqrt{1-\frac{b^2}{a^2}}$$. Given $$c$$ such that $$0<c<a$$, express the integral for the arc length of the ellipse, from $$x=0$$ to $$x=c$$, in terms of $$a$$, $$e$$ and $$c$$.
> > 
> > ## Solution
> >
> > The arc length formula for a curve $$y=f(x)$$ over the interval $$[a,b]$$ is given by:\
> > $$L = ∫[a,b] √(1+(f'(x))^2) dx$$\
> > For the upper arc of the ellipse, we have $$f(x)=(b/a)\sqrt{a^2-x^2}$ and $f'(x)=-(b/a^2)x/\sqrt{a^2-x^2}$$, so $$(f'(x))^2 = (a^2/(4b^2))x^2/(a^2-x^2)$$ Hence,\
> > $$1+(f'(x))^2 = a^2/(a^2-x^2)$$\
> > The integral for the arc length of the ellipse from $$x = 0$$ to $$x=c$$ is therefore\
> > $$L = ∫[0,c] √(a^2/(a^2-x^2)) dx$$\
> > To simplify this integral, we use the substitution $$x=ac\sin\theta$$, so $$dx = ac\cos\theta\ d\theta$$ and\
> > $$L = ∫[0,sin^-1(c/a)] a√(1-e^2 sin^2θ) dθ$$\
> > Using the substitution $$u=\sin\theta$$, we get\
> > $$L = a ∫[0,c/a] √(1-e^2 u^2)/(1-u^2) du$$\
> > This last integral is an elliptic integral of the second kind, denoted by $$E(\phi,e)$$, where $$\phi=\sin^{-1}(c/a)$$, so the arc length is given by\
> > $$L = a E(sin^-1(c/a), e)$$\
> > 
> {: .solution}