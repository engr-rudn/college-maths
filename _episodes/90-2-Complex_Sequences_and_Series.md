---
title:  Complex Sequences and Series

questions:
- ""

objectives:
- ""
---

## 10.1 The Limit of a Complex Sequence

Let $$(z_n)_{n=1}^{\infty}$$ be a sequence of complex numbers and let w be a complex number.

### Definition

The number w is said to be the limit of the sequence $$(z_n)_{n=1}^{\infty}$$ if the following condition is satisfied:
For every $$\epsilon > 0$$, there exists a natural number N, such that $$|z_n - w| < \epsilon$$ for all $$n \geq N$$.

Formally this definition is the same as that for convergence of real sequences; only that the absolute value is reinterpreted as the modulus of a complex number. A complex sequence $$(z_n)_{n=1}^{\infty}$$ is said to be convergent if there exists some w, such that $$lim_{n \to \infty} z_n = w$$. If there is no such w then the sequence is said to be divergent. We will not make any use of infinite limits in the complex realm.

$$
\begin{flushleft}
Let $z_n=a_n+b_ni$ and $w=s+ti$ where $a_n$, $b_n$, $s$, and $t$ are real numbers. That is, $a_n=\operatorname{Re} z_n$, $b_n=\operatorname{Im} z_n$, $s=\operatorname{Re} w$, and $t=\operatorname{Im} w$. By the rules for complex numbers listed in 9.1 we have:
\end{flushleft}

\begin{equation*}
|a_n-s| \leq |z_n-w| \quad \text{and} \quad |b_n-t| \leq |z_n-w|
\end{equation*}

\begin{flushleft}
so that if $\lim_{n\to\infty}z_n=w$ then:
\end{flushleft}

\begin{equation*}
\lim_{n\to\infty}a_n=s \quad \text{and} \quad \lim_{n\to\infty}b_n=t.
\end{equation*}

\begin{flushleft}
But the converse of this last statement is also true because:
\end{flushleft}

\begin{equation*}
|z_n-w|^2=|a_n-s|^2+|b_n-t|^2.
\end{equation*}

\begin{flushleft}
We have proved the following.
\end{flushleft}

\textbf{Proposition 10.1} A complex sequence $(z_n){n=1}^{\infty}$ satisfies $\lim{n\to\infty}z_n=w$ if and only if $\lim_{n\to\infty}\operatorname{Re} z_n=\operatorname{Re} w$ and $\lim_{n\to\infty}\operatorname{Im} z_n=\operatorname{Im} w$.

\begin{flushleft}
This also shows that if a complex sequence has a limit, then the limit is unique (because that is known for real sequences). Another important conclusion is as follows.
\end{flushleft}

\textbf{Proposition 10.2} Let $\lim_{n\to\infty}z_n=w$. Then $\lim_{n\to\infty}|z_n|=|w|$.

\begin{flushleft}
\textbf{Proof} It follows from the inequality $| |z| - |w| |\leq |z-w|$ stated in Proposition 9.2.
\end{flushleft}
$$
