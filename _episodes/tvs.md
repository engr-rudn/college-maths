# Topological Vector Spaces
My notes for tvs

## Basic Concepts

### Definition of TopMod
$M$ is a top module, if it is a modle (a top Able group) on top ring $R$, with top that
$(r,m)\mapsto rm:R\times M\to M$ is continuous.

When $R$ is a top field, $M$ is a tvs.


### Basic Type of Sets
$A$ absorbs $B$ if $B\subset\lambda A$ for large $|\lambda|$. $A$ is radical if $A$ absorbs $\forall x\in X$.

### Lemma
If $V\in\mathcal{N}_0$ is compact and circle, $\lambda_n\to0+$, then $\{\lambda_nV\}$ is 0-basis.

## Homomorphism Theorem

### first homomorphism theorem for tvs
Let $f:X\to Y$ be continous and surjective, then $f$ is open iff $f_0:X/N\leftrightarrow Y$ is top isomorphism, where $N=ker f=f^{-1}[0]$.

*Remark.* In this case, if $X$ is complete then $Y$ is complete.

### Corollary
Suppose $f: X\to Y$ is of finite-rank where $0$ is closed in $f[X]$. Then $f$ is continuous iff $ker f$ is closed iff $f$ is open.

If $f\in X^*,f\neq 0$, then $f$ is open.

## Banach's Homomorphism Theorem

We denote by $S_r=\{|x|<r\},r>0$ in a tvs, where $|\cdot|$ is a pseudo-norm.

### Lemma 1
Suppose $X,Y$ are pseudonorm spaces and $X$ is complete, $T:X\to Y$ is continuous and satisfies that
$$\forall r>0\exists \rho>0, S_\rho\subset \overline{TS_r}.$$
Then $\overline{TS_r}\subset TS_t, t>r$.


*Proof.* Construct $\sum_ir_i<t(r_1=r),\rho_n\to0$ that
$$y\in T[S_r+S_{r_2}+\cdots+S_{r_n}]+S_{\rho_n}.$$ And $x_n\to x\in S_t, |y-Tx_n|<\rho_n$.

*Remark.* It holds if define $S_r=\{|x|\leq r\}$.

### Corollary (Continue Lemma 1)
If $X, Y$ are norm spaces (in Lemma 1), $T:X\to Y$ is continuous, then
$$S_\rho\subset\overline{TS_r} \iff S_\rho\subset TS_r.$$

*Proof.* (=> part) $T$ satisfies the condition of Lemma 1. $y\in S_\rho$, so there exists $0<\rho'<\rho, y\in S_{\rho'}$, then $y\in S_{\rho'}\subset\overline{TS_{r'}}\subset TS_r,r'(=r\rho'/\rho)<r$.

### Theorem 1
Let $X,Y$ be complete pseudonorms and $T:X\to Y, T[X]$ is dense in $Y$. Then either $T[X]$ is of first category in $M$, or else $T[X]=Y$ and $T$ is open.

*Proof.* $X=\bigcup_nnS_r$. Try to prove $0\in (\overline{TS_r})^\circ$ under sub-top $T[X]$.

*Remark.*
In addition, $T$ is bijective, then $T:L\leftrightarrow Y$ is a isomorphism.

### Corollary[Surject-Open Principle]
$T:X\to Y$ in Theorem 1. $T$ is $T[X]$-open iff $T[X]$ is closed (specially $T$ is surjective).

### Corollary
$(X,\mathcal{T}_1),(X,\mathcal{T}_2)$ are complete pseudonorm spaces, $\mathcal{T}_1\subset \mathcal{T}_2$, then thay are identified.
In Banach space, $\|\cdot\|_1\leq C \|\cdot\|_2$, then $\|\cdot\|_1\simeq\|\cdot\|_2$.


## Spaces of Linear Mappings
Let $\mathcal{G}$ be a directed family of subsets of $T$.
$$M(S,V)=\{f\in Hom(T,F), f[S]\subset V\},S\in\mathcal{G}, V\in\mathcal{B}$$ form a top basis of $F^T$. $F$ is linear space then so $F^T$ is.

### proposition
$\forall V\in\mathcal{B}_0, M(S,V)$ is radical iff $f[S]$ is $F$-closed.

### Theorem
Let $G\subset F^T$ (subspace). $G$ is tvs iff $\forall f\in G,S\in\mathcal{B}, f[S]$ is bounded. In addition, if $F$ is lcs, and $\bigcup\mathcal{G}$ is dense, then $G$ is lcs.

*Remark.*
If $F$ is lcs with seminorms $\mathcal{P}$, then $M(S,\mathcal{P},\epsilon)=\{\sup_{x\in S,p\in \mathcal{P}}p(f(x))<\epsilon\}$. If $F$ is normed space, then $M(S,\epsilon)=\{\|f\|=\sup_{x\in S}\|f(x)\|<\epsilon\}$.

It is easy to see $L(T,F)$ is lcs where $\bigcup\mathcal{G}$ is total and $\mathcal{G}$ is a family of bounded subsets of tvs $T$.
