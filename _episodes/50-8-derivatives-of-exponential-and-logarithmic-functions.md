---
title:  Derivatives of Exponential and Logarithmic Functions

questions:
- "How do you find derivatives of exponential and logarithmic functions?"

objectives:
- "Solve simple exponential and log equations"
-  Solve non simple exponential functions
- "Derive rules for derivatives of exponential and logs"
- "Compute derivatives of problems that contain exponentials and logs"
---

## Concepts / Definitions

Follow the rules of SADME for one variable.

### Solving Exponential

$$b^x = a$$
$$\log_{b}{b^x} = \log_{b}{a}$$
$$x = \log_{b}{a}$$

### Solving Logarithmic

$$\log_{b}{x} = a$$
$$b^{\log_{b}{x}} = b^a$$
$$x = b^a$$

> ## Example
> Solve $$5 + 2 \ln (x-1) = 4$$
{: .challenge}

> ## Exercises
  1. Solve $$4^x-5=3$$.
  2. Solve $$\frac 12(6)^{x+3} - 1 = 17$$.
  3. Solve $$3^{x+4} + 2 = -7$$.
  4. Solve $$10^{2x-3} + 4 = 21$$ Exact and approximate answer using log button.
  5. Solve $$-5e^-x + 9 = 6$$ Exact and approximate answer using $$\ln$$ button.
  6. Solve $$\log_2 x = -1$$.
  7. Solve $$\log_5 \lvert 3x+1 \rvert = 2$$.
  8. Solve $$15 + 2\log_2 x = 31$$.
  9. Solve $$\log_6 (x-5) + 8 \leq 10$$.
  10. Solve $$1 - 2\ln x = -4$$.
  11. Solve $$\log_x 25 = 2$$.
  12. Solve $$\log_3 (5x-1) = \log_3 (x+7)$$.
  13. Are the following equations equivalent, and do they produce the same solutions? Explain. $$4\log x = 2$$ and $$\log x^4 = 2$$
{: .challenge}

# Solving Non Simple Exponential Functions

## Concepts / Definitions

### Strategies

Equating if two terms, combine using properties, or factoring.

Note: All answers should be evaluated, unless it is irrational.

> ## Examples
1) Algebraically solve $$e^{2x} - 7e^x = -12$$\
2) Algebraically solve $$\ln(x-2) + \ln(2x-3) = 2\ln x$$\
3) Algebraically solve $$\frac{2^x - 2^{-x}}{2} = 4$$
{: .challenge}

> # Exercises
> Solve the following algebraically. (Exact answer)
  1. $$\log_4x + \log_4(x-3) = 1$$.
  2. $$23^{2x} + 5e^x = 3$$.
  3. $$\frac{e^x+e^{-x}}{2} = 4$$.
  4. $$\ln(x-3) + \ln(x+4) - 3\ln2 = 0$$.
  5. $$2^{2x} + 2^{x+2} = 12$$.
  6. $$2\log(x+1) - 2\log6 < 0$$.
  7. $$\ln x + \ln (x+2) = 4$$.
  8. $$5^{x-2}=3^{3x+2}$$.
  9. $$x^2e^x-4x^2=0$$.
  10. $$\log_3(x-6) = \log_92x$$.
  11. $$\frac{62}{1+3e^{-0.3x}} = 2$$.
  12. $$\lvert\log_5x\rvert - \log_5 (2x+1) = 0$$.
  13. Use calculator to solve $$x + \log_3 x = 8$$
{: .challenge}

# Derivatives of Exponential and Logarithmic Functions

## Concepts / Definitions

### Figuring out the derivative of $$y = a^x$$

$$\frac{d}{dx}y = \lim_{h\to 0}\frac{a^{x+h}-a^x}{h}$$\

$$\frac{dy}{dx} = \lim_{h\to 0}\frac{a^xa^h-a^x}{h}$$\

$$\frac{dy}{dx} = \lim_{h\to 0}a^x\frac{a^h-1}{h}$$\

Notice that the limit does not depend on $$a^x$$.

What does $$\lim_{h\to 0}\frac{a^h-1}{h}$$ equal?

$$\lim_{h\to 0}\frac{a^h-1}{h} = ?$$\

If $$a=e$$, then...

#### Definitions with the number $$e$$
  1. $$e = \lim_{n\to \infty}(1+\frac{1}{n})^n$$.
  2. $$e$$ is the unique positive number for which $$\lim_{h\to 0}\frac{e^h -1}{h} = 1$$.
  3. $$e = \sum_{n=0}^{\infty}\frac{1}{n!}$$\

$$\frac{dy}{dx} = a^x \lim_{h\to 0}\frac{a^h-1}{h}$$\

The first part, $$a^x$$ does not depend on $$h$$, and we have some number, a derivative times $$a^x$$. The derivative of rate of change of $$a^x$$ is proportional to the function itself, $$ka^x$$. What is that number?

If $$a$$ is a number other than $$e$$, let $$f(a) = \frac{a^{0.001}-1}{0.001}$$

$$X$$ | $$Y_1$$
---|---
0 | -1000
1 | 0
2 | .69339
3 | 1.0992
4 | 1.3873
5 | 1.6107
6 | 1.7934

### Derivative of a exponential function

$$\frac{d}{dx}a^x = a^x\ln a$$\

$$\frac{d}{dx}e^x = e^x\ln e = e^x$$\

### Finding the derivative of a logarithmic function

$$\frac{d}{dx}f(x) = \frac{d}{dx}\ln x$$.

$$\frac{df}{dx} = \lim_{h\to 0}\frac{\ln(x+h) - \ln x}{h}$$.

$$\frac{df}{dx} = \lim_{h\to 0}\frac{\ln(\frac{x+h}{x})}{h}$$.

$$\frac{df}{dx} = \lim_{h\to 0}\frac{1}{h}\ln(1+\frac{h}{x})$$.

$$\frac{df}{dx} = \lim_{h\to 0}\frac{1}{kx}\ln(1+k),\ for\ k = \frac{h}{x}$$.

$$\frac{df}{dx} = \lim_{h\to 0}\frac{1}{x}\ln(1+k)^{1/k},\ for\ k = \frac{h}{x}$$.

$$\frac{df}{dx} = \lim_{h\to 0}\frac{1}{x}\ln(\lim_{k\to\infty}(1+\frac{1}{k})^k),\ for\ k = \frac{h}{x}$$.

$$\frac{df}{dx} = \lim_{h\to 0}\frac{1}{x}\ln e = \frac{1}{x}$$.

---

$$y = \log_ax,\ for\ y = f(x)$$\
$$a^y = x$$\
$$\frac{d}{dx}a^y = \frac{d}{dx}x$$\
$$a^y \ln a \frac{dy}{dx} = 1$$\
$$\frac{dy}{dx} = \frac{1}{a^y \ln a}$$\
$$\frac{dy}{dx} = \frac{1}{a^{\log_ax}\ln a}$$\
$$\frac{df}{dx} = {1}{x\ln a}$$

### Derivative of a logarithmic function

$$\frac{d}{dx}\log_a\lvert x \rvert = \frac{1}{x\ln a}$$\
$$\qquad$$ $$\frac{d}{dx}\log_ax = \frac{1}{x\ln a},\ for\ x > 0$$\
$$\frac{d}{dx}\ln\lvert x \rvert = \frac{1}{x\ln e} = \frac{1}{x}$$\
$$\qquad$$ 
$$\frac{d}{dx}\ln x = \frac{1}{x\ln e} = \frac{1}{x},\ for\ x > 0$$

### Differentiate $$x^{\sin x}$$

Let $$y = x^{\sin x}$$\

$$\ln y = ln x^{\sin x}$$\

$$\ln y = \sin x \ln x$$\

$$\frac{d}{dx}\ln y = \frac{d}{dx}(\sin x \ln x)$$\

$$\frac{1}{y}\frac{d}{dx}y = \frac{d}{dx}\sin x \ln x + \sin x \frac{d}{dx} \ln x$$\

$$\frac{1}{y}\frac{d}{dx}y = \cos x \ln x + \sin x \frac{1}{x}$$\

$$\frac{dy}{dx} = y(\cos x \ln x + \sin x \frac{1}{x})$$\

$$\frac{dy}{dx} = x^{\sin x}(\cos x \ln x + \sin x \frac{1}{x})$$\



> ## Challenge 1 - Find a formula for the derivative $$ \frac{d}{dx} \log_a(x)$$. 
> > ## Solution
> >
> > The formula for the derivative of log base a of x, denoted as $$ \log_a(x) $$, is:\
> > $$ \frac{d}{dx} \log_a(x) = \frac{1}{x \ln(a)} $$\
> > where $$ \ln(a)$$ is the natural logarithm of a. We can derive this formula using the chain rule of differentiation and the formula for the derivative of the natural logarithm:\
> > $$ \frac{d}{dx} \ln(x) = \frac{1}{x} $$\
> > Let $$ y = \log_a(x) $$. Then, we can rewrite this equation as:\
> > $$ \ln(a^y) = y \ln(a) $$\
> > Taking the derivative of both sides with respect to $$x$$, we get:\
> > $$ \frac{d}{dx} \ln(a^y) = \frac{d}{dx} (y \ln(a)) $$\
> > Using the chain rule, we have:\
> > $$ \frac{d}{dx} \ln(a^y) = \frac{d}{dy} \ln(a^y) \cdot \frac{dy}{dx} = \frac{1}{a^y} \cdot \frac{dy}{dx} $$\
> > $$ \frac{d}{dx} (y \ln(a)) = \ln(a) \cdot \frac{dy}{dx} $$\
> > Substituting these expressions back into the original equation, we get:\
> > $$ \frac{1}{a^y} \cdot \frac{dy}{dx} = \ln(a) \cdot \frac{dy}{dx} $$\
> > Solving for (dy/dx), we obtain:\
> > $$ \frac{dy}{dx} = \frac{1}{x \ln(a)} $$\
> > Substituting $$ y = \log_a(x) $$, we arrive at the desired formula:\
> > $$ \frac{d}{dx} \log_a(x) = \frac{1}{x\cdot\ln(a)} $$
> > 
> {: .solution}
{: .challenge}

> ## Challenge 2 - Calculate the following limits (including proofs that they exist):. 
> 
> > ## Solution
> >
> > We can use L'Hopital's rule to find the limit of this expression:\
> > $$\lim x->\pi \frac{\sin(mx)}{\sin(x)} = \lim x->\pi \frac{m*cos(mx)}{cos(x)}$$ [applying L'Hopital's rule]\
> > = m*cos(m*pi)/cos(pi) [since cos(pi) = -1 and cos(m*pi) = cos(pi) = -1 for odd values of m] = -m
> > Therefore, the limit of sin(mx)/sin(x) as x approaches pi is -m.
> > 
> {: .solution}
{: .challenge}
> ## 7.2.9 Exercises 2 - Find a formula for the derivative $$(\frac{d}{dx})\log_{a}(x)$$. 
> 
> > ## Solution
> >
> > The logarithm function $$\log_{a}(x)$$ is defined as the inverse function of the exponential function $$a^x$$, such that $$\log_{a}(a^x) = x$$ for all $$x$$.\
> > Using the chain rule, we can differentiate $$\log_{a}(x)$$ with respect to $$x$$ as follows:\
> > $$(\frac{d}{dx})\log_{a}(x) = (\frac{d}{dx})(\frac{\ln(x)}{(ln(a)}) = \frac{1}{\ln(a)}.(\frac{d}{dx}\ln(x))$$\
> > Since $$\ln(x)$$ is the natural logarithm of $$x$$ (i.e., the logarithm with base $$e$$), its derivative is simply $$1/x$$. Thus, we have:\
> > $$(\frac{d}{dx})\log_{a}(x) = \frac{1}{x\ln(a)}$$\
> > Therefore , the formula for the derivative of $$\log_{a}(x)$$ with respect to $$x$$ is $$\frac{1}{x\ln(a)}$$.
> > 
> {: .solution}
{: .challenge}
> ## 7.2.9 Exercises 7 - Calculate the following limits (including proofs that they exist):
>  (a) $$\lim_{x \to 0^+} x^x$$
> > ## Solution
> > To evaluate the limit $$\lim_{x \to 0^+} x^x$$, we first rewrote\
> >  $$x^x$$ as $$e^{x \ln x}$$\
> >  using the property $$a^b = e^{b \ln a}$$\
> >  for all positive real numbers $$a$$ and $$b$$.\ 
> > Then, we applied L'Hopital's rule to evaluate $$\lim_{x \to 0^+} x \ln x$$,\
> >  which resulted in $$0$$. Therefore, the original limit became\
> >  $$\lim_{x \to 0^+} e^{x \ln x}$$, which evaluates to\
> >  $$e^0 = 1$$. Hence, the limit of $x^x$ as $x$ approaches $0$ from the right is $1$.
> > 
> {: .solution}
{: .challenge}
>  (b) $$\lim_{x \to \pi/2} (\pi/2)(\cos^2 x)/(x-(\pi/2))^2$$
> > ## Solution
> > The limit $$\lim_{x \to \pi/2} (\pi/2)(\cos^2 x)/(x-(\pi/2))^2$$\
> >  was evaluated using L'Hopital's rule twice. First, we applied the rule to obtain\
> >  $$\lim_{x \to \pi/2} (-\cos x \sin x)/(x-\pi/2)$$.\
> >  Then, we applied the rule again to obtain $$\lim_{x \to \pi/2} (-\cos^2 x + \sin^2 x)/1$$,\
> >  which evaluates to $$-1$$. Therefore, the original limit evaluates to $$-1$$.
> > 
> {: .solution}
{: .challenge}
>  (c) $$\lim_{x \to \pi} \sin(mx)/\sin(x)$$
> > ## Solution
> > The limit $$\lim_{x \to \pi} \sin(mx)/\sin(x)$$ was evaluated using the property\
> > $$\sin a/\sin b = (\sin a/a)/( \sin b/b)$$ for $a,b \neq 0$.\
> > The expression was then rewritten as $$\lim_{x \to \pi} (mx/\sin(mx)) \cdot (\sin(mx)/(mx)) \cdot (x/\sin(x))$$.\
> > Since $$\lim_{x \to \pi} (mx/\sin(mx)) = 1$$ and $$\lim_{x \to \pi} (x/\sin(x)) = 1$$, 
> > the limit simplifies to \
> > $$\lim_{x \to \pi} \sin(mx)/(mx)$$.\
> > Finally, this expression evaluates to $$m$$ because $$\lim_{x \to \pi} \sin(mx)/(mx) = m$$.\ > > Therefore, the original limit evaluates to $$m$$, where $$m$$ is an integer.
> > 
> {: .solution}
{: .challenge}
>  (f) $$\lim_{x \to \infty} (x+1)^s - x^s)/(x^{s+1}(s+1))$$
> > ## Solution
> > The limit $$\lim_{x \to \infty} (x+1)^s - x^s)/(x^{s+1}(s+1))$$\
> >  was evaluated using L'Hopital's rule twice. After the first application of the rule, the expression was simplified to \
> > $$\lim_{x \to \infty} s[(x+1)^{s-1} - x^{s-1}]/[(s+1)x^s]$$.\
> >  After the second application of the rule, the expression was simplified to\
> >  $$\lim_{x \to \infty} s(s-1)(x+1)^{s-2}/[(s+1)x^{s-1}]$$.\
> >  Taking the limit as $$x$$ approaches infinity, we see that the expression converges to $$s/(s+1)$, since $(x+1)^{s-2}/x^{s-1} \to 0$$ as $$x \to \infty$$.\
> > Therefore, the original limit evaluates to $$s/(s+1)$$.
> > 
> {: .solution}
{: .challenge}



[==>](../50-9-extreme-values-of-functions)