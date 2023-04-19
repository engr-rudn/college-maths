---
title:  Integration by Parts

questions:
- How do you evaluate integrals using parts"
objectives:
- "Use By Parts to evaluate integrals"
---

# Integration by Parts

## Concepts / Definitions

### Integration by Parts for Indefinite Integrals

If $$u$$ and $$v$$ are functions of $$x$$ and have continuous derivatives, then

$$\int udv = uv - \int vdu$$

$$\int f(x)g'(x)dx = f(x)g(x) = \int g(x)f'(x)dx$$

### Strategy

$$u = \ln x$$ as a first choice, then an algebraic type;
$$dv = $$ the functions where the derivative repeats ($$dv = $$ exponential or $$dv = $$ trig function)

As a general rule, when doing parts, $$\int udv$$ should be more complicated than $$\int vdu$$.

### Order

As we continue on when evaluating integrals

Order in which to calculate

- Try manipulating using algebra then just do it
- u-substitution
- Combination of Substitution and Algebra
- Integration by Parts
- Combination of any of the previous

## Examples

$$\int_0^1 \frac{2x + 1}{e^x} dx$$

$$\int e^{2x} \sin x dx$$

> ## 6.4.5 Exercise 1 - show that if $$f$$ and $$g$$ are bounded functions, both integrable on the interval [a,b], then so is $$fg$$. 
> > ## Solution
> >
> > To show that the product of two bounded and integrable functions is also integrable, we need to show that the product function $$fg$$ satisfies the conditions for integrability.\
> > First, since $$f$$ and $$g$$ are bounded functions, there exist real numbers $$M_1$$ and $$M_2$$ such that $$|f(x)| \leq M_1$$ and $$|g(x)| \leq M_2$$ for all $$x$$ in $$[a,b]$$.\
> > Then, we have:\
> > $$|fg(x)| = |f(x)g(x)| \leq |f(x)| |g(x)| \leq M_1 M_2$$\
> > This shows that $$fg$$ is also bounded, with $$|fg(x)| \leq M_1 M_2$$ for all $$x$$ in $$[a,b]$$.\
> > Next, we can use the Cauchy-Schwarz inequality to show that $$fg$$ is integrable.\
>> The Cauchy-Schwarz inequality states that for any integrable functions $$f$$ and $$g$$ on $$[a,b]$$,\
> > $$|\int_a^b f(x)g(x) dx| \leq \int_a^b |f(x)||g(x)| dx$$\
> > Since we know that $$|f(x)| \leq M_1$$ and $$|g(x)| \leq M_2$$ for all $$x$$ in $$[a,b]$$, we have:\
> > $$|\int_a^b f(x)g(x) dx| \leq \int_a^b |f(x)||g(x)| dx \leq M_1 M_2 (b-a)$$\
> > Since $$M_1 M_2$$ is a constant, this shows that $$fg$$ is integrable on $$[a,b]$$ with integral $$|\int_a^b fg(x) dx| \leq M_1 M_2 (b-a)$$.\
> > Therefore, we have shown that if $$f$$ and $$g$$ are bounded and integrable on $$[a,b]$$, then $$fg$$ is also integrable on $$[a,b]$$.
> > 
> {: .solution}
{: .challenge}

> ## 6.4.5 Exercise 2 - In the mean value theorem for integrals, it was assumed that the function g was non-negative. show, however, by means of an example, that the conclusion may not hold if g takes both positive and negative values. 
> 
> > ## Solution
> >
> > The Mean Value Theorem for Integrals states that if $$g(x)$$ is a non-negative continuous function on the interval $$[a,b]$$, then there exists a number $$c \in [a,b]$$ such that $$\int_a^b g(x)dx = g(c)(b-a)$$. If we relax the assumption that $$g(x)$$ is non-negative, the conclusion may not hold.\
> > Here is an example to illustrate this point. Consider the function $$g(x) = x - \frac{1}{2}$$ on the interval $$[0,1]$$.\ 
> > This function takes positive values on the interval $$(0, \frac{1}{2})$$, negative values on the interval $$(\frac{1}{2},1)$$, and has a zero at $$x=\frac{1}{2}$$.\
> > We can compute the definite integral of $$g(x)$$ on $$[0,1]$$ as follows:\
> > $$\int_0^1 g(x) dx = \int_0^{1/2} g(x) dx + \int_{1/2}^1 g(x) dx$$\
> > $$= \left[\frac{x^2}{2} - \frac{x}{2}\right]0^{1/2} + \left[\frac{x^2}{2} - \frac{x}{2}\right]{1/2}^1$$\
> > $$= \left(\frac{1}{8} - \frac{1}{4}\right) + \left(\frac{1}{2} - \frac{1}{2}\right)$$
> > $$= -\frac{1}{8}$$\
> > Note that $$g(x)$$ takes on the value $$g(\frac{1}{2}) = 0$$ at the midpoint of the interval $$[0,1]$$. However, we cannot apply the Mean Value Theorem for Integrals to conclude that there exists a point $$c \in [0,1]$$ such that $$g(c)(1-0) = -\frac{1}{8}$$, because $$g(x)$$ is not non-negative on the entire interval $$[0,1]$$. In fact, $$g(x)$$ takes on negative values on the interval $$[0,\frac{1}{2})$$ and positive values on the interval $$(\frac{1}{2},1]$$, so there is no point $$c$$ in $$[0,1]$$ where $$g(c) = \frac{-1}{8(1-0)} = -\frac{1}{8}$$. Therefore, the conclusion of the Mean Value Theorem for Integrals does not hold for this function when it takes both positive and negative values.
> > 
> {: .solution}
{: .challenge}
> ## 6.4.5 Exercise 4 - Suppose that $$f$$ is integrable on the interval $$[a, b]$$ and that there exists $$\alpha>0$$ such that $$f(x) > \alpha$$ for all $$x$$ in $$[a, b]$$. Show that $$\sqrt{f}$$ is integrable on $$[a, b]$$. Compare the oscillation of $$\sqrt{f}$$ on an interval with that of $$f$$. Hint: try using the identity $$\sqrt{x} - \sqrt{y} = \frac{x-y}{\sqrt{x} + \sqrt{y}}$$. 
> 
> > ## Solution
> >
> > To show that $$\sqrt{f}$$ is integrable on $$[a,b]$$, we need to show that $$\int_a^b \sqrt{f(x)} dx$$ exists and is finite.\
> > We can use the inequality $$\sqrt{f(x)} > \sqrt{\alpha}$$ for all $$x \in [a,b]$$ to obtain:\
> > $$\int_a^b \sqrt{f(x)} dx \geq \int_a^b \sqrt{\alpha} dx = \sqrt{\alpha} \int_a^b dx = \sqrt{\alpha}(b-a)$$\
> > Since $$\sqrt{\alpha}(b-a)$$ is a finite number, it follows that $$\sqrt{f}$$ is integrable on $$[a,b]$$.
> > To compare the oscillation of $$\sqrt{f}$$ on an interval with that of $$f$$, we can use the identity\
> > $$\sqrt{x} - \sqrt{y} = \frac{x-y}{\sqrt{x}+\sqrt{y}}$$ for $$x,y>0$$. \
> > Then, for any $$x,y \in [a,b]$$ with $$x \neq y$$, we have:\
> > $$\sqrt{f(x)} - \sqrt{f(y)} = \frac{f(x)-f(y)}{\sqrt{f(x)}+\sqrt{f(y)}} < \frac{f(x)-f(y)}{\sqrt{\alpha}+\sqrt{\alpha}} = \frac{1}{\sqrt{2\alpha}} |f(x)-f(y)|$$\
> > Thus, the oscillation of $$\sqrt{f}$$ on an interval is smaller than that of $$f$$ by a factor of $$\frac{1}{\sqrt{2\alpha}}$$.
> > 
> {: .solution}
{: .challenge}

> ## 6.5.2 Exercise 1 - Let $$f$$ be a continuous function on an open interval $$A$$. For every choice of $$a$$ in $$A$$, the function $$F(x) = \int_a^x f(t)dt$$ is an antiderivative for $$f$$. However, it is possible for $$f$$ to have antiderivatives that cannot be expressed in this form. Provide an example of such a function. 
> > ## Solution
> >
> > One example of a function that has antiderivatives that cannot be expressed in the form of the given integral is:\
> > $$f(x) = \frac{\sin x}{x}, \text{ where } x \neq 0 \text{ and } f(0) = 1$$\
> > To see that this function has antiderivatives that cannot be expressed in the given form, suppose that there exists a function $$F(x)$$ such that $$F'(x) = f(x)$$ for all $$x$$ in some open interval $$A$$. Then, we have:\
> > $$F'(x) = f(x) = \frac{\sin x}{x}$$
> > Integrating both sides with respect to $$x$$, we get:
> > $$F(x) = \int \frac{\sin x}{x} dx + C$$
> > where $$C$$ is a constant of integration.
> > However, it can be shown that the integral $$\int \frac{\sin x}{x} dx$$ does not have an elementary antiderivative, i.e., an antiderivative that can be expressed in terms of elementary functions (such as polynomials, exponentials, logarithms, trigonometric functions, etc.). Therefore, the function $$F(x)$$ cannot be expressed in the given form for this choice of $$f(x)$$.
> > 
> {: .solution}
{: .challenge}

> ## 6.5.2 Exercise 3 - Give an example to show that Proposition 6.19 does not hold if the requirement that $$F$$ is continuous is omitted. 
> > ## Solution
> >
> > Let $$f(x) = \begin{cases} 1 & \text{if } 0 \leq x \leq 1 \ -1 & \text{if } 1 < x \leq 2 \end{cases}$$\
> >  be a piecewise continuous function on the interval $$[0, 2]$$.\
> >  Let $$F(x) = \begin{cases} x & \text{if } 0 \leq x \leq 1 \ x-2 & \text{if } 1 < x \leq 2 \end{cases}$$\
> >  be a function that is continuous on $$[0,2]$$, differentiable everywhere except at $$x=1$$, and satisfies $$F'(x) = f(x)$$ for all $$x$$ except $$x=1$$.\
> > Note that $$\int_0^2 f(x) , dx = \int_0^1 1 , dx + \int_1^2 -1 , dx = 0$$. However, we have:\
> > $$F(2) - F(0) = (2-2) - (0-0) = 0$$\
> > So, $$F$$ is a primitive of $$f$$ on $$[0,2]$$. However, $$F$$ is not differentiable at $$x=1$$, so the conclusion of the proposition fails if we do not require $$F$$ to be continuous.
> > 
> {: .solution}
{: .challenge}