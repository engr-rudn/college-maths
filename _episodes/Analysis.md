---
title: Real Analysis
questions:
- "What basic?"
- "How can ?"
- "How do ?"
- "Can I ?"
objectives:
- "???"
- "???"
---

# Real Analysis

## Right Control (Shadow) Points

Suppose $$f\in C[a,b]$$,
$$
r.c.(f)=\{x\in(a,b)|\exists x'\in(x,b),f(x)<f(x')\}
$$.

$$ 
x\not\in r.c.(f) \iff \forall x'\in[x,b], f(x)\geq f(x')
$$.

$$
l.c.(f)=\{x\in(a,b)|\exists x'\in(a,x),f(x)<f(x')\}
$$.

#### Riesz Sunrise Lemma

Suppose $$f\in C[a,b]$$. $$rc(f)=\bigcup_i(a_i,b_i)$$ (from left to right), $$b_i$$ is the local maximum, $$f(a_i)=f(b_i)>f(x),x\in(a_i,b_i),i>1, f(a_1)\leq f(b_1)$$, $$f(b_i)\searrow$$.

*Proof.*
$$rc(f)$$ is open.

## Right Control (Shadow) Points (General)
Suppose $$f\in C[a,b]$$,
$$
r.c.(f)=\{x\in(a,b)|\exists x'\in(x,b),f(x), f(x-),f(x+)<f(x')\}
$$.

$$
x\not\in r.c.(f) \iff \forall x'\in[x,b], f(x)\geq f(x')
$$.

$$
l.c.(f)=\{x\in(a,b)|\exists x'\in(a,x),f(x),f(x-),f(x+)<f(x')\}
$$.

#### Riesz Sunrise Lemma (General)

Suppose $$f\in PC[a,b]$$. $$r.c.(f)=\bigcup_i(a_i,b_i)$$ (from left to right), $$f(a_i+)\leq\max\{f(b_i),f(b_i-),f(b_i+)\}>f((a_i,b_i))$$.

#### Riesz sloping

if $$D^+f(x)>n$$ then $$x\in r.c.(f(x)-nx)$$.

### Problem

$$f:[a,b]\to\mathscr{P}(\mathbb{R})$$, define
$$$$rc(f)=\{x\in(a,b)|\exists x'\in(x,b),\sup f(x)<\sup f(x')\}=?$$$$

## Banach Index

#### Banach Index Fuction

$$N_f(y,E) := \sharp \{x\in E|f(x)=y\}, L_f(y,E):=\begin{cases}
1,& \exists x\in E, f(x)=y,\\
0,& else.
\end{cases}$$. $$E$$ is the definition domain defaultly.

#### Theorem (Banach)

If $$f\in C[a,b]$$, then $$N_f$$ is measurable and
$$$$\int_m^M N = V_a^b(f).$$$$ 

*proof.*
Construct $$N_n=\sum_kL_k \nearrow N$$. (Approximation Lemma) $$N_n(y)=N(y)$$ for large $$n$$ when $$N(y)<\infty$$.

*remark.* $$m\{N(y)=\infty\}=0$$.

#### Fact

Suppose $$f\in C[a,b], N(y)<\infty$$, $$N(y,E_k)\not\rightarrow 0$$. Then there exists $$x\in\limsup_kE_k$$ that $$f(x)=y$$.


### Method
Investigate $$f$$ that (Dini derivative) $$|Df(x)|\leq M$$ on $$E$$.
$$
E_n:=\{x\in E| \forall y\in[a,b],|y-x|<\frac{1}{n}, |f(y)-f(x)|\leq (M+\epsilon)|y-x|\}\nearrow E
$$. If $$
|Df(x)|\geq M
$$ on $$E$$. 
$$
E_n:=\{x\in E| \forall y\in[a,b],|y-x|<\frac{1}{n}, |f(y)-f(x)|\geq (M-\epsilon)|y-x|\}\nearrow E
$$.



## Baire Functions

#### Romanovski Lemma

$$\Theta$$ open interval family in $$[a,b]$$:

1. $$(\alpha,\beta),(\beta,\gamma)\in \Theta$$, then $$(\alpha, \gamma)\in \Theta$$

2. subsets-closed

3. $$\forall [\alpha,\beta]\subset(c,d),(\alpha,\beta)\in\Theta$$, then $$(c,d)\in \Theta$$

4. intervals contiguous to perfect closed set $$E$$ $$\subset \Theta$$, then $$\exists I\in \Theta, I\cap E\neq\emptyset$$.

   Then $$(a,b)\in\Theta$$.



## Approx. Cont. Functions

#### Definition

$$f$$: ap.c. at $$x_0\in I$$, =df $$E\subset I$$, $$d(E,x_0)=1$$ and $$f|_E$$: cont. at $$x_0$$.



## Darboux functions

#### Darboux functions

$$f\in D([a,b])$$ =df $$ \forall x_1,x_2\in[a,b], f(x_1)\leq y\leq f(x_2),\exists x_3\in [x_1,x_3],y=f(x_3)$$
$$f\in D^*([a,b])$$ =df $$\forall x_1,x_2\in[a,b], f(x_1)\leq y\leq f(x_2),\exists(\infty) x_3\in [x_1,x_3],y=f(x_3)$$
$$f\in D^{**} ([a,b])$$ =df $$\forall x_1,x_2\in[a,b], f(x_1)\leq y\leq f(x_2),\exists(c) x_3\in [x_1,x_3],y=f(x_3)$$



*example*

$$W(x)=\limsup_n\frac{\sum_ia_i}{n},x=0.a_1a_2\cdots$$.