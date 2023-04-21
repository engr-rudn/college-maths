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

> ## 7.1.10 Exercise 1 - Check the formulas for the derivatives of $$tan x,sec x,csc x and cot x$$.
> > 
> > ## Solution
> >
> > The formulas for the derivatives of the trigonometric functions are:\
> > Derivative of $$\tan x$$:\
> > $$\frac{d}{dx} \tan x = \sec^2 x$$\
> > Derivative of $$\sec x$$:\
> > $$\frac{d}{dx} \sec x = \sec x \tan x$$\
> > Derivative of $$\csc x$$:\
> > $$\frac{d}{dx} \csc x = -\csc x \cot x$$\
> > Derivative of $$\cot x$$:\
> > $$\frac{d}{dx} \cot x = -\csc^2 x$$
> > Here, $$\sec x$$, $$\csc x$$, and $$\cot x$$ are the reciprocal functions of $$\cos x$$, $$\sin x$$, and $$\tan x$$ respectively.
> {: .solution}
{: .challenge}