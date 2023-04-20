---
title:  Finding the Length of a Curve

questions:
- "How to find the length of a smooth curve?"
objectives:
- Find the length of a smooth curve
- Find the length of a segment of a smooth curve

keypoints:

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

> ## 6.7.2 Exercise 1 - The upper unit semicircle is the curve $$y=\sqrt{1-x^2}$$ for $$-1< x < 1$$. Write the integral for the arc length from $$x = 0$$ to $$x = c$$, where $$0 < c < 1$$.
> > 
> > ## Solution
> >
> > For the upper unit semicircle, we have $$y=\sqrt{1-x^2}$$, so $$\frac{dy}{dx}=-\frac{x}{\sqrt{1-x^2}}$$.\
> > Thus,the integral for the arc length from $$x = 0$$ to $$ x = c$$, where $$0 < c < 1$$ is:\
> > $$L = \int_{0}^{c} \sqrt{1 + \left(\frac{dy}{dx}\right)^2} dx$$\
> > where $$\frac{dy}{dx}$$ is the derivative of the upper unit semicircle, given by:\
> > $$\frac{dy}{dx} = -\frac{x}{\sqrt{1-x^2}}$$\
> > Therefore, the integral for the arc length of the upper unit semicircle from $$x=0$$ to $$x=c$$ is:\
> > $$L = \int_{0}^{c} \sqrt{1 + \left(\frac{dy}{dx}\right)^2} dx = \int_{0}^{c} \sqrt{1 + \frac{x^2}{1-x^2}} dx$$
> > 
> {: .solution}
{: .challenge}
> ## 6.7.2 Exercise 2 - The upper arc of the ellipse $$\frac{x^2}{a^2}+\frac{y^2}{b^2}=1$$, with semi-major axis $$a$$ and semi-minor axis $$b$$ is the curve $$y=\frac{b}{a}\sqrt{a^2-x^2}$$, $$-a< x < a$$. It is often convenient to express properties of the ellipse in terms of $$a$$, and the eccentricity $$e$$, defined as $$e=\sqrt{1-\frac{b^2}{a^2}}$$. Given $$c$$ such that $$0<c<a$$, express the integral for the arc length of the ellipse, from $$x=0$$ to $$x=c$$, in terms of $$a$$, $$e$$ and $$c$$.
> > 
> > ## Solution
> >
> > The upper arc of the ellipse $$\frac{x^2}{a^2}+\frac{y^2}{b^2}=1$$, with semi-major axis $$a$$ and semi-minor axis $$b$$ is the curve $$y=\frac{b}{a}\sqrt{a^2-x^2}$$, $$-a< x < a$$. It is often convenient to express properties of the ellipse in terms of $$a$$, and the eccentricity $$e$$, defined as $$e=\sqrt{1-\frac{b^2}{a^2}}$$.\
> > Given $$c$$ such that $$0<c<a$$, express the integral for the arc length of the ellipse, from $$x=0$$ to $$x=c$$, in terms of $$a$$, $$e$$ and $$c$$.\
> > The formula for the arc length of a curve given by $$y=f(x)$$ over the interval $$[a,b]$$ is:\
> > $$ L = \int_{a}^{b} \sqrt{1 + (f'(x))^2} \, dx $$\
> > For the ellipse, we have $$f(x) = \frac{b}{a}\sqrt{a^2-x^2}$$, so $$f'(x) = -\frac{bx}{a^2\sqrt{a^2-x^2}}$$. Therefore, the integral for the arc length from $$x=0$$ to $$x=c$$ is:\
> > $$ L = \int_{0}^{c} \sqrt{1 + \left(-\frac{bx}{a^2\sqrt{a^2-x^2}}\right)^2} \, dx $$\
> > Substituting the value of $$b$$ in terms of $$a$$ and $$e$$, we get:\
> > $$ L = \int_{0}^{c} \sqrt{1 + \left(-\frac{cx}{a^2\sqrt{a^2-x^2}\sqrt{1-e^2}}\right)^2} \, dx $$\
> > Simplifying the expression inside the square root, we get:\
> > $$ L = \int_{0}^{c} \sqrt{1 + \frac{c^2x^2}{a^4(1-\frac{x^2}{a^2})(1-e^2)}} \, dx $$\
> > We can then simplify the denominator as follows:\
> > $$ L = \int_{0}^{c} \sqrt{1 + \frac{c^2}{a^2} \cdot \frac{x^2}{a^2-x^2} \cdot \frac{1}{1-e^2}} \, dx $$\
> > Next, we use the substitution $$x = a\sin\theta$$ to obtain:\
> > $$ L = \int_{0}^{\arcsin(c/a)} \sqrt{1 - e^2\sin^2\theta} \, d\theta $$\
> > This is the formula for the arc length of the ellipse from $$x=0$$ to $$x=c$$, expressed in terms of $$a$$, $$e$$, and $$c$$.
> {: .solution}
{: .challenge}