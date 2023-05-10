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

Let $$z_n=a_n+b_ni$$ and $$w=s+ti$$ where $$a_n$$, $$b_n$$, $$s$$, and $$t$$ are real numbers.\
That is, $$a_n=\operatorname{Re} z_n$$,\
 $$b_n=\operatorname{Im} z_n$$,\
  $$s=\operatorname{Re} w$$, and\
   $$t=\operatorname{Im} w$$.\
By the rules for complex numbers listed in 9.1 we have:

$$
|a_n-s| \leq |z_n-w| \quad \text{and} \quad |b_n-t| \leq |z_n-w|
$$

so that if $$\lim_{n\to\infty}z_n=w$$ then:

$$
\lim_{n\to\infty}a_n=s \quad \text{and} \quad \lim_{n\to\infty}b_n=t.
$$

But the converse of this last statement is also true because:

$$
|z_n-w|^2=|a_n-s|^2+|b_n-t|^2.
$$

We have proved the following.\
**Proposition 10.1**
 A complex sequence $$(z_n)_{n=1}^{\infty}$$\
  satisfies $$\lim_{n\to\infty}z_n=w$$\
   if and only if $$\lim_{n\to\infty}\operatorname{Re} z_n=\operatorname{Re}\
    w$$ and $$\lim_{n\to\infty}\operatorname{Im} z_n=\operatorname{Im} w$$.

This also shows that if a complex sequence has a limit, then the limit is unique (because that is known for real sequences).\
 Another important conclusion is as follows.

**Proposition 10.2**\
 Let $$\lim_{n\to\infty}z_n=w$$. Then $$\lim_{n\to\infty}|z_n|=|w|$$.

**Proof**\
 It follows from the inequality $$||z| - |w||\leq |z-w|$$ stated in Proposition 9.2.

**Cauchy's principle of convergence for real sequences (Proposition 3.12)**\ extends almost without change to complex sequences.\

**Proposition 10.3**\
 (Cauchy's convergence principle) A complex sequence $$(z_n)_{n=1}^{\infty}$$
  is convergent if and only if it satisfies Cauchy's condition:\
   for each $$\epsilon > 0$$ there exists $$N$$, such that $$|z_n - z_m| < \epsilon$$ for all $$n$$ and $$m$$ that satisfy $$n \geq N$$ and $$m \geq N$$.

**Proof**\
Let $$a_n = \Re(z_n)$$ and $$b_n = \Im(z_n)$$.\
 Since $$(z_n)_{n=1}^{\infty}$$ is convergent if and only if $$(a_n)_{n=1}^{\infty}$$ and $$(b_n)_{n=1}^{\infty}$$ are both convergent real sequences, it suffices to show that\
  $$(z_n)_{n=1}^{\infty}$$\
   satisfies Cauchy's condition for complex sequences if and only if\
    $$(a_n)_{n=1}^{\infty}$$ and $$(b_n)_{n=1}^{\infty}$$\
     satisfy Cauchy's condition for real sequences.\
      But that is obvious in virtue of the inequalities (all of which appeared in Sect. 9.1):

$$
|a_n - a_m| \leq |z_n - z_m|
$$,\
 $$
 |b_n - b_m| \leq |z_n - z_m|
 $$, and\
  $$
  |z_n - z_m| \leq \sqrt{2} \max(|a_n - a_m|,\
   |b_n - b_m|)
   $$.
> ## Exercises 10.2.6 Test the following series for convergence. In each case determine whether the series is absolutely convergent, conditionally convergent or divergent.
> (a) $$\sum_{n=1}^{\infty}\frac{-1^n}{\sqrt{n}}$$
> > ## Solution
> >
> > We can test the convergence of the given series using the alternating series test, which states that if a series\
> > $$\sum_{n=1}^{\infty}(-1)^{n+1}b_n$$\
> > satisfies the conditions:\
> > - $$b_n > 0$$ for all $$n \in \mathbb{N}$$, and\
> > - $$b_{n+1} \leq b_n$$ for all $$n \in \mathbb{N}$$,\
> > then the series converges.\
> > In the given series, we have $$b_n = \frac{1}{\sqrt{n}}$$, which is always positive.\
> > Also, $$b_{n+1} = \frac{1}{\sqrt{n+1}} \leq \frac{1}{\sqrt{n}} = b_n$$ for all $$n \in \mathbb{N}$$.\
> > Therefore, the alternating series test applies, and we can conclude that the series converges.\
> > To determine whether the series is absolutely convergent or conditionally convergent, we need to consider the series\
> >  $$\sum_{n=1}^{\infty}\left|\frac{(-1)^n}{\sqrt{n}}\right| = \sum_{n=1}^{\infty}\frac{1}{\sqrt{n}}$$.\
> > This series diverges, since it is a $$p$$-series with\
> >  $$p=\frac{1}{2}$$, and $$p \leq 1$$.\
> > Therefore, the given series is not absolutely convergent, but it is conditionally convergent.
> {: .solution}
{: .challenge}
> (b) $$\sum_{n}{\infty}\frac{(-1^n)*n*(n+1)}{\(n+2)*(n+3)}$$
> > ## Solution
> >
> > $$
\begin{align*}
\sum_{n=1}^{\infty}\left|\frac{(n^2+n)}{(n+2)(n+3)}\right| &= \sum_{n=1}^{\infty}\frac{n^2+n}{(n+2)(n+3)} \
&= \sum_{n=1}^{\infty}\left(\frac{1}{n+3} - \frac{1}{n+2}\right) \
&= \sum_{n=4}^{\infty}\frac{1}{n} - \frac{1}{2} + \frac{1}{3}
\end{align*}
$$\
> > Since the terms of this series do not approach zero, the series diverges.\
> > Using the ratio test, we have:\
> > $$
\begin{align*}
\lim_{n\rightarrow \infty}\left|\frac{a_{n+1}}{a_n}\right| &= \lim_{n\rightarrow \infty}\frac{(n+1)^2+(n+1)}{(n+2)(n+3)}\frac{(n+2)(n+3)}{n^2+n} \
&= \lim_{n\rightarrow \infty}\frac{(n^2+2n+1+n+1)(n+2)}{(n^2+n)(n+4)} \
&= \lim_{n\rightarrow \infty}\frac{(n^2+3n+2)(n+2)}{(n^2+n)(n+4)} \
&= \lim_{n\rightarrow \infty}\frac{n^3+5n^2+8n+4}{n^3+5n^2+4n^2+4n} \
&= \lim_{n\rightarrow \infty}\frac{n^3+5n^2+8n+4}{n^3+9n^2+4n} \
&= 1
\end{align}
$$\
> > Since the limit is equal to 1, the ratio test is inconclusive.\
> > However, using the alternating series test, we can show that the series converges. We have:\
> > $$\frac{(n^2+n)}{(n+2)*((n+3)}>0 for all $$n \in \mathbb{N}$$,\
> > $$a_{n+1} \le a_{n} for all n \ge 1$$.\
> > Therefore, the series converges by the alternating series test.\
> > Since the series $$\sum_{n=1}^{\infty}\left|\frac{(n^2+n)}{(n+2)(n+3)}\right|$$ diverges,\
> >the original series\
> > $$\sum_{n=1}^{\infty}\frac{(-1)^nn*(n+1)}{(n+2)*(n+3)}$$\
> >  is conditionally convergent.\
> > $$\sum_{n=1}^{\infty}\frac{(-1)^nn(n+1)}{(n+2)(n+3)} = \sum_{n=1}^{\infty}\frac{(-1)^n(n^2+n)}{(n+2)*(n+3)}$$\
> > Let $$a_n = \frac{(n^2+n)}{(n+2)*(n+3)}$$. Then,\
> > $$\lim_{n\rightarrow \infty}\left|\frac{a_{n+1}}{a_n}\right| =\
> > $$\lim_{n\rightarrow \infty}\frac{(n+1)^2+(n+1)}{(n+3)(n+4)}\frac{(n+2)*(n+3)}{n^2+n}$$\
> > $$=\lim_{n\rightarrow \infty}\frac{(n^2+2n+1+n+1)(n+2)}{(n^2+n)(n+4)}$$ =\
> > $$\lim_{n\rightarrow \infty}\frac{(n^2+3n+2)(n+2)}{(n^2+n)(n+4)}$$\
> > $$=\lim_{n\rightarrow \infty}\frac{n^3+5n^2+8n+4}{n^3+5n^2+4n^2+4n}$$\
> > $$=\lim_{n\rightarrow \infty}\frac{n^3+5n^2+8n+4}{n^3+9n^2+4n} = 1$$\
> > Using the alternating series test, we can determine that the series is conditionally convergent.\
> > The absolute value series can be written as:\
> > $$\sum_{n=1}^{\infty}\left|\frac{(n^2+n)}{(n+2)(n+3)}\right| = \sum_{n=1}^{\infty}\frac{n^2+n}{(n+2)(n+3)}$$\
> > Using partial fractions, we can write:\
> > $$\frac{n^2+n}{(n+2)*(n+3)} = \frac{1}{n+3} - \frac{1}{n+2}$$
> {: .solution}
{: .challenge}
> (c) $$\sum_{n}{\infty}\frac{(-1^n)*n*(n+1)}{\(n+2)*(n+3)*(n+4)}$$
> > ## Solution
> >
> > We will use the alternating series test to show that the series converges. We have:
> > $$frac{(-1^n)*n*(n+1)}{\(n+2)*(n+3)*(n+4)}>0$$ for all $$n \in \mathbb{N}$$, and\
> > $$
\begin{align*}
\lim_{n\rightarrow \infty}\frac{n*(n+1)}{(n+2)(n+3)(n+4)} &= \lim_{n\rightarrow \infty}\frac{n*(n+1)}{(n+2)n(n+3)(n+4)/n} \
&= \lim_{n\rightarrow \infty}\frac{n(n+1)}{(n+2)n(n+3)*(n+4)}n \
&= \lim_{n\rightarrow \infty}\frac{n^2+n}{(n^4+9n^3+26n^2+24n)} \
&= \lim_{n\rightarrow \infty}\frac{1/n+1/n^3}{1+9/n+26/n^2+24/n^3} \
&= 0.
\end{align}
$$\
> > Therefore, the series\
> > $$\sum_{n=1}^{\infty}\frac{(-1)^nn(n+1)}{(n+2)(n+3)(n+4)}$$\
> >  converges by the alternating series test.\
> > To determine whether the series is absolutely convergent, we consider the series of absolute values:\
> > $$\sum_{n=1}^{\infty}\left|\frac{(-1)^nn*(n+1)}{(n+2)*(n+3)*(n+4)}\right|$$=\
> > $$\sum_{n=1}^{\infty}\frac{n*(n+1)}{(n+2)*(n+3)*(n+4)}$$\
> > Using partial fractions,\
> > $$\frac{n*(n+1)}{(n+2)*(n+3)*(n+4)}$$ = $$\frac{1}{2*(n+2)}-\frac{2}{(n+3)}+\frac{3}{2*(n+4)}\
> > Therefore,\
> > $$\sum_{n=1}^{\infty}\left|\frac{(-1)^nn*(n+1)}{(n+2)*(n+3)*(n+4)}\right|$$=\
> > $$\sum_{n=1}^{\infty}\frac{1}{2*(n+2)}-\frac{2}{(n+3)}+\frac{3}{2*(n+4)}$$\
> > We can rewrite this series as:\
> > $$-\frac{1}{4}-\frac{1}{5}+\frac{3}{8}-\frac{1}{6}-\frac{1}{7}+\frac{3}{4}-\frac{1}{8}-\frac{1}{9}+\frac{3}{12}- ...$$\
> > It can be observed that the series of absolute values does not converge. Hence, the original series is not absolutely convergent.\
> > Therefore, the original series $$\sum_{n=1}^{\infty}\frac{(-1)^nn(n+1)}{(n+2)(n+3)(n+4)}$$ is conditionally convergent.
> {: .solution}
{: .challenge}
<!-- > (d) $$\sum_{n=1}^{\infty}\frac{-1^n}{\sqrt{n}}$$
> > ## Solution
> >
> > We can test the convergence of the given series using the alternating series test, which states that if a series\
> > $$\sum_{n=1}^{\infty}(-1)^{n+1}b_n$$\
> > satisfies the conditions:\
> > - $$b_n > 0$$ for all $$n \in \mathbb{N}$$, and\
> > - $$b_{n+1} \leq b_n$$ for all $$n \in \mathbb{N}$$,\
> > then the series converges.\
> > In the given series, we have $$b_n = \frac{1}{\sqrt{n}}$$, which is always positive.\
> > Also, $$b_{n+1} = \frac{1}{\sqrt{n+1}} \leq \frac{1}{\sqrt{n}} = b_n$$ for all $$n \in \mathbb{N}$$.\
> > Therefore, the alternating series test applies, and we can conclude that the series converges.\
> > To determine whether the series is absolutely convergent or conditionally convergent, we need to consider the series\
> >  $$\sum_{n=1}^{\infty}\left|\frac{(-1)^n}{\sqrt{n}}\right| = \sum_{n=1}^{\infty}\frac{1}{\sqrt{n}}$$.\
> > This series diverges, since it is a $$p$$-series with\
> >  $$p=\frac{1}{2}$$, and $$p \leq 1$$.\
> > Therefore, the given series is not absolutely convergent, but it is conditionally convergent.
> {: .solution}
{: .challenge}
> (e) $$\sum_{n=1}^{\infty}\frac{-1^n}{\sqrt{n}}$$
> > ## Solution
> >
> > We can test the convergence of the given series using the alternating series test, which states that if a series\
> > $$\sum_{n=1}^{\infty}(-1)^{n+1}b_n$$\
> > satisfies the conditions:\
> > - $$b_n > 0$$ for all $$n \in \mathbb{N}$$, and\
> > - $$b_{n+1} \leq b_n$$ for all $$n \in \mathbb{N}$$,\
> > then the series converges.\
> > In the given series, we have $$b_n = \frac{1}{\sqrt{n}}$$, which is always positive.\
> > Also, $$b_{n+1} = \frac{1}{\sqrt{n+1}} \leq \frac{1}{\sqrt{n}} = b_n$$ for all $$n \in \mathbb{N}$$.\
> > Therefore, the alternating series test applies, and we can conclude that the series converges.\
> > To determine whether the series is absolutely convergent or conditionally convergent, we need to consider the series\
> >  $$\sum_{n=1}^{\infty}\left|\frac{(-1)^n}{\sqrt{n}}\right| = \sum_{n=1}^{\infty}\frac{1}{\sqrt{n}}$$.\
> > This series diverges, since it is a $$p$$-series with\
> >  $$p=\frac{1}{2}$$, and $$p \leq 1$$.\
> > Therefore, the given series is not absolutely convergent, but it is conditionally convergent.
> {: .solution}
{: .challenge}
 -->