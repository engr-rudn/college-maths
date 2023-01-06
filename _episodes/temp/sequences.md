---
layout: default
---

# Sequences

## Learning Targets

You should be able to
- [ ] Evaluate and write sequences as an explicit rule and as a recursive rule
- [ ] Determine if a sequences converges or diverges

## Concepts / Definitions

A **sequence** is an ordered set of numbers; it is a function with *sequential natural numbers as the domain* and the terms of the sequence as the range.

Sequence values (terms or output numbers) are written by using subscripts. The first term is $a_1$, the second term is $a_2$, and the $n$th term is $a_n$.

An explicit formula would have the form $a_n = \frac{3n}{n+1}$

Sequences can be finite or infinite.<br>
Let $a_n$ be a sequence of real numbers, and let $L$ be a finite number. A sequence will **converge** if
$$\lim_{x \to \infty} a_n = L$$
If the sequence is infinite or nonexistant, the sequence diverges.

A **recursive formula** is a rule in which one or more previous terms are used to generate the next term.

An **arithmetic sequence** has an explicit rule or form $a_n = a_1 + (n-1)d$, where $d$ is the *common difference* between terms.<br>
Recursive Rule: $a_n = a_{n-1} * r$ for $n \geq 2$

A **geometric sequence** has an explicit rule or form $a_n = a_1 r^{n-1}$, where $r$ is the *common ratio* between terms.<br>
Recursive Rule: $a_n = a_{n-1} * r$ for $n \geq 2$

### Fibonacci Sequence

$$ a_1 = 1, \quad a_2 = 2, \quad a_n a_{n-2} + a_{n-1}$$

![Fibonacci Sequence](../assets/precalculus/sequences_1.jpg)
![Golden Ratio](../assets/precalculus/sequences_2.svg)

As the spiral continues, the ratios of the numbers approach a number called the **Golden Ratio**.

$$\frac{a+b}{a} = \frac{1+\sqrt{5}}{2} \approx 1.6180$$

### Examples

#### Example 1
Write an explicit rule for $5, -7, 9, 11, 13, ...$

#### Example 2
Determine if the following sequence converges or diverges. $2, \frac 32, \frac 43, \frac 54, ...$

#### Example 3
Write an explicit rule for the following sequence. $3, 9, 17, 27, 39$

#### Example 4
Write an explicit rule for a geometric sequence given that $a_3 = 54$, and $a_6 = 2$

## Exercises
Calculator okay, find with algebra.
  1. Determine if the following sequences converge or diverge.
     1. $\frac 12, \frac 14, \frac 18, \frac{1}{16}, ...$
     2. $-1,1,-1,1,-1,...$
     3. $a_n = 1.3^{n-1}$
     4. $a_n = \frac{1-2n}{n+1}$
  2. Write an explicit and recursive rule for $-5, -2, 1, 4, ...$
  3. Write an explicit rule for $\frac e2, \frac{e^2}{3}, \frac{e^3}{4}, ...$
  4. Write an explicit rule for $\frac{-6}{5}, \frac{7}{15},\frac{-8}{45},\frac{1}{15},\frac{-2}{81}, ...$
  5. Write an explicit rule for $2, 7, 16, 29, 46$
  6. Write an explicit rule $1\frac 12, 3\frac 14, 5\frac 16, 7\frac 18, ...$
  7. Given the ninth term is -5 and the fifteenth term is 31, write an arithmetic explicit rule.
  8. Given $a_4 = 2$, and $a_7 = \frac{54}{125}$, write a geometric explicit rule.
  9. Find $x$ so that $x$, $x+2$, and $x+3$ are consecutive terms of a geometric sequence.
  10. Suppose that you have been hired at an annual salary of $30,000 and expect to receive annual increases of 3%. What will your salary be when you begin your fifth year?
