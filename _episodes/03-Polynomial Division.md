---
title: Polynomial Long Division and Synthetic Division
questions:
- "What basic?"
- "How can ?"
- "How do ?"
- "Can I ?"
objectives:
- "???"
- "???"
---
# Polynomial Long Division and Synthetic Division

* In any division problem in the form $$\frac{a}{b} = c$$, $$a$$ is the **dividend** and $$b$$ is the **divisor**
* There are two types of polynomial division:
	* Long Division (slow but always works)
	* Synthetic Division (fast but works for only specific types of questions)
* We typically prefer to use synthetic division whenever we can, and use long division if a problem can't be solved with synthetic division

## Long Division

Using long division, we can solve any division problem involving polynomials. Whenever we need to divide polynomials, and the divider isn't a factor of the dividend, we can use long division.

For instance, suppose we want to solve the expression $$(x^3+4x^2-3x-12) \div (x^2-3)$$ using long division. Let's put it into long division form first:

$$
\begin{array}{cc}
x^2-3 & {
\begin{array}{|c}
\hline
x^3+4x^2-3x-12 \\
\end{array}
}
\end{array}
$$

The first thing we must do is to put the dividend and divisor in *expanded polynomial form*. This means that they are in the form $$a_nx^n+a_{n-1}x^{n-1}+\dots + a_0$$ - if the polynomial is of degree 3 for instance, it must have:

- An $$x^3$$ term (like $$5x^3$$)
- An $$x^2$$ term (like $$2x^2$$)
- An $$x^1$$ term (like $$3x$$ which is the same as $$3x^1$$)
- An $$x^0$$ term, also called a constant term (like $$15$$, because it's the same as $$15x^0$$)

The same goes for every polynomial of degree $$n$$ - they must have at least $$n+1$$ ordered terms. A 4th-degree polynomial must have 5 ordered terms, a 5th-degree polynomial must have 6, a 6th-degree one 7, and so on.

Let's examine our divisor $$x^2-3$$ first. We notice that it is a 2nd-degree polynomial. That means it _should_ have:

- An $$x^2$$ term,
- An $$x^1$$ term,
- And an $$x^0$$ term

We observe that it has an $$x^2$$ term, and an $$x^0$$ term, but no $$x^1$$ term. So, we can set it to standard form by adding a "zeroed" $$x^1$$ term, like so:

$$
x^2 - 3 \rightarrow x^2 + 0x^1 - 3
$$

Which simplifies to:

$$
x^2 + 0x - 3
$$

Let's now check our dividend. Our dividend is already in complete polynomial form and it has all of its terms in order already, so we don't need to repeat the same process.

Now we can begin long division:

$$
\begin{array}{cc}
x^2 + 0x -3 & {
\begin{array}{|c}
\hline
x^3+4x^2-3x-12 \\
\end{array}
}
\end{array}
$$

The first step is to find a term that our divisor can go into. We know that $$x^2 + 0x -3$$ would need a polynomial of at least 3 terms to go into. So we could rewrite our long division as this:

$$
\begin{array}{cc}
x^2 + 0x -3 & {
\begin{array}{|c}
\hline
\underline{x^3+4x^2-3x}-12 \\
\end{array}
}
\end{array}
$$

How many times would $$x^2 + 0x -3$$ go into $$x^3+4x^2-3x$$? The trick is to take the first term of $$x^3+4x^2-3x$$, which is $$x^3$$, and divide it by the first term of $$x^2 + 0x -3$$, which is $$x^2$$. Since $$\frac{x^3}{x^2} = x$$, that's our answer! So let's add $$x$$ to the top-right of the division bar:

$$
\begin{array}{ll}
% 2 left-aligned rows

% Top row
{
\begin{array}{rrrrrrrr}
&&&&&&& x
\end{array}
} \\

% Bottom row
{
\begin{array}{lr}
x^2 + 0x -3 & {
\begin{array}{|c}
\hline
\underline{x^3+4x^2-3x}-12 \\
\end{array}
}
\end{array}
}

% End
\end{array}
$$

Now, we will multiply $$x \cdot x^2 + 0x -3$$, which gives us $$x^3 + 0x^2 - 3x$$. Let's move that to our long division:

$$
\begin{array}{lll}
% 3 left-aligned rows

% Top row
{
\begin{array}{rrrrrrrr}
&&&&&&& x
\end{array}
} \\

% Middle row
{
\begin{array}{lr}
x^2 + 0x -3 & {
\begin{array}{|c}
\hline
\underline{x^3+4x^2-3x}-12 \\
\end{array}
}
\end{array}
} \\

% Bottom row
{
\begin{array}{rrrrrrrr}
&&&& & - & x^3-0x^2 -3x \\
\hline
\end{array}
}

% End
\end{array}
$$

Now, we just need to do the subtraction:

$$
\begin{array}{llll}
% 3 left-aligned rows

% Top row
{
\begin{array}{rrrrrrrr}
&&&&&&& x
\end{array}
} \\

% Middle row
{
\begin{array}{lr}
x^2 + 0x -3 & {
\begin{array}{|c}
\hline
\underline{x^3+4x^2-3x}-12 \\
\end{array}
}
\end{array}
} \\

% Lower middle row
{
\begin{array}{rrrrrrrr}
&&&& & - & x^3-0x^2 -3x \\
\hline
\end{array}
} \\

% Bottom row
{
\begin{array}{rrrrrrrrrr}
&&&&&&&&& 4x^2 +0x \\
\end{array}
}

% End
\end{array}
$$

* There are also some more difficult cases involving long division
  * For instance, let's try to do $$\left(6 x^{3}+10 x^{2}+x+8\right) \div\left(2 x^{2}+1\right)$$
  * If we start...we realize that we can't do it! Because we can't do $$10x^2-3$$!
  * So instead, we have to convert our original equation into the form $$\left(6 x^{3}+10 x^{2}+x+8\right) \div\left(2 x^{2}+0+1\right)$$
  * This allows us to...

## Synthetic Division

![](https://www.chilimath.com/wp-content/uploads/2017/02/p1_animated_v2.gif)

* Synthetic division works only for divisors of the form $$(x-k)$$ or $$(x+k)$$ - you cannot use synthetic division with a divisor with exponents such as $$(x^2-3)$$
  * For instance, let's try to do this question with synthetic division:
  * We must first convert our divisor $$(x+3)$$ to the form $$(x-c)$$ - $$(x+3)$$ is equivalent to $$(x-(-3))$$, so $$c = 3$$
  * We must also remember that if the exponents of our terms are _not consecutive_ (e.g. $$x^5 - 3x^2 -x$$ is not consecutive because we don't have a $$x^4$$ term between $$x^5$$ and $$x^3$$), we must "add" 0 raised to that exponent
  * So in this case it would be $$x^5 - 0x^4 - 3x^2 -x$$
  * (Fix this LaTeX matrix to look like the L-shape this should be in)

$$
\begin{array}{r|rrrr}
-3 & 4 & 7 & -13 & -3 \\
& & \downarrow & -12 & 15 & -6 \\
\hline & 4 & -5 & 2 & -9 &
\end{array}
$$


### Using Synthetic Division to prove a solution to a polynomial

### Uses of the remainder in Synthetic Division

The remainder found through synthetic division tells us that:
* Something
* Something
* Something

### The Remainder Theorem