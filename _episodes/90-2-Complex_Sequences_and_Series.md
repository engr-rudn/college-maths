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
\begin{align*}
&\text{Let } z_n = a_n + b_ni \text{ and } w = s+ti \text{ where } a_n, b_n, s, t \text{ are real numbers.} \
&\text{That is, } a_n = \operatorname{Re}z_n, b_n = \operatorname{Im}z_n, s = \operatorname{Re}w, \text{ and } t = \operatorname{Im}w. \
&\text{By the rules for complex numbers listed in 9.1 we have} \
&|a_n-s| \leq |z_n-w| \text{ and } |b_n-t| \leq |z_n-w| \
&\text{so that if } \lim_{n \to \infty} z_n = w \text{ then} \
&\lim_{n \to \infty} a_n = s \text{ and } \lim_{n \to \infty} b_n = t. \
&\text{But the converse of this last statement is also true because} \
&|z_n-w|^2 = |a_n-s|^2 + |b_n-t|^2. \
&\text{We have proved the following.} \
&\textbf{Proposition 10.1:} \text{ A complex sequence } (z_n){n=1}^{\infty} \text{ satisfies } \lim{n \to \infty} z_n = w \text{ if and only} \
&\text{if } \lim_{n \to \infty} \operatorname{Re}z_n = \operatorname{Re}w \text{ and } \lim_{n \to \infty} \operatorname{Im}z_n = \operatorname{Im}w. \
&\text{This also shows that if a complex sequence has a limit, then the limit is unique} \
&\text{(because that is known for real sequences). Another important conclusion is as follows.} \
&\textbf{Proposition 10.2:} \text{ Let } \lim_{n \to \infty} z_n = w. \text{ Then } \lim_{n \to \infty} |z_n| = |w|. \
&\textbf{Proof:} \text{ It follows from the inequality } | |z| - |w| | \leq |z-w| \text{ stated in Proposition 9.2.} \
&\text{Cauchy’s principle of convergence for real sequences (Proposition 3.12) extends almost without change to complex sequences.} \
&\textbf{Proposition 10.3: } \text{(Cauchy’s convergence principle) A complex sequence } (z_n){n=1}^{\infty} \text{ is convergent if and only} \
&\text{if it satisfies Cauchy’s condition: for each } \epsilon > 0 \text{ there exists } N \text{ such that } \
&|z_n-z_m| < \epsilon \text{ for all } n, m \text{ that satisfy } n \geq N \text{ and } m \geq N. \
&\textbf{Proof: } \text{Let } a_n = \operatorname{Re}z_n \text{ and } b_n = \operatorname{Im}z_n. \text{Since } (z_n){n}
$$
$$
\begin{align*}
\text{Let } z_n &= a_n + b_n i \text{ and } w = s + ti \text{ where } a_n, b_n, s, t \text{ are real numbers.} \
\text{That is, } a_n &= \operatorname{Re} z_n, \quad b_n = \operatorname{Im} z_n, \quad s = \operatorname{Re} w, \quad t = \operatorname{Im} w. \
\text{By the rules for complex numbers listed in 9.1 we have } \
|a_n - s| &\leq |z_n - w| \quad \text{and} \quad |b_n - t| \leq |z_n - w|, \
\text{so that if } \lim_{n \to \infty} z_n &= w \text{ then } \lim_{n \to \infty} a_n = s \text{ and } \lim_{n \to \infty} b_n = t. \
\text{But the converse of this last statement is also true because } \
|z_n - w|^2 &= |a_n - s|^2 + |b_n - t|^2. \
\text{We have proved the following.} \
\textbf{Proposition 10.1} \quad \text{A complex sequence } (z_n){n=1}^{\infty} \text{ satisfies } \lim{n \to \infty} z_n = w \text{ if and only if } \lim_{n \to \infty} \operatorname{Re} z_n = \operatorname{Re} w \text{ and } \lim_{n \to \infty} \operatorname{Im} z_n = \operatorname{Im} w. \
\text{This also shows that if a complex sequence has a limit, then the limit is unique (because that is known for real sequences). Another important conclusion is as follows.} \
\textbf{Proposition 10.2} \quad \text{Let } \lim_{n \to \infty} z_n = w. \text{ Then } \lim_{n \to \infty} |z_n| = |w|. \
\textbf{Proof} \quad \text{It follows from the inequality } | |z| - |w| | \leq |z - w| \text{ stated in Proposition 9.2.} \
\text{} \
\text{Cauchy's principle of convergence for real sequences (Proposition 3.12) extends almost without change to complex sequences.} \
\textbf{Proposition 10.3} \quad \text{(Cauchy’s convergence principle) A complex sequence } (z_n){n=1}^{\infty} \text{ is convergent if and only if it satisfies Cauchy’s condition: for each } \epsilon > 0 \
&\text{there exists } N \text{ such that } |z_n - z_m| < \epsilon \text{ for all } n \text{ and } m \text{ that satisfy } n \geq N \text{ and } m \geq N. \
\textbf{Proof} \quad \text{Let } a_n = \operatorname{Re} z_n \text{ and } b_n = \operatorname{Im} z_n. \
&\text{Since } (z_n){n=1}
$$
$$
\begin{aligned}
& \text{Let } z_n = a_n + b_n i \text{ and } w = s + t i \text{ where } a_n, b_n, s, t \text{ are real numbers.} \
& \text{That is, } a_n = \operatorname{Re} z_n, b_n = \operatorname{Im} z_n, s = \operatorname{Re} w, \text{ and } t = \operatorname{Im} w. \
& \text{By the rules for complex numbers listed in 9.1 we have} \
& \qquad \left| a_n - s \right| \leq \left| z_n - w \right| \text{ and } \left| b_n - t \right| \leq \left| z_n - w \right|, \
& \qquad \text{so that if } \lim_{n \to \infty} z_n = w \text{ then } \lim_{n \to \infty} a_n = s \text{ and } \lim_{n \to \infty} b_n = t. \
& \text{But the converse of this last statement is also true because } \left| z_n - w \right|^2 = \left| a_n - s \right|^2 + \left| b_n - t \right|^2. \
& \text{We have proved the following.} \
& \textbf{Proposition 10.1 } \text{A complex sequence } (z_n){n=1}^{\infty} \text{ satisfies } \lim{n \to \infty} z_n = w \text{ if and only if } \lim_{n \to \infty} \operatorname{Re} z_n = \operatorname{Re} w \text{ and } \lim_{n \to \infty} \operatorname{Im} z_n = \operatorname{Im} w. \
& \text{This also shows that if a complex sequence has a limit, then the limit is unique (because that is known for real sequences).} \
& \textbf{Proposition 10.2 } \text{Let } \lim_{n \to \infty} z_n = w. \text{ Then } \lim_{n \to \infty} \left| z_n \right| = \left| w \right|. \
& \textbf{Proof } \text{It follows from the inequality } \left| \left| z \right| - \left| w \right| \right| \leq \left| z - w \right| \text{ stated in Proposition 9.2.} \
& \
& \text{Cauchy’s principle of convergence for real sequences (Proposition 3.12) extends almost without change to complex sequences.} \
& \textbf{Proposition 10.3 } \text{(Cauchy’s convergence principle)} \text{A complex sequence } (z_n)_{n=1}^{\infty} \text{ is convergent if and only if it satisfies Cauchy’s condition:} \
& \qquad \text{for each } \epsilon > 0 \text{ there exists } N \text{, such that } \left| z_n - z_m \right| < \epsilon \text{ for all } n, m \text{ that satisfy } n \geq N \text{}
$$
$$
\begin{aligned}
&\text{Let } z_n = a_n + b_ni \text{ and } w = s+ti \text{ where } a_n, b_n, s, t \text{ are real numbers.} \
&\text{That is, } a_n = \operatorname{Re}(z_n), b_n = \operatorname{Im}(z_n), s = \operatorname{Re}(w), t = \operatorname{Im}(w). \
&\text{By the rules for complex numbers listed in 9.1 we have } \
&\qquad |a_n-s| \leq |z_n-w| \quad \text{and} \quad |b_n-t| \leq |z_n-w|, \
&\text{so that if } \lim_{n \to \infty} z_n = w \text{ then} \
&\qquad \lim_{n \to \infty} a_n = s \quad \text{and} \quad \lim_{n \to \infty} b_n = t. \
&\text{But the converse of this last statement is also true because} \
&\qquad |z_n-w|^2 = |a_n-s|^2 + |b_n-t|^2. \
&\text{We have proved the following.} \
&\textbf{Proposition 10.1 } \text{A complex sequence } (z_n){n=1}^{\infty} \text{ satisfies } \lim{n \to \infty} z_n = w \
&\qquad \text{if and only if} \lim_{n \to \infty} \operatorname{Re}(z_n) = \operatorname{Re}(w) \text{ and } \lim_{n \to \infty} \operatorname{Im}(z_n) = \operatorname{Im}(w). \
&\text{This also shows that if a complex sequence has a limit, then the limit is unique} \
&\qquad (\text{because that is known for real sequences}). \text{Another important conclusion is as follows.} \
&\textbf{Proposition 10.2 } \text{Let } \lim_{n \to \infty} z_n = w. \text{ Then } \lim_{n \to \infty} |z_n| = |w|. \
&\textbf{Proof } \text{It follows from the inequality } | |z|-|w| | \leq |z-w| \text{ stated in Proposition 9.2.} \
& \
&\text{Cauchy’s principle of convergence for real sequences (Proposition 3.12) extends} \
&\qquad \text{almost without change to complex sequences.} \
&\textbf{Proposition 10.3 } \text{(Cauchy’s convergence principle) A complex sequence } (z_n)_{n=1}^{\infty} \text{ is convergent} \
&\qquad \text{if and only if it satisfies Cauchy’s condition: for each } \epsilon > 0 \text{ there exists} \
&\qquad N \text{ such that } |z_n - z_m| < \epsilon \text{ for all } n, m \text{ that satisfy } n \geq N \text{ and } m \geq N. \
&\textbf{Proof } \text{Let } a_n = \operatorname{}$$
