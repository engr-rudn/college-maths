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
> > Since $$\sqrt{\alpha}(b-a)$$ is a finite number, it follows that $$\sqrt{f}$$ is integrable on $$[a,b]$$.\
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
> > $$F'(x) = f(x) = \frac{\sin x}{x}$$\
> > Integrating both sides with respect to $$x$$, we get:\
> > $$F(x) = \int \frac{\sin x}{x} dx + C$$\
> > where $$C$$ is a constant of integration.\
> > However, it can be shown that the integral\
> > $$\int \frac{\sin x}{x} dx$$ does not have an elementary antiderivative,\
> > i.e., an antiderivative that can be expressed in terms of elementary functions (such as polynomials, exponentials, logarithms, trigonometric functions, etc.).\
> > Therefore, the function $$F(x)$$ cannot be expressed in the given form for this choice of $$f(x)$$.
> > 
> {: .solution}
{: .challenge}

> ## 6.5.2 Exercise 3 - Give an example to show that Proposition 6.19 does not hold if the requirement that $$F$$ is continuous is omitted. 
> > ## Solution
> >
> > Let $$ f(x) = \begin{cases} 1 & \text{if } 0 \leq x \leq 1 \\ -1 & \text{if } 1 < x \leq 2 \end{cases} $$\
> >  be a piecewise continuous function on the interval $$[0, 2]$$.\
> >  Let $$F(x) = \begin{cases} x & \text{if } 0 \leq x \leq 1 \\ x-2 & \text{if } 1 < x \leq 2 \end{cases}$$\
> >  be a function that is continuous on $$[0,2]$$, differentiable everywhere except at $$x=1$$, and satisfies $$F'(x) = f(x)$$ for all $$x$$ except $$x=1$$.\
> > Note that $$\int_0^2 f(x)dx = \int_0^1 1 dx + \int_1^2 -1 dx = 0$$. However, we have:\
> > $$F(2) - F(0) = (2-2) - (0-0) = 0$$\
> > So, $$F$$ is a primitive of $$f$$ on $$[0,2]$$. However, $$F$$ is not differentiable at $$x=1$$, so the conclusion of the proposition fails if we do not require $$F$$ to be continuous.
> > 
> {: .solution}
{: .challenge}
> ## 7.3.1 Exercise 2 - For each natural number $$n$$ we define the function $$f_n(x) = (e^{x^2})\frac{d^n}{dx^n}(e^{-x^2})$$. 
> ### (a) Show that $$f_n$$ is a polynomial of degree $$n$$, and is moreover an even function when $$n$$ is even and an odd function when $$n$$ is odd 
> > ## Solution
> >
> > We have to show that $$f_n(x)$$ is a polynomial of degree $$n$$ multiplied by $$e^{x^2}$$\
> >  by using the derivative of $$e^{-x^2}$$ to write $$f_n(x)$$ in terms of a polynomial multiplied by $$e^{x^2}$$.\
> > Prove that $$f_n(x)$$ is even when $$n$$ is even and odd when $$n$$ is odd by using the behavior of the derivatives of $$e^{-x^2}$$ to show that $$f_n(x)$$ has the same parity as $$n$$ for all $$n$$. Specifically, they should show that:\
> > $$f_1(x)$$ is odd because the first derivative of $$e^{-x^2}$$ introduces a factor of $$-2x$$.\
> > $$f_2(x)$$ is even because the second derivative of $$e^{-x^2}$$ introduces a factor of $$4x^2-2$$.\
> > $$f_3(x)$$ is odd because the third derivative of $$e^{-x^2}$$ introduces a factor of $$-8x^3+12x$$.\
> > $$f_4(x)$$ is even because the fourth derivative of $$e^{-x^2}$$ introduces a factor of $$16x^4-48x^2+12$$.\
> > Generalize this pattern to all $$n$$ to show that $$f_n(x)$$ is even when $$n$$ is even and odd when $$n$$ is odd.\
> > More explanation of the solution follows:\
> > For each natural number $$n$$, we define the function $$f_n(x) = (e^{x^2})\frac{d^n}{dx^n}(e^{-x^2})$$.\
> > To show that $$f_n(x)$$ is a polynomial of degree $$n$$, we can find the first few derivatives of $$e^{-x^2}$$ and notice that each derivative introduces a polynomial of degree $$n$$ in $$x$$ multiplied by $$e^{-x^2}$$. Thus, $$f_n(x)$$ is a polynomial of degree $$n$$ multiplied by $$e^{x^2}$$.\
> > To show that $$f_n(x)$$ is even when $$n$$ is even and odd when $$n$$ is odd, we can look at the behavior of each derivative of $$e^{-x^2}$$.\
> >  The first derivative introduces a factor of $$-2x$$, which means that $$f_1(x)$$ is an odd function.\
> > The second derivative introduces a factor of $$4x^2-2$$, which means that $$f_2(x)$$ is an even function.\
> > The third derivative introduces a factor of $$-8x^3+12x$$, which means that $$f_3(x)$$ is an odd function.\
> > The fourth derivative introduces a factor of $$16x^4-48x^2+12$$, which means that $$f_4(x)$$ is an even function.\
> > We can see that this pattern continues for all $$n$$.\
> >  When $$n$$ is even, $$f_n(x)$$ is an even function because all of the derivatives up to the $$n$$th introduce even powers of $$x$$.\
> > When $$n$$ is odd, $$f_n(x)$$ is an odd function because all of the derivatives up to the $$n$$th introduce odd powers of $$x$$.
> > 
> {: .solution}
{: .challenge}
> ### (b) show that $$f_{n+1}(x) = f'n(x) - 2xf_n(x)$$ for $$n=0,1,2,\ldots$$ 
> > ## Solution
> >
> > To show that $$f_{n+1}(x) = f'n(x) - 2xf_n(x)$$ for $$n=0,1,2,\ldots$$, we can begin by writing out the definitions of $$f{n+1}(x)$$ and $$f_n(x)$$:\
> > $$f_{n+1}(x) = (e^{x^2})\frac{d^{n+1}}{dx^{n+1}}(e^{-x^2})$$\
> > $$f_n(x) = (e^{x^2})\frac{d^n}{dx^n}(e^{-x^2})$$\
> > We can then use the product rule for differentiation to find $$f'_n(x)$$:\
> > $$f'_n(x) = \frac{d}{dx}\left((e^{x^2})\frac{d^n}{dx^n}(e^{-x^2})\right)$$\
> > Using the product rule again, we can simplify this expression:\
> > $$f'_n(x) = (e^{x^2})\frac{d}{dx}\left(\frac{d^n}{dx^n}(e^{-x^2})\right) + \frac{d}{dx}(e^{x^2})\frac{d^n}{dx^n}(e^{-x^2})$$\
> > Notice that the first term in this expression is $$f_{n+1}(x)$$, so we can rewrite the equation as:\
> > $$f_{n+1}(x) = f'_n(x) - 2xe^{x^2}\frac{d^n}{dx^n}(e^{-x^2})$$\
Using the definition of $$f_n(x)$$, we can simplify the second term:\
> > $$f_{n+1}(x) = f'_n(x) - 2xf_n(x)$$\
> > Thus, we have shown that $$f_{n+1}(x) = f'_n(x) - 2xf_n(x)$$ for $$n=0,1,2,\ldots$$.
> > 
> {: .solution}
{: .challenge}
> ### (c) show that $$f_n(x)$$ has $$n$$ distinct real roots 
> > ## Solution
> >
> > To show that $$f_n(x)$$ has $$n$$ distinct real roots, we can begin by using the definition of $$f_n(x)$$:\
> > $$f_n(x) = (e^{x^2})\frac{d^n}{dx^n}(e^{-x^2})$$\
> > Notice that $$e^{-x^2}$$ is an even function, so its $$n$$th derivative is also an even function when $$n$$ is even and an odd function when $$n$$ is odd. Therefore, we only need to consider the roots of\
> > $$\frac{d^n}{dx^n}(e^{-x^2})$$.
> > We can find the roots of $$\frac{d^n}{dx^n}(e^{-x^2})$$ by solving the equation\
> >  $$\frac{d^n}{dx^n}(e^{-x^2}) = 0$$.\
> > This can be simplified by taking the derivative of $$e^{-x^2}$$ using the chain rule:\
> > $$\frac{d}{dx}(e^{-x^2}) = -2xe^{-x^2}$$\
> > Using this, we can find the second derivative:\
> > $$\frac{d^2}{dx^2}(e^{-x^2}) = (4x^2-2)e^{-x^2}$$\
> > By inspection, we can see that this function has two roots:\
> > $$x=\pm\frac{1}{\sqrt{2}}$$.\
> > Using induction and the product rule, we can show that the $$n$$th derivative of $$e^{-x^2}$$ has $$n$$ distinct real roots, alternating between positive and negative values.\
> > Therefore, $$f_n(x)$$ has $$n$$ distinct real roots for $$n=0,1,2,\ldots$$
> > 
> {: .solution}
{: .challenge}
> ### (d) show that $$f_n(x)$$ satisfies the differential equation $$y''-2xy'+2ny=0$$ 
> > ## Solution
> >
> > To show that $$f_n(x)$$ satisfies the differential equation $$y''-2xy'+2ny=0$$,\
> > we can start by differentiating $$f_n(x)$$ with respect to $$x$$.\
> > Using the product rule and the chain rule, we get:\
> > $$f_n'(x) = d/dx((e^{x^2})d^n/dx^n(e^{-x^2}))$$\
> > $$f_n'(x) = (2xe^{x^2})d^n/dx^n(e^{-x^2})+(e^{x^2})d^{n+1}/dx^{n+1}(e^{-x^2})$$\
> > $$f_n'(x) = (2xe^{x^2})d^n/dx^n(e^{-x^2})-(2n+2)(e^{x^2})d^n/dx^n(e^{-x^2})$$\
> > $$f_n'(x) = (2x-2n-2)f_n(x)$$\
> > Next, we differentiate $$f_n'(x)$$ with respect to $$x$$ using the product rule and the chain rule:\
> > $$f_n''(x) = d/dx((2x-2n-2)f_n(x)) + (2x-2n-2)f_n'(x)$$\
> > $$f_n''(x) = 2f_n(x) + (2x-2n-2)(2x-2n)f_n(x)$$\
> > $$f_n''(x) = (4x^2-4nx-2)f_n(x)$$\
> > Substituting these expressions for $$f_n'(x)$$ and $$f_n''(x)$$ into the differential equation $$y''-2xy'+2ny=0$$, we get:\
> > $$(4x^2-4nx-2)f_n(x) - 2x(2x-2n-2)(2x-2n)f_n(x) + 2nf_n(x) = 0$$\
> > Simplifying, we get:\
> > $$f_n(x)(4x^2-4nx+2-4x^2+8nx-4n^2-4n) = 0$$\
Therefore, $$f_n(x)$$ satisfies the differential equation $$y''-2xy'+2ny=0$$.
> > 
> {: .solution}
{: .challenge}
> ## 8.1.2 Solve the following integrals:
> ## 1. Solve the following integrals:
> ### (a) $$\int(xe^x)dx$$
> > ## Solution
> >
> > To evaluate the integral $$\int (x e^x)dx$$, we will use integration by parts,\
> > which is a technique that involves breaking down the integral into two parts and applying a formula involving the product rule of differentiation.\
> > Let $$u = x$$ and $$dv = e^x dx$$. Then, we have $$du = dx$$ and $$v = \int e^x dx = e^x$$.\
> > Using the formula for integration by parts, we have:\
> > $$
\begin{align*}
\int (x e^x)dx &= \int u dv \\
&= u v - \int v du \\
&= x e^x - \int e^x dx \\
&= x e^x - e^x + C,
\end{align*}
$$\
> > where $$C$$ is the constant of integration. \
> > Therefore, the antiderivative of $$xe^x$$ is $$xe^x - e^x + C$$.
> > 
> {: .solution}
{: .challenge}
> ### (b) $$\int (x^2 \cos x)dx$$
> > ## Solution
> >
> > To integrate $$\int (x^2 \cos x)dx$$, we can use integration by parts,\
> >  which is a technique that involves breaking down the integral into two parts and applying a formula involving the product rule of differentiation.\
> > Let's assume $$u = x^2$$ and $$dv = \cos x dx$$.\
> > Then, $$du = 2x dx$$ and $$v = \int \cos x dx = \sin x$$.\
> > Applying the formula for integration by parts, we have:\
> > $$
\begin{align*}
\int (x^2 \cos x)dx &= \int u dv \\
&= u v - \int v du \\
&= x^2 \sin x - \int 2x \sin x dx \\
&= x^2 \sin x + 2 \int x (-\cos x) dx \\
&= x^2 \sin x - 2x \cos x + 2 \int \cos x dx \\
&= x^2 \sin x - 2x \cos x + 2 \sin x + C,
\end{align*}
$$\
> > where $$C$$ is the constant of integration.\
> > Therefore, the antiderivative of $$x^2 \cos x$$ is\
> > $$x^2 \sin x - 2x \cos x + 2 \sin x + C$$.
> > 
> {: .solution}
{: .challenge}
> ### (c) $$\int e^x \cos x dx$$
> > ## Solution
> >
> > To integrate $$\int (x^2 \cos x)dx$$, we can use integration by parts, which is a technique that involves breaking down the integral into two parts and applying a formula involving the product rule of differentiation.\
> > Let's assume $$u = x^2$$ and $$dv = \cos x dx$$. Then,\
> >  $$du = 2x dx$$ and $$v = \int \cos x dx = \sin x$$.\
> > Applying the formula for integration by parts, we have:
> > $$
\begin{align*}
\int (x^2 \cos x)dx &= \int u dv \\
&= u v - \int v du \\
&= x^2 \sin x - \int 2x \sin x dx \\
&= x^2 \sin x + 2 \int x (-\cos x) dx \\
&= x^2 \sin x - 2x \cos x + 2 \int \cos x dx \\
&= x^2 \sin x - 2x \cos x + 2 \sin x + C,
\end{align*}
$$\
> > where $$C$$ is the constant of integration.\
> > Therefore, the antiderivative of $$x^2 \cos x$$ is $$x^2 \sin x - 2x \cos x + 2 \sin x + C$$.
> > 
> {: .solution}
{: .challenge}
> ### (c) $$\int e^x \cos x dx$$
> > ## Solution
> >
> > To evaluate the integral $$\int e^x \cos x dx$$, we can use integration by parts twice and solve for the integral.\
> > Let's assume $$u = \cos x$$ and $$dv = e^x dx$$. Then,\
> > $$du = -\sin x dx$$ and $$v = \int e^x dx = e^x$$.\
> > Applying the formula for integration by parts, we have:\
> > $$
\begin{align*}
\int e^x \cos x dx &= \int u dv \\
&= u v - \int v du \\
&= \cos x e^x + \int e^x \sin x dx \\
&= \cos x e^x - \int \sin x d(e^x) \\
&= \cos x e^x - e^x \sin x + \int e^x \cos x dx \\
&= \cos x e^x - e^x \sin x + I,
\end{align*}
$$\
> > where $$I = \int e^x \cos x dx$$.\
> > Now, let's assume $$u = \sin x$$ and $$dv = e^x dx$$. Then,\
> >  $$du = \cos x dx$$ and $$v = \int e^x dx = e^x$$.\
> > Applying the formula for integration by parts again, we have:\
> >$$
 \begin{align*}
I &= \int e^x \cos x dx \\
&= \int u dv \\
&= u v - \int v du \\
&= \sin x e^x - \int e^x \cos x dx \\
&= \sin x e^x - I.
\end{align*}
$$\
> > Solving for $$I$$ by adding $$I$$ to both sides, we get:\
> > $$
\begin{align*}
2I &= \cos x e^x - e^x \sin x + \sin x e^x \\
&= e^x (\cos x + \sin x) \\
\Rightarrow I &= \frac{1}{2} e^x (\cos x + \sin x) + C,
\end{align*}
$$\
> > where $$C$$ is the constant of integration.\
> > Therefore, the antiderivative of $$e^x \cos x$$ is\
> >  $$\frac{1}{2} e^x (\cos x + \sin x) + C$$.
> > 
> {: .solution}
{: .challenge}
> ### (e) $$\int \ln x dx$$
> > ## Solution
> >
> > To evaluate the integral $$\int \ln x dx$$, we can use integration by parts, which is a technique that involves breaking down the integral into two parts and applying a formula involving the product rule of differentiation.\
> > Let's assume $$u = \ln x$$ and $$dv = dx$$. \
> > Then, $$du = \frac{1}{x} dx$$ and $$v = \int dx = x$$. \
> > Applying the formula for integration by parts, we have:\
> > $$
\begin{align*}
\int \ln x dx &= \int u dv \\
&= u v - \int v du \\
&= x \ln x - \int x \frac{1}{x} dx \\
&= x \ln x - x + C,
\end{align*}
$$\
> > where $$C$$ is the constant of integration.\
> > Therefore, the antiderivative of $$\ln x$$ is\
> > $$x \ln x - x + C$$.
> > 
> {: .solution}
{: .challenge}
> ## 2. Solve the following useful integrals, where $$a$$ is a positive constant:
> ### (a) $$\int \frac{1}{\sqrt{a^2 - x^2}} dx$$
> > ## Solution
> >
> > To evaluate the integral $$\int \frac{1}{\sqrt{a^2 - x^2}} dx$$, where\
> > $$-a < x < a$$, we can use the substitution\
> > $$x = a \sin \theta$$, which gives us\
> > $$dx = a \cos \theta d\theta$$ and $$\sqrt{a^2 - x^2} = a \cos \theta$$. 
> > Thus, we have:\
> > $$
\begin{align*}
\int \frac{1}{\sqrt{a^2 - x^2}} dx &= \int \frac{1}{a \cos \theta} a \cos \theta d\theta \\
&= \int d\theta \\
&= \theta + C \\
&= \sin^{-1} \left( \frac{x}{a} \right) + C,
\end{align*}
$$\
> > where $$C$$ is the constant of integration.\
> > Since $$-a < x < a$$, we have  $$-\frac{\pi}{2} < \theta < \frac{\pi}{2}$$, so \
> >  $$\sin^{-1} \left( \frac{x}{a} \right)$$ is a valid antiderivative within the given range of $$x$$.\
> > Therefore, the antiderivative of $$\frac{1}{\sqrt{a^2 - x^2}}$$ is $$\sin^{-1} \left( \frac{x}{a} \right) + C$$.
> > 
> {: .solution}
{: .challenge}
> ### (b) $$\int \frac{1}{\sqrt{a^2+x^2}} dx$$
> > ## Solution
> >
> > This integral can be solved by using a trigonometric substitution.\
> > Let's substitute $$x = a\tan\theta$$:\
> > $$
\begin{align*}
x &= a\tan\theta \\
dx &= a\sec^2\theta d\theta \\
\sqrt{a^2+x^2} &= \sqrt{a^2+a^2\tan^2\theta} \\
&= \sqrt{a^2\sec^2\theta} \\
&= a\sec\theta
\end{align*}
$$\
> >
> > Substituting these expressions in the integral gives:
> > $$
\begin{align*}
\int \frac{1}{\sqrt{a^2+x^2}} dx &= \int \frac{1}{a\sec\theta} a\sec^2\theta d\theta \\
&= \int \cos\theta d\theta \\
&= \sin\theta + C \\
&= \frac{x}{\sqrt{a^2+x^2}} + C
\end{align*}
$$\
> > 
> {: .solution}
{: .challenge}
> ### (d) $$\int \frac{1}{a^2 + x^2} dx$$
> > ## Solution
> >
> > To evaluate the integral $$\int \frac{1}{a^2 + x^2} dx$$, we can use the substitution $$x = a \tan t$$.\
> > Then, $$dx = a \sec^2 t dt$$ and $$a^2 + x^2 = a^2(1 + \tan^2 t) = a^2 \sec^2 t$$.\
> > Substituting these into the integral, we get:\
> > $$
\begin{align*}
\int \frac{1}{a^2 + x^2} dx &= \int \frac{1}{a^2 + a^2 \tan^2 t} a \sec^2 t dt \\
&= \int \frac{1}{a^2 \sec^2 t} a \sec^2 t dt \\
&= \int \frac{1}{a^2} dt \\
&= \frac{1}{a} \tan^{-1} \left( \frac{x}{a} \right) + C,
\end{align*}
$$\
> > where $$C$$ is the constant of integration.\
> > Therefore, the antiderivative of $$\frac{1}{a^2 + x^2}$$ is\
> > $$\frac{1}{a} \tan^{-1} \left( \frac{x}{a} \right) + C$$.
> > 
> {: .solution}
{: .challenge}
> ## 5. Solve the following integrals:
> ### (a) $$\int \sin^2 x dx$$
> > ## Solution
> >
> > To evaluate the integral $$\int \sin^2 x dx$$, we can use the trigonometric identity\
> >  $$\sin^2 x = \frac{1}{2}(1 - \cos 2x)$$ and simplify the integral.\
> > $$
\begin{align*}
\int \sin^2 x dx &= \int \frac{1}{2}(1 - \cos 2x) dx \\
&= \frac{1}{2} \int (1 - \cos 2x) dx \\
&= \frac{1}{2} \left(x - \frac{1}{2} \sin 2x \right) + C,
\end{align*}
$$\
> > where $$C$$ is the constant of integration.\
> > Therefore, the antiderivative of $$\sin^2 x$$ is\
> >  $$\frac{1}{2} \left(x - \frac{1}{2} \sin 2x \right) + C$$.
> > 
> {: .solution}
{: .challenge}
> ### (a) $$\int \sin^2 x dx$$
> > ## Solution
> >
> > To evaluate the integral $$\int \sin^2 x dx$$, we can use the trigonometric identity\
> >  $$\sin^2 x = \frac{1}{2}(1 - \cos 2x)$$ and simplify the integral.\
> > $$
\begin{align*}
\int \sin^2 x dx &= \int \frac{1}{2}(1 - \cos 2x) dx \\
&= \frac{1}{2} \int (1 - \cos 2x) dx \\
&= \frac{1}{2} \left(x - \frac{1}{2} \sin 2x \right) + C,
\end{align*}
$$\
> > where $$C$$ is the constant of integration.\
> > Therefore, the antiderivative of $$\sin^2 x$$ is\
> >  $$\frac{1}{2} \left(x - \frac{1}{2} \sin 2x \right) + C$$.
> > 
> {: .solution}
{: .challenge}
> ### (a) $$\int \sin^2 x dx$$
> > ## Solution
> >
> > To evaluate the integral $$\int \sin^2 x dx$$, we can use the trigonometric identity\
> >  $$\sin^2 x = \frac{1}{2}(1 - \cos 2x)$$ and simplify the integral.\
> > $$
\begin{align*}
\int \sin^2 x dx &= \int \frac{1}{2}(1 - \cos 2x) dx \\
&= \frac{1}{2} \int (1 - \cos 2x) dx \\
&= \frac{1}{2} \left(x - \frac{1}{2} \sin 2x \right) + C,
\end{align*}
$$\
> > where $$C$$ is the constant of integration.\
> > Therefore, the antiderivative of $$\sin^2 x$$ is\
> >  $$\frac{1}{2} \left(x - \frac{1}{2} \sin 2x \right) + C$$.
> > 
> {: .solution}
{: .challenge}
> ### (b) $$\int \cos^2 x \cos^2 x dx$$
> > ## Solution
> >
> > To evaluate the integral $$\int \cos^2 x \cos^2 x dx$$, we can use the trigonometric identity\
> >  $$\cos^2 x = \frac{1}{2}(1 + \cos 2x)$$ and simplify the integral.\
> > $$
\begin{align*}
\int \cos^2 x \cos^2 x dx &= \int \cos^2 x \left( \frac{1}{2}(1 + \cos 2x) \right) dx \\
&= \frac{1}{2} \int (\cos^2 x + \cos^3 2x) dx \\
&= \frac{1}{2} \left( \int \cos^2 x dx + \int \cos^3 2x dx \right)
\end{align*}
$$\
> > To evaluate $\int \cos^2 x dx$, we can use the trigonometric identity\
> >  $$\cos^2 x = \frac{1}{2}(1 + \cos 2x)$$.
> > $$
\begin{align*}
\int \cos^2 x dx &= \int \frac{1}{2}(1 + \cos 2x) dx \
&= \frac{1}{2} \left( x + \frac{1}{2} \sin 2x \right) + C,
\end{align*}
$$\
> > where $$C$$ is the constant of integration.\
> > To evaluate $$\int \cos^3 2x dx$$, we can use the substitution $$u = 2x$$ and simplify the integral.\
> > $$
\begin{align*}
\int \cos^3 2x dx &= \frac{1}{2} \int \cos^3 u du \\
&= \frac{1}{2} \int \cos u \cos^2 u du \\
&= \frac{1}{2} \int \cos u (1 + \cos 2u) du \\
&= \frac{1}{2} \left( \int \cos u du + \int \cos u \cos 2u du \right) \\
&= \frac{1}{2} \left( \sin u + \frac{1}{3} \sin^3 u \right) + C \\
&= \frac{1}{2} \left( \sin 2x + \frac{1}{3} \sin^3 2x \right) + C,
\end{align*}
$$\
> > where $$C$$ is the constant of integration.\
> > Substituting these results back into the original integral, we get:
> > $$
\begin{align*}
\int \cos^2 x \cos^2 x dx &= \frac{1}{2} \left( \frac{1}{2} \left( x + \frac{1}{2} \sin 2x \right) + \frac{1}{2} \left( \sin 2x + \frac{1}{3} \sin^3 2x \right) \right) + C \
&= \frac{1}{4} x + \frac{1}{8} \sin 2x + \frac{1}{6} \sin^3 2x + C,
\end{align*}
$$\
> > where $$C$$ is the constant of integration.\
> > Therefore, the antiderivative of $$\cos^2 x \cos^2 x$$ is\
> >  $$\frac{1}{4} x + \frac{1}{8} \sin 2x + \frac{1}{6} \sin^3 2x + C$$.
> > 
> {: .solution}
{: .challenge}
> ### (c) $$\int \cos^3 x \cos^2 x dx$$
> > ## Solution
> >
> > To evaluate the integral $$\int \cos^3 x \cos^2 x dx$$, we can use the trigonometric identity\
> >  $$\cos^2 x = 1 - \sin^2 x$$ \
> > to express the integrand in terms of only $$\cos x$$.
> > $$
\begin{align*}
\int \cos^3 x \cos^2 x dx &= \int \cos^3 x (1 - \sin^2 x) dx \\
&= \int (\cos^3 x - \cos^3 x \sin^2 x) dx.
\end{align*}
$$\
> > To integrate $$\cos^3 x$$, we can use another trigonometric identity\
> >  $$\cos^3 x = \cos x (1 - \sin^2 x)$$. So, we have\
> > $$
\begin{align*}
\int \cos^3 x \cos^2 x dx &= \int (\cos x - \cos x \sin^2 x - \cos x \sin^2 x + \cos x \sin^4 x) dx \\
&= \int \cos x dx - 2\int \cos x \sin^2 x dx + \int \cos x \sin^4 x dx \\
&= \sin x - 2\int \cos x (1 - \cos^2 x) dx + \frac{1}{4} \int \cos x (3 - 4\sin^2 x) dx \\
&= \sin x - 2\int \cos x dx + 2\int \cos^3 x dx + \frac{3}{4} \int \cos x dx - \int \cos x \sin^2 x dx \\
&= \sin x - 2\sin x + 2\int \cos x (1 - \sin^2 x) dx + \frac{3}{4} \sin x - \frac{1}{2}\int (1 - \sin^2 x) d(\sin x) \\
&= -\sin x + \frac{3}{4} \sin x + \frac{1}{2} \int \sin^2 x d(\sin x) \\
&= -\frac{1}{4} \sin x + \frac{1}{6} \sin^3 x + C,
\end{align*}
$$\
> > where $$C$$ is the constant of integration.\
> > Therefore, the antiderivative of $$\cos^3 x \cos^2 x$$ is\
> >  $$-\frac{1}{4} \sin x + \frac{1}{6} \sin^3 x + C$$.
> > 
> {: .solution}
{: .challenge}
> ### (d) $$\int \sin^4 x , dx$$
> > ## Solution
> >
> > To find $$\int \sin^4 x , dx$$, we use the identity\
> >  $$\sin^2 x = 1 - \cos^2 x$$ to express $$\sin^4 x$$ as\
> >  a product of two powers of $$\sin x$$ and two powers of $$\cos x$$.\
> >  Thus, $$\sin^4 x = (\sin^2 x)^2 = (\sin^2 x)(1 - \cos^2 x) = \sin^2 x - \sin^2 x \cos^2 x$$.\
> >  Therefore, we have:\
> > $$
\begin{align*}
\int \sin^4 x , dx &= \int (\sin^2 x - \sin^2 x \cos^2 x) , dx \\
&= \int \sin^2 x , dx - \int \sin^2 x \cos^2 x , dx \\
&= \frac{1}{2} \int (1 - \cos 2x) , dx - \frac{1}{4} \int \sin^2 2x , dx \\
&= \frac{1}{2} \left(x - \frac{1}{2} \sin 2x \right) - \frac{1}{8} \int (1 - \cos 4x) , dx \\
&= \frac{1}{2} \left(x - \frac{1}{2} \sin 2x \right) - \frac{1}{8} \left(x - \frac{1}{4} \sin 4x \right) + C \\
&= \frac{3}{8} x - \frac{1}{4} \sin 2x - \frac{1}{32} \sin 4x + C,
\end{align*}
$$\
> > where $$C$$ is a constant of integration.
> > 
> {: .solution}
{: .challenge}