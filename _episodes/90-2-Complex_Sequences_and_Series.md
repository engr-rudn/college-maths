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
> > We can test the convergence of the given series using the alternating series test, which states that if a series<br>
> > $$\sum_{n=1}^{\infty}(-1)^{n+1}b_n$$<br>
> > satisfies the conditions:<br>
> > \* $$b_n > 0$$ for all $$n \in \mathbb{N}$$, and<br>
> > \* $$b_{n+1} \leq b_n$$ for all $$n \in \mathbb{N}$$,<br>
> > then the series converges.<br>
> > In the given series, we have $$b_n = \frac{1}{\sqrt{n}}$$, which is always positive.<br>
> > Also, $$b_{n+1} = \frac{1}{\sqrt{n+1}} \leq \frac{1}{\sqrt{n}} = b_n$$ for all $$n \in \mathbb{N}$$.<br>
> > Therefore, the alternating series test applies, and we can conclude that the series converges.<br>
> > To determine whether the series is absolutely convergent or conditionally convergent, we need to consider the series<br>
> >  $$\sum_{n=1}^{\infty}\left|\frac{(-1)^n}{\sqrt{n}}\right| = \sum_{n=1}^{\infty}\frac{1}{\sqrt{n}}$$.<br>
> > This series diverges, since it is a $$p$$-series with<br>
> >  $$p=\frac{1}{2}$$, and $$p \leq 1$$.<br>
> > Therefore, the given series is not absolutely convergent, but it is conditionally convergent.
> {: .solution}
{: .challenge}
> (b) $$\sum_{n}{\infty}\frac{(-1^n)n(n+1)}{\(n+2)(n+3)}$$
> > ## Solution
> >
> > $$
\begin{align*}
\sum_{n=1}^{\infty}\left|\frac{(n^2+n)}{(n+2)(n+3)}\right| &= \sum_{n=1}^{\infty}\frac{n^2+n}{(n+2)(n+3)} \
&= \sum_{n=1}^{\infty}\left(\frac{1}{n+3} - \frac{1}{n+2}\right) \
&= \sum_{n=4}^{\infty}\frac{1}{n} - \frac{1}{2} + \frac{1}{3}
\end{align*}
$$\
> > Since the terms of this series do not approach zero, the series diverges.<br>
> > Using the ratio test, we have:<br>
> > $$\lim_{n\rightarrow \infty}\left|\frac{a_{n+1}}{a_n}\right| = \lim_{n\rightarrow \infty}\frac{(n+1)^2+(n+1)}{(n+2)(n+3)}\frac{(n+2)(n+3)}{n^2+n}$$ <br>
> > $$\lim_{n\rightarrow \infty}\frac{(n^2+2n+1+n+1)(n+2)}{(n^2+n)(n+4)}$$
> > $$\lim_{n\rightarrow \infty}\frac{(n^2+3n+2)(n+2)}{(n^2+n)(n+4)}$$<br>
> > $$\lim_{n\rightarrow \infty}\frac{n^3+5n^2+8n+4}{n^3+5n^2+4n^2+4n}$$ 
> > $$\lim_{n\rightarrow \infty}\frac{n^3+5n^2+8n+4}{n^3+9n^2+4n}= 1$$<br>
> > Since the limit is equal to 1, the ratio test is inconclusive.<br>
> > However, using the alternating series test, we can show that the series converges. We have:<br>
> > $$\frac{(n^2+n)}{(n+2)((n+3)}>0$$ for all $$n \in \mathbb{N}$$,<br>
> > $$a_{n+1} \le a_{n}$$ for all $$n \ge 1$$.<br>
> > Therefore, the series converges by the alternating series test.<br>
> > Since the series $$\sum_{n=1}^{\infty}\left|\frac{(n^2+n)}{(n+2)(n+3)}\right|$$ diverges,<br>
> >the original series<br>
> > $$\sum_{n=1}^{\infty}\frac{(-1)^nn(n+1)}{(n+2)(n+3)}$$<br>
> >  is conditionally convergent.<br>
> > $$\sum_{n=1}^{\infty}\frac{(-1)^nn(n+1)}{(n+2)(n+3)} = \sum_{n=1}^{\infty}\frac{(-1)^n(n^2+n)}{(n+2)(n+3)}$$<br>
> > Let $$a_n = \frac{(n^2+n)}{(n+2)(n+3)}$$. Then,<br>
> > $$\lim_{n\rightarrow \infty}\left|\frac{a_{n+1}}{a_n}\right| =$$<br>
> > $$\lim_{n\rightarrow \infty}\frac{(n+1)^2+(n+1)}{(n+3)(n+4)}\frac{(n+2)(n+3)}{n^2+n}$$<br>
> > $$=\lim_{n\rightarrow \infty}\frac{(n^2+2n+1+n+1)(n+2)}{(n^2+n)(n+4)}$$ =<br>
> > $$\lim_{n\rightarrow \infty}\frac{(n^2+3n+2)(n+2)}{(n^2+n)(n+4)}$$<br>
> > $$=\lim_{n\rightarrow \infty}\frac{n^3+5n^2+8n+4}{n^3+5n^2+4n^2+4n}$$<br>
> > $$=\lim_{n\rightarrow \infty}\frac{n^3+5n^2+8n+4}{n^3+9n^2+4n} = 1$$<br>
> > Using the alternating series test, we can determine that the series is conditionally convergent.<br>
> > The absolute value series can be written as:<br>
> > $$\sum_{n=1}^{\infty}\left|\frac{(n^2+n)}{(n+2)(n+3)}\right| = \sum_{n=1}^{\infty}\frac{n^2+n}{(n+2)(n+3)}$$<br>
> > Using partial fractions, we can write:<br>
> > $$\frac{n^2+n}{(n+2)(n+3)} = \frac{1}{n+3} - \frac{1}{n+2}$$
> {: .solution}
{: .challenge}
> (c) $$\sum_{n}{\infty}\frac{(-1^n)n(n+1)}{(n+2)(n+3)(n+4)}$$
> > ## Solution
> >
> > We will use the alternating series test to show that the series converges. We have:\
> > $$\frac{(-1)^nn(n+1)}{(n+2)(n+3)(n+4)}>0$$ for all $$n \in \mathbb{N}, and$$<br>
> > $$\lim_{n\rightarrow \infty}\frac{n(n+1)}{(n+2)(n+3)(n+4)} = $$	 
> > $$\lim_{n\rightarrow \infty}\frac{n(n+1)}{(n+2)n(n+3)(n+4)/n}= $$<br>	 
> > $$ \lim_{n\rightarrow \infty}\frac{n(n+1)}{(n+2)n(n+3)(n+4)}n= $$		
> > $$\lim_{n\rightarrow \infty}\frac{n^2+n}{(n^4+9n^3+26n^2+24n)}= $$<br>	
> > $$\lim_{n\rightarrow \infty}\frac{1/n+1/n^3}{1+9/n+26/n^2+24/n^3} = 0$$.	
> > Therefore, the series<br>
> > $$\sum_{n=1}^{\infty}\frac{(-1)^nn(n+1)}{(n+2)(n+3)(n+4)}$$
> >  converges by the alternating series test.<br>
> > To determine whether the series is absolutely convergent, we consider the series of absolute values:<br> 
> > $$\sum_{n=1}^{\infty}\left|\frac{(-1)^nn(n+1)}{(n+2)(n+3)(n+4)}\right|$$= 
> > $$\sum_{n=1}^{\infty}\frac{n(n+1)}{(n+2)(n+3)(n+4)}$$<br> 
> > Using partial fractions,<br> 
> > $$\frac{n(n+1)}{(n+2)(n+3)(n+4)}= \frac{1}{2(n+2)}-\frac{2}{(n+3)}+\frac{3}{2(n+4)}$$<br>
> > Therefore,<br>
> > $$\sum_{n=1}^{\infty}\left|\frac{(-1)^nn(n+1)}{(n+2)(n+3)(n+4)}\right|=\sum_{n=1}^{\infty}\frac{1}{2(n+2)}-\frac{2}{(n+3)}+\frac{3}{2(n+4)}$$<br>
> > We can rewrite this series as:<br>
> > $$-\frac{1}{4}-\frac{1}{5}+\frac{3}{8}-\frac{1}{6}-\frac{1}{7}+\frac{3}{4}-\frac{1}{8}-\frac{1}{9}+\frac{3}{12}- ...$$<br>
> > It can be observed that the series of absolute values does not converge. Hence, the original series is not absolutely convergent.<br>
> > Therefore, the original series $$\sum_{n=1}^{\infty}\frac{(-1)^nn(n+1)}{(n+2)(n+3)(n+4)}$$ is conditionally convergent.
> {: .solution}
{: .challenge}
> (e) $$\sum_{n}{\infty}\frac{(-1^n)(n+a)(n+b)}{\(n+c)(n+d)(n+e)}$$
> where a, b, c, d and e are real numbers and none of c, d or e is a negative integer (but e is not necessarily the base of the natural logarithm).
> > ## Solution
> >
> >We will use the alternating series test to show that the series converges. We have:<br>
> >  $$\frac{(-1)^n(n+a)(n+b)}{(n+c)(n+d)(n+e)}>0$$ for all $$n \in \mathbb{N}$$,<br>
> > and <br>
> > $$\lim_{n\rightarrow \infty}\frac{(n+a)(n+b)}{(n+c)(n+d)(n+e)}$$<br>
> > $$=\lim_{n\rightarrow \infty}\frac{n^2+(a+b)n+ab}{n^3+(c+d+e)n^2+(cd+ce+de)n+cde}$$<br>
> >= \lim_{n\rightarrow \infty}\frac{1+\frac{a+b}{n}+\frac{ab}{n^2}}{1+\frac{c+d+e}{n}+\frac{cd+ce+de}{n^2}+\frac{cde}{n^3}} = 0.$$<br>
> >Therefore, the series $$\sum_{n=1}^{\infty}\frac{(-1)^n(n+a)(n+b)}{(n+c)(n+d)(n+e)}$$<br>
> >converges by the alternating series test.<br>
> > To determine whether the series is absolutely convergent, we consider the series of absolute values:<br>
> >$$\sum_{n=1}{\infty}\left|\frac{(-1^n)(n+a)(n+b)}{\(n+c)(n+d)(n+e)}\right|=\sum_{n}{\infty}\frac{\left|(n+a)\right|\left|(n+b)\right|}{\left|\(n+c)\right|\left|(n+d)\right|\left|(n+e)\right|}$$<br>
> >Using the comparison test with the series $$\sum_{n=1}^{\infty}\frac{1}{n^3}$$, we have:<br>
> >$$\frac{\left|(n+a)\right|\left|(n+b)\right|}{\left|\(n+c)\right|\left|(n+d)\right|\left|(n+e)\right|} \le \frac{(n+\left|a\right|)\frac{(n+\left|b\right|)}{n^3}$$<br>
> >Since $$\sum_{n=1}^{\infty}\frac{(n+|a|)(n+|b|)}{n^3}$$ converges (it is a convergent p-series with $$p=3>1$$),<br>
> >the series $$\sum_{n=1}^{\infty}\frac{|n+a||n+b|}{|n+c||n+d||n+e|}$$ converges absolutely,<br>
> >and hence the original series $$\sum_{n=1}^{\infty}\frac{(-1)^n*(n+a)(n+b)}{(n+c)(n+d)*(n+e)}$$<br>
> >is absolutely convergent.
> >Therefore, the original series $$\sum_{n=1}^{\infty}\frac{(-1)^n*(n+a)(n+b)}{(n+c)(n+d)*(n+e)}$$ is convergent, and it is also absolutely convergent.
> {: .solution}
{: .challenge}
> (g) $$\sum_{n=1}{\infty}\frac{1}{\(n+i)}$$
> where a, b, c, d and e are real numbers and none of c, d or e is a negative integer 
>
> > ## Solution
> >
> > We will use the limit comparison test to determine the convergence of the series $$\sum_{n=1}^{\infty}\frac{1}{n+i}$$.<br>
> >Let $$a_n = \frac{1}{n+i}$$. We will compare this series with the harmonic series, $$b_n = \frac{1}{n}$$.<br>
> >We have:<br>
> >$$\lim_{n\rightarrow \infty}\frac{a_n}{b_n} = \lim_{n\rightarrow \infty}\frac{\frac{1}{n+i}}{\frac{1}{n}}$$<br>
> >$$\lim_{n\rightarrow \infty}\frac{n}{n+i}= 1$$<br>.
> >Since $$\sum_{n=1}^{\infty}\frac{1}{n}$$ is a divergent series, the limit comparison test implies that $$\sum_{n=1}^{\infty}\frac{1}{n+i}$$ is also a divergent series.<br>
> >Therefore, the series $$\sum_{n=1}^{\infty}\frac{1}{n+i}$$ is divergent.
> {: .solution}
{: .challenge}
> ## Exercises 10.3.2 
> 1. The series $$\sum_{n=0}^{\infty}\frac{(-1)^n}{\sqrt{n+1}}$$ converges by Leibniz’s test. Let its Cauchy product with itself be the series $$\sum_{n=0}^{\infty}c_{n}$$. Show that $$\left|c_{n}\right | \ge 1$$, so that $$\sum_{n=0}^{\infty}c_{n}$$ diverges.
>
> > ## Solution
> >
> > The series $$\sum_{n=0}^{\infty}\frac{(-1)^n}{\sqrt{n+1}}$$ converges by Leibniz’s test.<br>
> > Let its Cauchy product with itself be the series $$\sum_{n=0}^{\infty}c_{n}$$. That is,<br>
> >$$\sum_{n=0}^{\infty}c_{n} = \sum_{n=0}^{\infty}\left(\frac{(-1)^n}{\sqrt{n+1}}\right) \left(\frac{(-1)^n}{\sqrt{n+1}}\right)<br>
> > $$\sum_{n=0}^{\infty}\frac{1}{n+1}.$$<br>
> >Now, consider $$n \geq 1$$. Then, $$n+1 \geq 2$$, so $$\frac{1}{n+1} \leq \frac{1}{2}$$.<br>
> >Therefore, we have<br>
> >$$\left∣c_{n}\right|=\left|\frac{1}{n+1} \ge \frac{1}{n+1} \ge \frac{1}{2},$$<br>
> >since $$n+1 \geq 2$$. Hence, $$\sum_{n=0}^{\infty}c_{n}$$ diverges by the Comparison Test.
> {: .solution}
{: .challenge}
> 3. Prove Mertens’ theorem. Let the series  $$\sum_{n=0}^{\infty}a_{n}$$ and    $$\sum_{n=0}^{\infty}b_{n}$$ be convergent, let  $$\sum_{n=0}^{\infty}a_{n}=A$$ 
 and     $$\sum_{n=0}^{\infty}b_{n}=B$$. Assume that one of the series, let us say the first, is absolutely convergent. Then the Cauchy product is convergent and its sum is AB.
Hint. Let $$A_{n}  = \sum_{k=0}^{n}a_{k}$$, $$B_{n}  = \sum_{k=0}^{n}b_{k}$$ ,$$c_{n}  = \sum_{k=0}^{n}a_{k}b_{n-k}$$, $$C_{n}  = \sum_{k=0}^{n}c_{k}$$ Show that $$Cn =  \sum_{k=0}^{n}a_{k}B_{n-k}$$  and use this to estimate $$C_{n} - B\sum_{k=0}^{n}a_{k}$$ for large n.
>
> > ## Solution
> >
> > We are given two convergent series $$\sum_{n=0}^{\infty} a_n = A$$ and $$\sum_{n=0}^{\infty} b_n = B$$, where the first series is absolutely convergent. Let $$A_n = \sum_{k=0}^{n} a_k$$ and $$B_n = \sum_{k=0}^{n} b_k$$. We define the Cauchy product of the two series as $$\sum_{n=0}^{\infty} c_n$$ where $$c_n = \sum_{k=0}^{n} a_k b_{n-k}$$, and $$C_n = \sum_{k=0}^{n} c_k$$. Our goal is to show that $$C = AB$$.<br>
> >First, note that we can express $$C_n$$ as $$C_n = \sum_{k=0}^{n} a_k \sum_{j=0}^{n-k} b_j = \sum_{k=0}^{n} a_k B_{n-k}$$, using the definition of $$B_n$$.<br>
> >Next, we can estimate $$C_n - AB$$ as follows:<br>
> >$$C_n - AB &= \sum_{k=0}^{n} a_k B_{n-k} - AB$$<br>
> >$$= \sum_{k=0}^{n} a_k B_{n-k} - \sum_{k=0}^{n} a_k B + \sum_{k=0}^{n} a_k B - AB $$<br>
> >$$= \sum_{k=0}^{n} a_k (B_{n-k} - B) + (\sum_{k=0}^{n} a_k)(B - B) $$<br>
> >$$= \sum_{k=0}^{n} a_k (B_{n-k} - B) $$<br>
> >$$= \sum_{k=0}^{n} a_k \sum_{j=n-k+1}^{\infty} b_j $$<br>
> >$$= \sum_{k=0}^{n} a_k \sum_{j=0}^{\infty} b_{n-k+j+1}$$<br>
> >Since $$\sum_{n=0}^{\infty} b_n = B$$ is convergent, we have $$\lim_{n\to\infty} B_n = B$$, so for any $$\epsilon \gt 0$$, there exists an $$N$$ such that for all $$n \gt N$$, $$|B_n - B| \lt \epsilon$$. Then, for $$n > 2N$$, we have
> >$$\left|C_n - AB\right| = \left|\sum_{k=0}^{n} a_k \sum_{j=0}^{\infty} b_{n-k+j+1} - AB \right|<br>
> >= \left|\sum_{k=0}^{n} a_k \sum_{j=0}^{N} b_{n-k+j+1} + \sum_{k=0}^{n} a_k \sum_{j=N+1}^{\infty} b_{n-k+j+1} - AB \right|<br>
> >$$\leq \left|\sum_{k=0}^{n} a_k \sum_{j=0}^{N} b_{n-k+j+1} - AB_n \right| + \left|\sum_{k=0}^{n} a_k \sum_{j=N+1}^{\infty} b_{n-k+j+1} \right|$$
> {: .solution}
{: .challenge}