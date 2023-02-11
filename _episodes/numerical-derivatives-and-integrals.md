---
layout: default
---

# More on Limits and using calculator for Numerical Derivatives and Integrals

## Learning Targets

You should be able to
- [ ] Evaluate limits algebraically and numerically, with and without calculator
- [ ] Numerically calculate derivatives and integrals using nDeriv and fnInt on calculator

## Concepts / Definitions

### Theorem for a Limit

$$\lim_{x \to a} f(x) = L \quad iff \quad \lim_{x \to a^-} f(x) = L = \lim_{x \to a^+} f(x)$$

### Theorem

$$\lim_{x \to \infty} \frac{\sin{x}}{x} = 1 \qquad \lim_{x \to 0} \frac{\cos{x}-1}{x} = 0$$

### Derivative and Integral buttons

From Graphing Screen:<br>
Graph $f(x)$, $2^{nd}$ TRACE (calc), 6 deriv, 7 integral<br>
From Main Screen:<br>
MATH, 8nDeriv$(f(x), x, x_a)$, 9fnIn$t(f(x), x, a, b)$

Note: Technically the theorem is based on real numbers, we do include infinity as a possible answer to give more information about answer.

### Theorem

If $r > 0$ is a rational number, then
$$\lim_{x \to \pm \infty} \frac{1}{x^r} = 0$$

Suppose we want to answer a limit question, and *when we "plug in" the limit value*, this is what we get. So, what would they equal?

$$
\begin{matrix}
    \frac{0}{0}&\frac{\infty}{\infty}&0^{infty}\\
    \frac{some\ number}{\infty}&\infty - \infty&0^0\\
    \frac{\infty}{some\ number}&(0)(\infty)&1^{infty}\\
    \frac{some\ number}{0}\\
\end{matrix}
$$

$$
\begin{matrix}
    indeterminate&indeterminate&???\\
    0&indeterminate&indeterminate\\
    \pm\infty&indeterminate&indeterminate\\
    indeterminate\\
\end{matrix}
$$

undefined: we don't know<br>
indeterminute: we can find out
