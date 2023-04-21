---
title:  Trigonometric Substitution

questions:
- "How to evaluate integrals using trigonometric substitution?"
objectives:
- "Evaluate integrals using trigonometric substitution"
---

# Trigonometric Substitution

## Concepts / Definitions

How do we solve these algebraically?

$$\int \sqrt{4 - x^2} dx$$

let $$x = 2\sin\theta$$, $$\frac{dx}{d\theta} = 2\cos\theta$$, $$dx = 2\cos\theta d\theta$$

$$\int \sqrt{4-4\sin^2\theta} 2\cos\theta d\theta$$

$$2\int \sqrt{4(1-\sin^2\theta)} \cos\theta d\theta$$

$$4\int \sqrt{\cos^2\theta)} \cos\theta d\theta$$

$$4\int \cos^2\theta d\theta$$

### Seperate

$$2[\sin\theta\cos\theta + \theta] + C$$

$$2[\frac x2  + \arcsin \frac x2] + C$$

> ## 7.1.10 Exercise 1 - Check the formulas for the derivatives of $$\tan x,\sec x,\csc x and \cot x$$.
> > 
> > ## Solution
> >
> > The formulas for the derivatives of the trigonometric functions are:\
> > Derivative of $$\tan x$$:
> > - $$\frac{d}{dx} \tan x = \sec^2 x$$\
> > Derivative of $$\sec x$$:
> > - $$\frac{d}{dx} \sec x = \sec x \tan x$$\
> > Derivative of $$\csc x$$:
> > - $$\frac{d}{dx} \csc x = -\csc x \cot x$$\
> > Derivative of $$\cot x$$:
> > - $$\frac{d}{dx} \cot x = -\csc^2 x$$\
> > Here, $$\sec x$$, $$\csc x$$, and $$\cot x$$ are the reciprocal functions of $$\cos x$$, $$\sin x$$, and $$\tan x$$ respectively.
> {: .solution}
{: .challenge}
> ## 7.1.10 Exercise 2 - Obtain the addition formula for $$\tan x$$ (familiar from school mathematics):    $$\tan u + \tan v = \tan(u + v) / (1 - \tan u \tan v)$$.
> > 
> > ## Solution
> >
> > To obtain the addition formula for tangent, we start by expressing tan(u+v) in terms of tangent functions of $$u$$ and $$v$$. We have:\
> > $$\tan(u+v) = \sin(u+v)/\cos(u+v)$$\
> > Using the sum formulas for sine and cosine, we get:\
> > $$\tan(u+v) = (\sin u \cos v + \cos u \sin v)/(\cos u \cos v - \sin u \sin v)$$\
> > Rearranging terms, we obtain:\
> > $$\tan(u+v) = (\tan u + \tan v)/(1 - \tan u \tan v)$$\
> > Multiplying both sides by $$1 - \tan u \tan v$$, we get:\
> > $$\tan(u+v)(1 - \tan u \tan v) = \tan u + \tan v$$\
> > Expanding the left-hand side, we get:\
> > $$\tan u + \tan v - \tan u \tan v \tan(u+v) = \tan u + \tan v$$\
> > Canceling the terms on both sides, we obtain the desired addition formula for tangent:\
> > $$\tan(u+v) = (\tan u + \tan v)/(1 - \tan u \tan v)$$
> > This is the formula we were asked to derive, which shows the relationship between the tangent of the sum of two angles and the tangents of the individual angles.\
> {: .solution}
{: .challenge}
> ## 7.1.10 Exercise 3 - Let $$t = \tan(x /2)$$. Express $$\sin x, \cos x and \tan x$$ as rational functions of $$t$$ .
> > 
> > ## Solution
> >
> > We can express sin x, cos x, and tan x in terms of t as follows:\
> > First, we note that:\
> > $$\tan(x) = 2 \tan(x/2) / (1 - \tan^2(x/2))$$\
> > Substituting $$t$$ for $$\tan(x/2)$$, we get:\
> > $$\tan(x) = 2t / (1 - t^2)$$\
> > Solving for $$\sin x and \cos x$$:\
> > $$\sin x = 2 \tan(x/2) / (1 + \tan^2(x/2))= 2t / (1 + t^2)$$\
> > $$\cos x = (1 - \tan^2(x/2)) / (1 + \tan^2(x/2))$$ = $$(1 - t^2) / (1 + t^2)$$\
> > Finally, we have:\
> > $$\tan x = \sin x / \cos x$$
> >       $$ = (2t / (1 + t^2)) / ((1 - t^2) / (1 + t^2))$$\
> >       $$ = 2t / (1 - t^2)$$\
> > Therefore, we have expressed $$\sin x, \cos x, and \tan x$$ as rational functions of $$t$$.
> {: .solution}
{: .challenge}
> ## 7.1.10 Exercise 5 - Prove the following formulas, no doubt familiar to you from school mathematics. They are important tools for integration.
> >### (a) $$ 1 + \tan^2(x/2) =\ sec^2(x/2)$$
> > ## Solution
> >
> > To prove the identity $$1 + \tan^2(x/2) = \sec^2(x/2)$$, we can start with the definition of tangent and secant:\
> > $$\tan(x/2) = \sin(x/2) / \cos(x/2)$$\
> > $$\sec(x/2) = 1 / \cos(x/2)$$\
> > Squaring both sides of the secant definition, we get:\
> > $$\sec^2(x/2) = 1 / \cos^2(x/2)$$\
> > Using the Pythagorean identity $$\sin^2(x/2) + \cos^2(x/2) = 1$$, we can solve for $$\cos^2(x/2)$$:\
> > $$\cos^2(x/2) = 1 - \sin^2(x/2)$$\
> > Substituting this into the definition of tangent, we get:\
> > $$\tan^2(x/2) = \sin^2(x/2) / (1 - \sin^2(x/2))$$\
> > We can then simplify this expression using the Pythagorean identity again:\
> > $$\tan^2(x/2) = \sin^2(x/2) / \cos^2(x/2)$$\
> >            $$ = (\sin(x/2)/\cos(x/2))^2$$\
> >            $$ = \tan^2(x/2)$$\
> > Substituting this into the original expression for sec^2(x/2), we get:\
> > $$\1 + \tan^2(x/2) = 1 + sin^2(x/2) / cos^2(x/2)$$\
> >                $$  = cos^2(x/2) / cos^2(x/2) + sin^2(x/2) / cos^2(x/2)$$\
> >                $$  = (sin^2(x/2) + cos^2(x/2)) / cos^2(x/2)$$\
> >                $$  = 1 / cos^2(x/2)$$\
> >                $$  = sec^2(x/2)$$\
> > Therefore, we have proven the identity $$1 + \tan^2(x/2) = \sec^2(x/2)$$.
> {: .solution}
{: .challenge}
> >### (b) $$ \sin(2x) = 2\sin(x)\cos(x)$$
> > ## Solution
> >
> > To prove the double angle formula $$\sin(2x) = 2\sin(x)cos(x)$$, we can use the angle addition formula for sine:\
> > $$\sin(a + b) = \sin(a)\cos(b) + \cos(a)\sin(b)$$\
> > Setting $$a = b = x$$, we get:\
> > $$\sin(2x) = \sin(x + x) = \sin(x)\cos(x) + \cos(x)\sin(x)$$\
> >         $$ = 2sin(x)cos(x) $$\
> > Therefore, we have proven the double angle formula $$\sin(2x) = 2\sin(x)\cos(x).$$\
> {: .solution}
{: .challenge}
> >### (c) $$ \cos(2x) = \cos^2(x) - \sin^2(x)$$
> > ## Solution
> >
> > To prove the double angle formula $$\cos(2x) = \cos^2(x) - \sin^2(x)$$, we can use the angle addition formula for cosine:\
> > $$\cos(a + b) = \cos(a)\cos(b) - \sin(a)\sin(b)$$\
> > Setting $$a = b = x$$, we get:\
> > $$\cos(2x) = \cos(x + x) = \cos(x)\cos(x) - \sin(x)\sin(x)$$\
> >         $$ = cos^2(x) - sin^2(x)$$\
> > Therefore, we have proven the double angle formula $$\cos(2x) = \cos^2(x) - \sin^2(x)$$.\
> > This relates the cosine and sine functions of twice an angle to the cosine and sine functions of the angle itself.
> {: .solution}
{: .challenge}
> >### (d) $$ \cos(2x) = 2\cos^2(x) - 1$$
> > ## Solution
> >
> > To prove the double angle formula cos(2x) = 2cos^2(x) - 1, we can use the angle addition formula for cosine:
> > $$\cos(a + b) = \cos(a)\cos(b) - \sin(a)\sin(b)$$\
> > Setting $$a = b = x$$, we get:\
> > $$\cos(2x) = \cos(x + x) = \cos(x)\cos(x) - \sin(x)\sin(x)$$\
> >        $$  = \cos^2(x) - \sin^2(x)$$\
> > Now, using the Pythagorean identity $$\cos^2(x) + \sin^2(x) = 1$$, we can express $$\sin^2(x)$$ in terms of $$\cos^2(x)$$:\
> > $$\sin^2(x) = 1 - \cos^2(x)$$\
> > Substituting this into the previous equation, we get:\
> > $$\cos(2x) = \cos^2(x) - (1 - \cos^2(x))$$\
> >        $$  = 2cos^2(x) - 1$$\
> {: .solution}
{: .challenge}
> >### (e) $$ \cos(2x) = 1 - 2\sin^2(x)$$
> > ## Solution
> >
> > To prove the double angle formula $$\cos(2x) = 1 - 2\sin^2(x)$$, we can use the angle addition formula for cosine:\
> > $$\cos(a + b) = \cos(a)\cos(b) - \sin(a)\sin(b)$$\
> > Setting $$a = b = x$$, we get:\
> > $$\cos(2x) = \cos(x + x) = \cos(x)\cos(x) - \sin(x)\sin(x)$$\
> >         $$ = cos^2(x) - sin^2(x)$$\
> > Now, using the Pythagorean identity $$\cos^2(x) + \sin^2(x) = 1$$, we can express $$\cos^2(x)$$ in terms of $$\sin^2(x)$$:\
> > $$\cos^2(x) = 1 - \sin^2(x)$$\
> > Substituting this into the previous equation, we get:\
> > $$\cos(2x) = (1 - \sin^2(x)) - \sin^2(x)$$\
> >         $$ = 1 - 2sin^2(x)$$\
> > Therefore, we have proven the double angle formula $$\cos(2x) = 1 - 2\sin^2(x)$$.\
> {: .solution}
{: .challenge}
> >### (f) $$ \cos(3x) = 4\cos^3(x) - 3\cos(x)$$
> > ## Solution
> >
> > To prove the triple angle formula for cosine $$\cos(3x) = 4\cos^3(x) - 3\cos(x)$$, we can use the angle addition formula for cosine to derive a formula for $$\cos(3x)$$ in terms of $$\cos(x)$$ and $$\sin(x)$$:\
> > $$\cos(3x) = \cos(2x + x) = \cos(2x)\cos(x) - \sin(2x)\sin(x)$$\
> > Using the double angle formula $$\cos(2x) = 2\cos^2(x) - 1$$ and the angle addition formula for sine\
> > $$\sin(a + b) = \sin(a)\cos(b) + \cos(a)\sin(b)$$, we can simplify the above equation as follows:\
> > $$\cos(3x) = (2\cos^2(x) - 1)\cos(x) - 2\sin(x)\cos(x)\sin(x)$$\
> > $$         = 2\cos^3(x) - \cos(x) - 2\sin^2(x)\cos(x)$$\
> > $$         = 2\cos^3(x) - \cos(x) - 2(1 - \cos^2(x))\cos(x)$$\
> > $$         = 2\cos^3(x) - \cos(x) - 2\cos(x) + 2\cos^3(x)$$\
> > $$         = 4\cos^3(x) - 3\cos(x)$$\
> > Therefore, we have proven the triple angle formula for cosine $$\cos(3x) = 4\cos^3(x) - 3\cos(x)$$.
> {: .solution}
{: .challenge}
> >### (g) $$ \sin(3x) = 3\sin(x) - 4\sin^3(x)$$
> > ## Solution
> >
> > To prove the triple angle formula for sine $$\sin(3x) = 3\sin(x) - 4\sin^3(x)$$, we can use the angle addition formula for sine to derive a formula for $$\sin(3x)$$ in terms of $$sin(x)$$ and $$cos(x)$$:\
> > $$\sin(3x) = \sin(2x + x) = \sin(2x)\cos(x) + \cos(2x)\sin(x)$$\
> > Using the double angle formula for sine $$\sin(2x) = 2\sin(x)\cos(x)$$ and the double angle formula for cosine\
> > $$\cos(2x) = 2\cos^2(x) - 1$$, we can simplify the above equation as follows:\
> > $$\sin(3x) = 2\sin(x)\cos^2(x) + (2\cos^2(x) - 1)\sin(x)$$\
> > $$        = 2\sin(x)\cos^2(x) + 2\cos^2(x)\sin(x) - \sin(x)$$\
> > $$        = \sin(x)(4\cos^2(x) - 1)$$\
> > $$        = \sin(x)(2 - (2\sin^2(x)))$$\
> > $$        = 3\sin(x) - 4\sin^3(x)$$\
> > Therefore, we have proven the triple angle formula for sine:\
> > $$\sin(3x) = 3\sin(x) - 4\sin^3(x)$$
> {: .solution}
{: .challenge}