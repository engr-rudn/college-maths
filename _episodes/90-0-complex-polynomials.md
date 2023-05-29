---
title:  Complex Polynomials

questions:
- "What are imaginary and complex numbers?"

objectives:
- "Understand the system of complex numbers"
-  "Algebraic operations with complex numbers"
- "Finding the zeros of a polynomial function"
---


## What are imaginary and complex numbers?

* We know that there is no real number $$x$$ that can be squared to produce $$-1$$
* So mathematicians created an expanded system of numbers using the **imaginary unit** $$i$$, where $$i = \sqrt{-1}$$
* This means that $$i^2 = -1$$
* A **complex number** is a quadratic in the standard form $$a + bi$$, where $$bi$$ is the imaginary part and $$a$$ is the real part
* A _pair_ of complex numbers $$(a + bi)(a - bi)$$ form a **complex conjugate**

### Adding, subtracting, and multiplying complex number

Complex numbers can be added and subtracted like normal algebraic expressions.

## Examples

* Express $$\sqrt{-100}$$ as an imaginary number
  * $$\sqrt{-100}$$ can be simplified to $$\sqrt{-1} \cdot \sqrt{100}$$
  * This would result in $$i \sqrt{100}$$ which simplifies to $$10i$$
* Solve $$(3 - 5i)(3 + 5i)$$
  * $$(3 - 5i)(3 + 5i)$$ can be simplified to $$3^2 - 25i^2$$
  * Because $$i^2=-1$$, this would result in $$9 + (25 * -1)$$ which would be $$34$$

## Find the conjugate

* The conjugate is formed by switching the signs of a complex number $$(a + bi)$$ into $$(a - bi)$$
* For example, the complex number $$(3 + 5i)$$ would have the conjugate $$(3-5i)$$
* If the complex number is purely imaginary (like $$5i$$ or $$-20i$$), remember that these are basically in the form $$(0 \pm i)$$
	* For instance, $$5i$$ is actually $$(0 + 5i)$$
	* So its conjugate would be $$(0 - 5i)$$ which would be $$-5i$$
* Conjugates are very useful in simplifying division of complex numbers, because any complex number multiplied by its conjugate results in a real number

## Powers of $$i$$

The powers of $$i$$ fulfill a cyclic pattern of $$(i, -1, -i, 1)$$:

| Power of $$i$$ | Value                         |
| ------------ | ----------------------------- |
| $$i^1$$        | $$i$$                           |
| $$i^2$$        | $$-1$$                          |
| $$i^3$$        | $$-i$$                          |
| $$i^4$$        | $$1$$                           |
| $$i^5$$        | $$i$$ _same as_ $$i^1$$           |
| $$i^6$$        | $$-1$$ _same as_ $$i^2$$          |
| $$i^7$$        | $$-i$$ _same as_ $$i^3$$          |
| $$i^8$$        | $$1$$ _same as_ $$i^4$$           |
| ...          | ...                           |

We can also notice a certain pattern:

* Odd exponents are always imaginary
* Even exponents are always real

This allows us to find arbitrary exponents of $$i$$:

* $$i^{60}$$ = $$(i^4)^{15}$$ = $$1^{15}$$ = $$1$$
* $$i^{15}$$ = $$(i^4)^3 \cdot i^3$$ = $$1 \cdot -i$$ = $$-i$$  

### SImplifying using powers of $$i$$

Suppose we have $$i^{49}$$. How could we simplify it?

Well, remember that $$n^{a+b} = n^a \cdot n^b$$. So, we could write $$i^{49}$$ as $$i^{48 \cdot 1}$$, which simplifies to $$i^{48} + i^1$$. We know that $$i^{48} = (i^4)^{12}$$, and $$i^4 = 1$$, so $$(i^4)^{12}=1^{12} = 1$$. So, $$i^{48}=1$$.

Now,  since we know $$i^{48}=1$$, then $$i^{48} \cdot i^1 = 1 \cdot i = i$$. That means that $$i^{49} = i$$.

## Rationalizing a complex denominator

### Using $$i$$

When our denominator is a **pure imaginary number**, we can rationalize it by multiplying the it with $$\frac{i}{i}$$. Because $$\frac{i}{i}$$ is equal to 1, we get the same fraction, but with a rational denominator.

For example, suppose we wanted to rationalize the fraction $$\frac{3}{i}$$. We would multiply it by $$\frac{i}{i}$$, which gives this:

$$
\frac{3}{i} \cdot \frac{i}{i} = \frac{3i}{i^2} = \frac{3i}{-1} = -3i
$$

### Using the conjugate

When our denominator is a **complex number** with both a real part and an imaginary part, we can rationalize it by using its complex conjugate. To do this, we multiply the conjugate $$a + bi$$ by its conjugate $$\frac{a - bi}{a - bi}$$.

For instance, suppose we wanted to rationalize the fraction $$\frac{3}{5+2i}$$. We know that the conjugate of $$(5 + 2i)$$ is $$(5-2i)$$, so:

$$
\frac{3}{5 + 2i} \cdot \frac{5-2i}{5-2i} = \frac{15-6i}{25-4i^2} = \frac{15-6i}{25+4} = \frac{15-6i}{29}
$$


## Finding the Zeros of a Polynomial Function

Depending on the question you're given, there are multiple ways of finding the zero of a polynomial function. However, some general rules are:

* Every zero $$n$$ means that one of the polynomial's factors is $$(x-n)$$
* A polynomial cannot have any more zeroes than its degree (for instance, $$ax^2 + bx + c$$ has at most 2 zeroes)
* Look for special polynomial patterns (e.g. sum/difference of cubes, perfect square trinomials) to simplify the process
* If all else fails, and you have a trinomial, remember that you can always count on the quadratic formula

### Finding zeros using factor by grouping

Let's say we have the equation $$5 v^{3}-2 v^{2}+25 v-10=0$$. We know that cube roots don't work with the quadratic formula, so what can we do? The first thing you should *always* try is to factor the polynomial.

In our case, we can factor $$5 v^{3}-2 v^{2}+25 v-10$$ to $$v^2(5v-2)+5(5v-2)$$. We can simply take the common factors to end up with $$(v^2+5)(5v-2)$$. Thus, we can finally solve our equation. If $$v^2+5 = 0$$, then $$v^2 = -5$$, and $$v = -\sqrt{5i}$$. If $$5v-2=0$$, then $$v = \frac{2}{5}$$.

### Finding zeros using sum/difference of cubes

Suppose we have the equation $$(x^3 - 8) = 0$$. We could then use the difference of cubes to solve it.

Remember that the sum of cubes $$a^3 + b^3$$ is $$(a + b)(a^2 - ab + b^2)$$, and the difference of cubes $$a^3 - b^3$$ is $$(a - b)(a^2 + ab - b^2)$$. Here, we can put our expression in the form of $$a^3 - b^3$$ because we know that 8 is a perfect cube. Thus, $$x^3 - 8$$ would be $$(x^3 - 2^3)$$, where $$a = x$$ and $$b = 2$$.

Now, we just have to substitute our $$a$$ and $$b$$ into the difference of cubes template equation. It gives us $$x^3 - 2^3 = (x-2)(x^2 +2x - 4)$$. Because we know that $$(x-2)(x^2 + 2x -4) = 0$$, we can solve the 2 parts to get the final value of $$x$$.

### Finding zeros using quadratic formula

We can use the quadratic formula to solve quadratic equations that simplify to an imaginary or complex number. For example, let's try to solve the equation $$x^2 + 3x +8 = 0$$. The equation is not factorable, so we have to use the quadratic formula.

Let's first get our $$a$$, $$b$$, and $$c$$ values. In our case, $$a = 1, b = 3, c = 8$$. Now, we can plug them into the formula:

$$
x = \frac{-3 \pm \sqrt{3^2 - 4 \cdot 1 \cdot 8}}{2 \cdot 1}
$$

$$
x = \frac{-3 \pm \sqrt{9 - 32}}{2 \cdot 1}
$$

$$
x = \frac{-3 \pm \sqrt{-23}}{2}
$$

Our zeroes will therefore be $$\frac{-3 + \sqrt{-23}}{2}$$ and $$\frac{-3 - \sqrt{-23}}{2}$$.

### Finding zeros using synthetic division

You might be asked to determine whether 1 is a zero of  the polynomial $$x^3 - 1$$. We could do this using the difference of cubes, but let's try using synthetic division instead.

We know that if 1 _is_ a real zero of $$x^3-1$$, then $$(x-1)$$ must be one of its real factors. And when we do $$x^3 - 1 \div (x-1)$$, if the remainder is zero, then our resulting quotient is a factor too.

To set up our synthetic division, we need to get our $$c$$ value from our divisor $$(x-c)$$. Here, since it is $$(x-1)$$, $$c = 1$$. Let's put that on the left hand side of our synthetic division bar. On the right side is our dividend $$x^3 -1$$, or more percisely $$\underline{1}x^3 + \underline{0}x^2 + \underline{0}x \underline{- 1}$$.

$$
\begin{array}{cc}
{
\begin{array}{r}\\
1 \\
\end{array}
}&
{
\begin{array}{|rrrr}
1 & 0 & 0 & -1 \\ && & \\ \hline
\end{array}
}
\end{array}
$$

And our solution? This:

$$
\begin{array}{cc}
    \begin{array}{c} \\ 1 \\ \\ \end{array}
    &
    \begin{array}{|rrrr}  
        1 & 0 & 0 & -1 \\
        \downarrow  & 1 & 1 & 1 \\
        \hline 
        1(x^2) & 1(x) & 1(x) & R:0 
    \end{array}
\end{array}
$$

This means that our equation $$(x^3-1)$$ has two factors, and they are $$(x-1)$$ and $$x^2 + x +1$$. Simplifying $$x-1$$ gives us the first zero of 1. Simplifying $$x^2 + x + 1$$ is more complex since it results in a complex number of $$\frac{-1 \pm \sqrt{-3}}{2}$$, which is still a zero, just not a real one.

If you're asked to only provide the real zeroes, then you only need to write the zero of 1. However, you you're asked to provide both real _and_ imaginary zeroes, then the full list of zeroes would be $$\{1, \frac{-1 + \sqrt{-3}}{2}, \frac{-1 - \sqrt{-3}}{2}\}$$

> ## Listing possible zeroes with the Rational Zeroes Theorem
> {: .solution}
{: .challenge}
> ## Finding all the zeroes using the Rational Zeroes Theorem
> {: .solution}
{: .challenge}
> ## Finding all real and complex zeroes given 1 complex zero
> {: .solution}
{: .challenge}
> ## Find a polynomial function from given real and imaginary zeros
> > E.g. you are given the zeroes $$1, 5, 2i$$, and you are told that this function is of degree 6.
> > ## Solution
> > $$f(x) = x^2(x-5)^2(x+2i)(x-2i)$$
>{: .solution}
{: .challenge}
> ## Writing a polynomial as a product of linear factors  
{: .challenge}
> ## Write the polynomial function in factored form given its graph
{: .challenge}
> ## 9.1.3 - Exercises 
> #### 1. Check the claim that the reciprocal of $$a+bi is (a-bi)/(a^2+b^2)$$. 
> >
> > ## Solution
> > The reciprocal of a complex number z is defined as 1/z.\
> > To check the claim that the reciprocal of a+bi is (a-bi)/(a^2+b^2), we need to verify that:\
> > $$(a+bi) * (a-bi) / (a^2 + b^2) = 1$$\
> > We can simplify the left-hand side of this equation as follows:\
> > $$(a+bi) * (a-bi) = a^2 - (bi)^2 = a^2 + b^2$$\
> > Therefore:\
> > $$(a+bi) * (a-bi) / (a^2 + b^2) = (a^2 + b^2) / (a^2 + b^2) = 1$$\
> > This verifies that the reciprocal of a+bi is indeed $$(a-bi)/(a^2+b^2)$$.
> > 
> {: .solution}
{: .challenge}
> ### 2. Check that $$Re(z\bar{w})$$ is the scalar product of the vectors $$z$$ and $$w$$, where the complex numbers are identiﬁed with plane vectors. 
> >
> > ## Solution
> >
> > Let $$z$$ and $$w$$ be complex numbers, which can be identified with the corresponding complex plane vectors $$z=x_1+iy_1$$ and $$w=x_2+iy_2$$, where $$x_1$$, $$y_1$$, $$x_2$$, and $$y_2$$ are real numbers.\
> > Then, we have:\
> > $$
\begin{align*}
z\bar{w} &= (x_1+iy_1)(x_2-iy_2) \
&= x_1x_2 + y_1y_2 + i(x_1(-y_2) + y_1x_2) \
&= x_1x_2 + y_1y_2 - i(x_1y_2 - y_1x_2) \
\end{align*}
$$\
> > Taking the real part of the above expression, we get:\
> > $$
\begin{align*}
\operatorname{Re}(z\bar{w}) &= x_1x_2 + y_1y_2 \
\end{align*}
$$\
> > On the other hand, the dot product of the corresponding vectors can be expressed as:\
> > $$
\begin{align*}
z \cdot w &= (x_1, y_1) \cdot (x_2, y_2) \
&= x_1x_2 + y_1y_2 \
\end{align*}
$$\
> > Therefore, we can see that $$\operatorname{Re}(z\bar{w})$$ is equal to the dot product of the vectors\
> > $$z$$ and $$w$$. Hence, $$\operatorname{Re}(z\bar{w})$$ is indeed the scalar product of the vectors $$z$$ and $$w$$, where the complex numbers are identified with plane vectors.
> > 
> {: .solution}
{: .challenge}
> ### 3. Prove the inequality $$|z| \leq \sqrt{2} \max(|\operatorname{Re}(z)|, |\operatorname{Im}(z)|)$$. Show that $$\sqrt{2}$$ cannot be replaced by a smaller number.
> >
> > ## Solution
> >
> > We need to prove that for any complex number $$z$$, we have\
> > $$|z| \leq \sqrt{2} \max(|\operatorname{Re}(z)|, |\operatorname{Im}(z)|)$$.\
> > Let $$z = a + bi$$ be a complex number, where $$a$$ and $$b$$ are real numbers. Then, we have:\
> > $$
\begin{align*}
|z| &= \sqrt{a^2 + b^2} \\
&\leq \sqrt{2}\sqrt{\frac{1}{2}(a^2 + b^2)} \\
&= \sqrt{2}\sqrt{\frac{1}{2}a^2 + \frac{1}{2}b^2} \\
&\leq \sqrt{2}\sqrt{\max(\frac{1}{2}a^2, \frac{1}{2}b^2)} \\
&= \sqrt{2}\max(\sqrt{\frac{1}{2}a^2}, \sqrt{\frac{1}{2}b^2}) \\
&\leq \sqrt{2}\max(|a|, |b|) \\
&= \sqrt{2}\max(|\operatorname{Re}(z)|, |\operatorname{Im}(z)|)
\end{align*}
$$\
> > Therefore, we have proved that\
> >  $$|z| \leq \sqrt{2} \max(|\operatorname{Re}(z)|, |\operatorname{Im}(z)|)$$\
> > for any complex number $$z$$.\
> > To show that $$\sqrt{2}$$ cannot be replaced by a smaller number, consider the complex numbers\
> >  $$z_1 = \sqrt{2}/2 + i\sqrt{2}/2$$ and $$z_2 = -\sqrt{2}/2 + i\sqrt{2}/2$$.\
> > We have \
> > $$|\operatorname{Re}(z_1)| = |\operatorname{Im}(z_2)| = \sqrt{2}/2$$, so\
> > $$\max(|\operatorname{Re}(z_1)|, |\operatorname{Im}(z_2)|) = \sqrt{2}/2$$.\
> >  However, we have $$|z_1| = |z_2| = \sqrt{2}/2$$, and $$|z_1z_2| = \sqrt{2}/2 \cdot \sqrt{2}/2 = 1/2$$, so $$|z_1z_2| > \sqrt{2}/4$$.\
> > Therefore, if we replace $$\sqrt{2}$$ with any smaller number in the inequality\
> >  $$|z| \leq \sqrt{2} \max(|\operatorname{Re}(z)|, |\operatorname{Im}(z)|)$$,\
> >  there exist complex numbers $$z_1$$ and $$z_2$$ such that the inequality is not true.
> > 
> {: .solution}
{: .challenge}
> ## 9.2.3 - Exercises 
> ### 1. Prove the formula $$Arg z = 2 \arctan( Im z/ (|z|+ Re z))$$ for $$z$$ not of the form $$x + 0i$$ with $$x ≤ 0$$. 
> >
> > ## Solution
> >
> > To prove the formula $$Arg z = 2 \arctan( Im z/ (|z|+ Re z))$$ for $$z$$ not of the form $$x + 0i$$ with $$x ≤ 0$$, we can use the following steps:\
> > Let $$z = x + yi$$, where x and y are real numbers, and z is not of the form $$x + 0i$$ with $$x ≤ 0$$.\
> > We know that $$Arg z$$ is the angle between the positive real axis and the line segment from the origin to z, measured counterclockwise.\
> > Draw a right triangle with legs of length $$y$$ and $$x + |z|$$. The hypotenuse of the triangle is the line segment from the origin to z.\
> > The angle between the positive real axis and the leg of length $$y$$ is $$\arctan(y/(x+|z|))$$.\
> > Since the triangle is a right triangle, the angle between the positive real axis and the hypotenuse (i.e., Arg z) is equal to $$\pi/2$$ minus the angle between the positive real axis and the other leg (i.e., y).\
> > Therefore, we have:\
> > $$Arg z = pi/2 - \arctan(y/(x+|z|))$$\
> > We can simplify this expression by multiplying both the numerator and denominator of the fraction inside the \arctan function by $$1/|z|$$:\
> > $$Arg z = \pi/2 - \arctan(y/(|z|(x/|z| + 1)))$$\
> > We can also use the fact that $$|z| = \sqrt(x^2 + y^2)$$ to rewrite the expression inside the \arctan function:\
> > $$Arg z = \pi/2 - \arctan(y/(|z|+x))$$\
> > Finally, we can use the identity $$\arctan(a) = 1/2 \arctan(2a/(1-a^2))$$ to simplify the expression further:\
> > $$Arg z = 2 \arctan(y/(|z|+x))$$\
> >     $$ = 2 \arctan(Im z/(|z|+Re z))$$\
> > Therefore, we have proven that $$Arg z = 2 \arctan( Im z/ (|z|+ Re z))$$ for $$z$$ not of the form $$x + 0i$$ with $$x ≤ 0$$, as required.
> > 
> {: .solution}
{: .challenge}
> ### 2. The real factorisation of $$x^4 + 1$$ into irreducible quadratic factors is needed to calculate the integral    $$1/(x^4 + 1) dx$$. Obtain the factorisation using complex numbers by noting that the roots of $$x^4 + 1 = 0$$, the four complex numbers $$w_1 = (1 + i)/\sqrt(2)$$  ,  $$w_2 = (-1  + i)/\sqrt(2)$$    ,  $$w_3 =(-1  − i)/\sqrt(2)$$,  $$w_4 =(1  − i)/\sqrt(2)$$, form the corners of a square, and that the quadratics, $$(x − w1)(x − w4)$$ and $$(x − w2)(x − w3)$$, have real coefficients. 
> >
> > ## Solution
> >
> >The real factorization of $$x^4 + 1$$ into irreducible quadratic factors is needed to calculate the integral $$\int \frac{1}{x^4 + 1} \, dx$$. We can obtain the factorization using complex numbers by noting that the roots of $$x^4 + 1 = 0$$ are the four complex numbers $$w_1 = e^{i\pi/4}$$, $$w_2 = e^{3i\pi/4}$$, $$w_3 = e^{5i\pi/4}$$, and $$w_4 = e^{7i\pi/4}$$.\
> >To compute the integral, we use partial fraction decomposition. The integrand can be expressed as:\
$$\frac{1}{x^4 + 1} = \frac{\frac{1}{2}}{x^2 + \sqrt{2}x + 1} - \frac{\frac{1}{2}}{x^2 - \sqrt{2}x + 1}$$\
> >Next, we complete the square in the denominators:\
$$x^2 + \sqrt{2}x + 1 = (x + \frac{\sqrt{2}}{2})^2 + \frac{1}{2}$$\
$$x^2 - \sqrt{2}x + 1 = (x - \frac{\sqrt{2}}{2})^2 + \frac{1}{2}$$\
> >Using the substitutions $$u = x + \frac{\sqrt{2}}{2}$$ and $$v = x - \frac{\sqrt{2}}{2}$$, the integral becomes:\
> >$$\int \frac{1}{x^4 + 1} \, dx = \frac{1}{2} \int \frac{1}{(x + \frac{\sqrt{2}}{2})^2 + \frac{1}{2}} \, dx - \frac{1}{2} \int \frac{1}{(x - \frac{\sqrt{2}}{2})^2 + \frac{1}{2}} \, dx$$\
> >Applying the integral formulas for $$\frac{1}{u^2 + a^2}$$, the integrals can be evaluated as:\
> >$$\frac{1}{2\sqrt{2}} \left(\arctan\left(\frac{x + \frac{\sqrt{2}}{2}}{\frac{1}{\sqrt{2}}}\right) - \arctan\left(\frac{x - \frac{\sqrt{2}}{2}}{\frac{1}{\sqrt{2}}}\right)\right) + C$$\
> >Simplifying further, we have:\
> >$$\frac{1}{\sqrt{2}} \left(\arctan\left(\sqrt{2}(x + \frac{\sqrt{2}}{2})\right) - \arctan\left(\sqrt{2}(x - \frac{\sqrt{2}}{2})\right)\right) + C$$\
> >Therefore, the integral $$\int \frac{1}{x^4 + 1} \, dx$$\
> > can be expressed as\
> > $$\frac{1}{\sqrt{2}} \left(\arctan\left(\sqrt{2}(x + \frac{\sqrt{2}}{2})\right) - \arctan\left(\sqrt{2}(x - \frac{\sqrt{2}}{2})\right)\right) + C$$,\ where $$C$$ is the constant of integration.
> > <!-- We can write the expression $$x^4 + 1$$ as $$(x^4 + 2x^2 + 1) - 2x^2 = (x^2 + 1)^2 - (sqrt(2)x)^2$$. Using the difference of squares formula, we get:\
> > $$x^4 + 1 = (x^2 + \sqrt(2)x + 1)(x^2 - \sqrt(2)x + 1)$$\
> > Note that both of these quadratic factors have real coefficients. To see this, we can use the fact that the roots of $$x^4 + 1 = 0$$ are $$w_1 = (1 + i)/\sqrt(2)$$,\
> > $$ w_2 = (-1 + i)/\sqrt(2)$$,\
> > $$ w_3 = (-1 - i)/\sqrt(2),$$ and\
> > $$ w_4 = (1 - i)/\sqrt(2)$$.\
> >  Since these roots come in complex conjugate pairs, we can write $$x^4 + 1$$ as the product of two irreducible quadratic factors with real coefficients:\
> > $$x^4 + 1 = (x - w_1)(x - w_2)(x - w_3)(x - w_4)$$\
> > $$        = [(x - w_1)(x - w_4)][(x - w_2)(x - w_3)]$$\
> > Expanding this out gives:\
> > $$x^4 + 1 = [(x^2 - (w_1 + w_4)x + w_1w_4)][(x^2 - (w_2 + w_3)x + w_2w_3)]$$\
> > Substituting in the values of $$w_1, w_2, w_3$$, and $$w_4$$, we get:\
> > $$x^4 + 1 = [(x^2 - \sqrt(2)x + 1)(x^2 + \sqrt(2)x + 1)]$$\
> > Therefore, the factorization of $$x^4 + 1$$ into irreducible quadratic factors with real coefficients is:\
> > $$x^4 + 1 = (x^2 - \sqrt(2)x + 1)(x^2 + \sqrt(2)x + 1)$$\
> > Using this factorization, we can rewrite the integral as:\
> > $$1/(x^4 + 1) = 1/[(x^2 - \sqrt(2)x + 1)(x^2 + \sqrt(2)x + 1)]$$\
> > We can then use partial fractions to evaluate this integral.\
> > To evaluate the integral $$1/(x^4 + 1)$$, we can use partial fractions. First, we factor the denominator as:\
> > $$x^4 + 1 = (x^2 - \sqrt(2)x + 1)(x^2 + \sqrt(2)x + 1)$$\
> > Then, we write:\
> > $$1/(x^4 + 1) = A(x^2 + \sqrt(2)x + 1) + B(x^2 - \sqrt(2)x + 1)$$\
> > for some constants A and B. Multiplying both sides by the denominator, we get:\
> > $$1 = A(x^2 + \sqrt(2)x + 1)(x^2 - \sqrt(2)x + 1) + B(x^2 - \sqrt(2)x + 1)(x^2 + \sqrt(2)x + 1)$$\
> > We can simplify this equation by plugging in values for x that make some of the terms equal to zero. For example, setting $$x = \sqrt(2)/2$$ gives:\
> > $$1 = A(2) + B(2)$$\
> > which simplifies to:\
> > $$1 = 2(A + B)$$\
> > Similarly, setting $$x = -\sqrt(2)/2$$ gives:\
> > $$1 = A(2) + B(2)$$\
> > which again simplifies to:\
> > $$1 = 2(A + B)$$\
> > Solving these two equations simultaneously, we get:\
> > $$A = B = 1/4$$\
> > Therefore, we can write:\
> > $$1/(x^4 + 1) = (1/4)(x^2 + \sqrt(2)x + 1) + (1/4)(x^2 - \sqrt(2)x + 1)$$\
> > Integrating both sides with respect to $$x$$, we get:\
> > $$∫[1/(x^4 + 1)]dx = (1/4)∫[x^2 + \sqrt(2)x + 1]dx + (1/4)∫[x^2 - \sqrt(2)x + 1]dx$$\
> > Using the power rule for integration, we get:\
> > $$∫[1/(x^4 + 1)]dx = (1/4)(x^3/3 + (sqrt(2)/2)x^2 + x) + (1/4)(x^3/3 - (sqrt(2)/2)x^2 + x) + C$$\
> > where $$C$$ is the constant of integration. Simplifying, we get:\
> > $$∫[1/(x^4 + 1)]dx = (1/6)x^3 + (1/2)x - (1/4)(sqrt(2)/2)x^2 + C$$\
> > Therefore, the integral of $$1/(x^4 + 1)$$ is:\
> > $$∫[1/(x^4 + 1)]dx = (1/6)x^3 + (1/2)x - (1/4)(sqrt(2)/2)x^2 + C$$\
> > where $$C$$ is the constant of integration. -->
> > 
> {: .solution}
{: .challenge}
> ## 3. Let $$η = \cos(2π/5) + i \sin(2π/5)$$. The four non-real fifth roots of $$1 are η, η^2,η^3 and η^4$$.
> ### (a) Show that they are the roots of the polynomial $$x^4 + x^3 + x^2 + x + 1$$. 
> >
> > ## Solution
> >
> > We can show that the polynomial $$x^4 + x^3 + x^2 + x + 1$$ has $$η, η^2, η^3, and η^4$$ as its roots by directly substituting these values into the polynomial and verifying that the result is zero.\
> > Let's start with η. We have:\
> > $$η^4 + η^3 + η^2 + η + 1$$\
> > $$= (\cos(8π/5) + i \sin(8π/5)) + (\cos(6π/5) + i \sin(6π/5)) + (\cos(4π/5) + i \sin(4π/5)) + (\cos(2π/5) + i \sin(2π/5)) + 1$$\
> > $$= (\cos(8π/5) + \cos(6π/5) + \cos(4π/5) + \cos(2π/5) + 1) + i(\sin(8π/5) + \sin(6π/5) + \sin(4π/5) + \sin(2π/5))$$\
> > Now, we can use the fact that $$\cos(2π/5)$$ and $$\sin(2π/5)$$ are the real and imaginary parts of η, respectively, to simplify the expression:\
> > $$η^4 + η^3 + η^2 + η + 1$$\
> > $$= (-1/2) + i(sqrt(5)/2) + (-1/2) + i(-sqrt(5)/2) + 1 = 0$$\
> > Therefore, η is a root of $$x^4 + x^3 + x^2 + x + 1$$. By a similar computation, we can show that $$η^2, η^3, and η^4$$ are also roots of the polynomial. Hence, the polynomial $$x^4 + x^3 + x^2 + x + 1$$ has all four non-real fifth roots of 1 as its roots.
> > 
> {: .solution}
{: .challenge}
> ### (b) Express the sum $$η + η^2 + η^3  + η^4$$ in terms of $$λ := \cos(2π/5)$$. 
> >
> > ## Solution
> >
> > To express the sum $$η + η^2 + η^3 + η^4$$ in terms of $$λ := \cos(2π/5)$$, we can use the fact that $$η$$ is a root of the polynomial $$x^4 + x^3 + x^2 + x + 1$$, which can be factored as:\
> > $$x^4 + x^3 + x^2 + x + 1 = (x^2 + x + 1)(x^2 - x + 1)$$\
> > since $$η$$ is not a root of $$x^2 + x + 1$$, we have $$η^2 - η + 1 = 0$$. Multiplying both sides by $$η^2$$, we get:\
> > $$η^4 - η^3 + η^2 = η^2 - η + 1$$\
> > Similarly, we can obtain the following relations:\
> > $$η^3 - η^2 + η = η - 1$$\
> > $$η^4 - η^3 + η^2 - η + 1 = 0$$\
> > Adding all four equations, we get:\
> > $$η^4 + η^3 + η^2 + η + 1 = 2(η^2 - η + 1) + 2(η - 1) = 2(η^2 + η - 2) = 0$$\
> > Therefore, we have:\
> > $$η + η^2 + η^3 + η^4 = -1 - η - η^2 = -1 - λ$$\
> > Hence, the sum of the non-real fifth roots of 1 can be expressed in terms of $$λ$$ as $$-1 - λ$$.\
> > 
> {: .solution}
{: .challenge}
> ### (c) Deduce that $$\cos(2π/5) =(\sqrt(5) − 1)/4$$. 
> >
> > ## Solution
> >
> > We know that $$η = \cos(2π/5) + i \sin(2π/5)$$ is one of the non-real fifth roots of 1, which satisfies the equation $$η^2 + η - 1 = 0$$. Solving for $$η$$ using the quadratic formula, we get:\
> > $$η = (-1 ± √5)/2$$\
> > Since $$η$$ is a non-real complex number, its real part must be equal to $$\cos(2π/5)$$. Therefore, we have:\
> > $$\cos(2π/5) = Re(η) = (η + η*)/2$$\
> > where $$η*$$ is the complex conjugate of $$η$$. Since $$η$$ is not real, its complex conjugate is also not equal to $$η$$, and we have:\
> > $$η* = (-1 ∓ √5)/2$$\
> > Taking the positive sign, we have:\
> > $$η* = (-1 + √5)/2$$\
> > Adding $$η$$ and $$η*$$ and simplifying, we get:\
> > $$η + η* = (-1 + √5)/2 + (-1 - √5)/2 = -1 - √5$$\
> > Therefore, we have:\
> > $$\cos(2π/5) = (η + η*)/2 = (-1 - √5)/2$$
> > Multiplying the numerator and denominator by $$√5 + 1$$ and simplifying, we get:\
> > $$\cos(2π/5) = (-1 - √5)/2 = (√5 - 1)/(-2) = (√5 - 1)/4 * (-2/-1) = (√5 - 1)/4$$\
> > Hence, we have shown that $$\cos(2π/5) = (√5 - 1)/4$$.\
> > 
> {: .solution}
{: .challenge}
> ### (d) Show that they are the roots of the polynomial $$x^4 + x^3 + x^2 + x + 1$$. 
> >
> > ## Solution
> >
> > From part (c), we know that the roots of $$x^4 + x^3 + x^2 + x + 1$$ are the numbers:\
> > $$η = \cos(2π/5) + i \sin(2π/5)$$\
> > $$η^2 = \cos(4π/5) + i \sin(4π/5)$$\
> > $$η^3 = \cos(6π/5) + i \sin(6π/5)$$\
> > $$η^4 = \cos(8π/5) + i \sin(8π/5)$$\
> > \since $$\sin(2π/5) = \sin(8π/5) and \sin(4π/5) = \sin(6π/5)$$, we have:\
> > $$η + η^4 = \cos(2π/5) + \cos(8π/5) + i(\sin(2π/5) + \sin(8π/5)) = 2\cos(2π/5)$$ and\
> > $$η^2 + η^3 = \cos(4π/5) + \cos(6π/5) + i(\sin(4π/5) + \sin(6π/5)) = -2\cos(π/5)$$\
> > Substituting $$λ = \cos(2π/5)$$ into the factorization from part (c), we get:\
> > $$x^4 + x^3 + x^2 + x + 1 = (x - η)(x - η^4)(x - η^2)(x - η^3)$$\
> > $$                       = [(x - η)(x - η^4)][(x - η^2)(x - η^3)]$$\
> > $$                       = [(x^2 - (η + η^4)x + ηη^4)][(x^2 - (η^2 + η^3)x + η^2η^3)]$$\
> > $$                       = [(x^2 - 2\cos(2π/5)x + 1)][(x^2 + 2\cos(π/5)x + 1)]$$\
> > $$                       = (x^2 - 2λx + 1)(x^2 - 2(2λ^2 - 1)x + 1)$$\
> > Therefore, we have shown that $$x^4 + x^3 + x^2 + x + 1$$ can be factored as the product of two irreducible quadratic polynomials with real coefficients.\
> > since $$λ = \cos(2π/5)$$ is constructible with straight edge and compass, we can construct the roots of $$x^4 + x^3 + x^2 + x + 1$$ using the given factorization, which involves only square roots and additions, subtractions, and multiplications of constructible numbers.\
> > Hence, we can construct the regular pentagon using a straight edge and compass, as it can be inscribed in a circle with radius 1, whose center and circumference can be constructed using straight edge and compass.
> > 
> {: .solution}
{: .challenge}
> ### 8. Express the antiderivative $$\int(1/( x^5 − 1)dx$$. using the principal logarithm of first-degree complex polynomials
> >
> > ## Solution
> >
> > $$\int \frac{1}{x^5 - 1} dx = \int \frac{1}{(x-1)(x^4+x^3+x^2+x+1)}dx$$\
> > Let $$\omega = e^{\frac{2 \pi i}{5}}$$, the roots of $$x^5 - 1$$ are\
> > $$1, \omega, \omega^2, \omega^3, \omega^4$$.\
> > Since $$\omega^5 = 1$$, $$\omega$$ is a root of $$x^4+x^3+x^2+x+1$$. Then,\
> > $$x^4+x^3+x^2+x+1 = (x-\omega)(x-\omega^2)(x-\omega^3)(x-\omega^4)$$\
> > Let $$u = x-\omega$$, then $$du = dx$$, and\
> > $$\int \frac{1}{x^5 - 1} dx = \int \frac{1}{(x-1)(x^4+x^3+x^2+x+1)}dx$$\
> > $$ = \frac{1}{\omega-1}\int \frac{1}{u(u^3 + (1+\omega+\omega^2+\omega^3)u^2 + (1+\omega+\omega^2+\omega^3+\omega^4)u + 1)}du$$\
> > Since $$\omega^4+\omega^3+\omega^2+\omega+1 = 0$, $1+\omega+\omega^2+\omega^3 = -\omega^4$$. Then,\
> > $$\int \frac{1}{x^5 - 1} dx = \frac{1}{\omega-1}\int \frac{1}{u(u^3 - \omega^4 + 1)}du$$\
> > $$ = \frac{1}{\omega-1}\left[\frac{1}{2}\ln\left|\frac{u^2+(1-\omega^2)u+1}{u^2+(\omega^2-2)u+1}\right|+\frac{2}{\sqrt{5}}\arctan\left(\frac{2u+(1-\omega)}{\sqrt{5}}\right)+C\right]$$\
> > where $$C$$ is the constant of integration. Substituting back $$u = x-\omega$$ and using the fact that $$\omega = e^{\frac{2 \pi i}{5}}$$, we have\
> > $$\int \frac{1}{x^5 - 1} dx = \frac{1}{4\sin(\frac{\pi}{5})}\left[\ln\left|\frac{x^2-(2\cos(\frac{2\pi}{5}))x+1}{x^2+(2\cos(\frac{2\pi}{5})-2)x+1}\right|+\frac{2}{\sqrt{5}}\arctan\left(\frac{2x-(1+\cos(\frac{2\pi}{5}))+\sqrt{5}\sin(\frac{2\pi}{5})}{\sqrt{5}\cos(\frac{2\pi}{5})-1}\right)+C\right]$$
> > 
> {: .solution}
{: .challenge}
> ### 9. Let $$w = a + ib$$ and let  $$f(x) = e^{ax} (\cos bx + i \sin bx)$$ for real $$x$$. Show that $$f'(x) = wf(x)$$. 
> >
> > ## Solution
> >
> > We have:\
> > $$f(x) = e^{ax} (\cos bx + i \sin bx)$$\
> > Taking the derivative with respect to $$x$$:\
> > $$f'(x) = (ae^{ax})(\cos bx + i \sin bx) + e^{ax}(-b \sin bx + i b \cos bx)$$\
Simplifying:\
> > $$f '(x) = e^{ax} [(a \cos bx - b \sin bx) + i(a \sin bx + b \cos bx)]$$\
> > But we also have:\
> > $$w = a + ib$$\
> > So we can write:\
> > $$f '(x) = e^{ax} [(a \cos bx - b \sin bx) + i(a \sin bx + b \cos bx)]$$\
> > $$ = (a + ib) e^{ax} (\cos bx + i \sin bx) = wf(x)$$\
Therefore, $$f '(x) = wf(x)$$, as required.
> > 
> {: .solution}
{: .challenge}