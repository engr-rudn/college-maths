---
title: Rational Expressions
questions:
- "What basic?"
- "How can ?"
- "How do ?"
- "Can I ?"
objectives:
- "???"
- "???"
---
# Rational Expressions

## Domain of a Rational Expression

* A rational expression in the form $$\frac{a}{b}$$ would have a limited domain because $$b \neq 0$$
* For example, $$\frac{2x+1}{3-x}$$ would have the domain $$(-\infty, 3)\cup(3, \infty)$$ because if $$x=3$$, then the denominator is 0, which is undefined
* Also, a rational expression in the form $$\sqrt{a}$$ has a limited domain because $$a \geq 0$$
* For example, $$\sqrt{5x +2}$$ would have the domain $$(-\frac{5}{2}, 0)$$

## Simplifying a rational expression

* The distributive property can be used to simplify a rational expressions
* Factor out a rational expression completely, and then you can divide out by the common factors
* Remember that $$\frac{a + b}{c} \neq \frac{a \cdot b}{c}$$, so don't make the mistake of dividing by terms!
* Finally, look out for any domain restrictions (e.g. square root, zero division)

## Dividing Rational Expressions

E.g. 

$$\frac{x^3-8}{x^2-4}$$

## Subtracting Rational Expressions

E.g.

$$
\frac{2}{x+1} + \frac{2}{x-1} + \frac{1}{x^2-1}
$$

## Rational Functions

A **rational function** is a function that *can be* in the standard form:

$$
f(x) = \frac{N(x)}{D(x)}
$$

where $$N(x)$$ and $$D(x)$$ are polynomials and $$D(x)$$ is not the zero polynomial.

Note that rational functions are *not* necessarily given to you in this form, but you can convert any rational function to this form.

### Finding all of the zeroes of a rational function

Let's say you were given this rational function and were asked to find its zeroes: 

$$
f(x) = \frac{x^2-1}{x^2-2x-3}
$$

To do so, we have to set $$f(x) = 0$$. So we have:

$$
0 = \frac{x^2-1}{x^2-2x-3}
$$

$$
0 = x^2-1
$$

$$
0 = x^2-1
$$

$$
x = 1, x = -1
$$

But that's not all! We have to check for _domain restrictions_. Remember, in a rational function, the denominator cannot equal zero. So, that means:

$$
x^2 -2x -3 \neq 0
$$

$$
(x+1)(x-3) \neq 0
$$

$$
x \neq -1, x \neq 3
$$

That means that of our two _possible_ zeroes, $$1$$ and $$-1$$, there is only one actual zero, because $$x \neq -1$$.

So, we have our answer! The (only) zero is 1.

### Asymptotes of Rational Functions

We find the **vertical asymptote** using our denominator, since we know that the denominator cannot be equal to zero. For instance, if we have a rational function $$f(x) = \frac{1}{x^2}$$, we know that $$x^2 \neq 0$$. Solving that gives us $$\pm x \neq 0$$.

Because $$x$$ cannot be _exactly_ zero, but can be _very close_ to zero, we have an asymptote - a line that the rational function never touches. In our case, the vertical asymptote is the line $$x = 0$$, because $$f(x)$$ can never be zero.

We find the **horizontal asymptote** using the leading coefficients of the numerator and denominator as a fraction. For example, let's take the rational function $$g(x) = \frac{2x}{x + 1}$$. The leading coefficient of the _numerator's_ first term $$2x$$ is $$2$$. The leading coefficient of the _denominator's_ first term $$1x$$ is $$1$$.

Our horizontal asymptote is the **numerator's coefficient divided by the denominator's coefficient**. That means it is equal to $$\frac{2}{1} = 2$$. So our horizontal asymptote is the line $$y = 2$$.

But what if our rational function has a numerator and denominator of differing degrees? Let's take $$h(x) = \frac{x}{x^3 + 3x}$$ as an example. The numerator's first term $$x$$ is of degree 1, but the denominator's first term $$x^3$$ is of degree 3. So what do we do?

The solution is to add a zeroed placeholder term to the numerator. Remember that our function $$h(x) = \frac{x}{x^3 + 3x}$$ can also be written out like this:

$$
h(x) = \frac{0x^3 + 0x^2 + x}{x^3 + 3x}
$$

That's now much easier! Once we equalize the degrees, we can use our normal formula. The numerator's first term's coefficient is $$0$$, and the denominator's first term's coefficient is $$1$$. So our horizontal asymptote is $$\frac{0}{1} = 0$$, which means it's the line $$y = 0$$.

If a rational function has **no vertical asymptote**, we say that it is _continuous_. Otherwise, we say that it is _non-continuous_.

### Holes in Rational Functions

**Holes**, technically called _points of discontinuity_, are undefined points on the graph of a rational function. We show them on the graph of a rational function as open circles, like this:

![Example graph with hole](https://www.onlinemath4all.com/images/holeofafunction1.png)

To understand why a hole exists, let's consider a very basic rational function with a hole:

$$
f(x) = \frac{x}{x^2}
$$

What would happen if $$x=0$$? Well, if we substitute, we get this:

$$
f(0) = \frac{(0)}{(0)^2} = \frac{0}{0} = \ ?
$$

And $$\frac{0}{0}$$ is undefined. That's why there is a hole, a point that cannot exist in the graph.

A greatest common factor cancellation gives us the holes of a rational function. To understand what this means, let's try to find the holes of a basic rational function $$f(x)$$:

$$
f(x) = \frac{x^2-1}{x+1}
$$

So how do we know that $$f(x)$$ has a hole? The answer lies in its _factors_. When a rational function has a **common factor** in both its numerator and denominator, then it must have a hole.

When we simplify $$f(x)$$ like this:

$$
f(x) = \frac{x^2-1}{x+1} =\frac{(x+1)(x-1)}{x+1}
$$

We see that the factor $$(x+1)$$ in both its numerator (top) and denominator (bottom). So it has a hole. But where is that hole?

The x-coordinate of the hole is found using the **common factor**. In our case, that common factor is $$(x+1)$$. If we solve the equation $$x+1 = 0$$, we find that $$x = -1$$. That is the x-coordinate of our hole.

The y-coordinate of the hole is found by "plugging in" the hole's x-coordinate into the _remainder function_. Let's find our remainder function first. To do this, cross out the factor from the original function:

$$
f(x) = \frac{\cancel{(x+1)}(x-1)}{\cancel{x+1}} 
$$ 

This leaves us with the function $$f_{rem.}(x) = x-1$$, which is our **remainder function**. If we plug our x-coordinate $$x = -1$$ into $$f_{rem.}(x)$$, then we get $$y = -2$$. This is our y-coordinate. So, we now have the complete set of coordinates for the hole, and we know that the hole was located at $$(-1, -2)$$.

There is one last important property about holes - since they are points where a rational function is not defined, there are no asymptotes, zero or intercepts possible at the same position as a hole. That means that in our example $$f(x) = \frac{x^2-1}{x+1}$$, even if it had an asymptote of $$x=-1$$ or an intercept, say, at $$(-1, 3)$$, these **would not exist** because of the hole at $$(-1, -2)$$! The hole reigns absolute when finding the graph of a rational function!

### Intercepts of Rational Functions

To find the intercepts, we use the same technique as we use to find the intercepts for any other type of function.

To find x-intercepts, we simply set $$f(x) = 0$$. To find y-intercepts, we simply set $$x = 0$$. Let's see how this works in practice, by finding the intercepts of the rational function $$f(x) = \frac{x+1}{x-4}$$.

Let's find the x-intercept first. We know that we can find the x-intercept by setting $$f(x) = 0$$. So let's substitute that in:

$$
f(x) = \frac{x+1}{x-4}
$$

$$
0 = \frac{x+1}{x-4}
$$

Now, we can just solve algebraically:

$$
0(x-4) = x+1
$$

$$
0 = x+1
$$

$$
x = -1
$$

This gives us the **x-intercept** of $$(-1, 0)$$. Now, let's find the y-intercept by setting $$x = 0$$:

$$
f(x) = \frac{(0)+1}{(0)-4}
$$

$$
f(x) = -\frac{1}{4}
$$

This gives us the **y-intercept** of $$(0, -\frac{1}{4})$$.

However, we're not done yet! Rational function intercepts have a special property - they often have _restricted values_. If the rational function has asymptotes or holes, then they **cannot** be an intercept! So, let's check our solution for $$f(x) = \frac{x+1}{x-4}$$ for restricted values.

The vertical asymptote of $$f(x)$$ is $$x = 4$$. Our x-intercept is $$(-1, 0)$$, which is different, so this doesn't affect it. The horizontal asymptote of $$f(x)$$ is $$y = 1$$. Our y-intercept is $$(0, -\frac{1}{4})$$, which is different too, so this doesn't affect it either. There are also no holes, so they don't affect the intercepts.

So there you have it - the intercepts of the function $$f(x) = \frac{x+1}{x-4}$$ are $$(-1, 0)$$ (for $$x$$) and $$(0, -\frac{1}{4})$$ (for $$y$$), and none of them are subject to restricted values!

### Domain and Range of Rational Functions

Now that we know the holes and asymptotes, we can find the domain and range.

Remember, since the vertical asymptote is a value $$x$$ can never reach, it is a _domain restriction_.

Similarly, since the horizontal asymptote is a value $$y$$ can never reach, it is a _range restriction_.

### End Behavior of Rational Functions

## Graphing a Rational Function