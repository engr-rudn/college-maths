# Functional Analysis

### Opial's Theorem
In Hilbert space $X$, let $T:D\to D,D\subset X$ satisfy

* nonexpansive, $\|Tv-Tu\|\leq\|v-u\|$,
* asymptotically regular, $T^{n+1}-T^n\to 0,n\to\infty$,
* fix $T\neq\emptyset$.

Then $A^nv\to a\in fix T$ weakly.

*Proof.* 下极限分离性

*Remark.*

### Lemma(下极限分离性)
In Hilbert space, $x_n\to x$ weakly, then
$x=y \iff \liminf_n\|x_n-y\|\leq(=)\liminf_n\|x_n-x\|$.

*Proof.* $y\neq 0\Rightarrow \liminf_n\|x_n+y\|>\liminf_n\|x_n\|​$.

$\|x_n+y\|^2=\|x_n\|^2+\|y\|^2+o(1)$.$x_n\perp_{approx} y$

### Lemma

In metric space $X$, $T$ is nonexpansive. $(1-T)x_n\to h$ then $\liminf_nd(x_n,h+Tx)\leq\liminf_nd(x_n,x)$.


### Continouity

## Lemma
$f\in C(X,Y)\iff \forall x_\lambda\to x \exists x_{\lambda_k}\to x,f(x_{\lambda_k})\to f(x)$.

($\forall U\in \mathcal{T}_{f(x_0)}, \check{lrg}\lambda, f(x_\lambda)\in U$)

*Remark.* In (semi)normal space, we select $|x_n-x|<2^{-n}$.



# $TT^*$-method

### Basic thoerem
Assume $H$: Hilbert space, $X$: Banach space, $D\subset X$ is dense.

$T\in L_a(D, H), T^*\in L_a(H, D_a^*)$ where 
$$ T^*v(f) =\langle v,Tf\rangle, f\in D, v\in H.$$

$\begin{align*}
\|Tf\|\lesssim \|f\|, f\in D \iff & ran T^*\subset X^*, \|T^*v\|\lesssim \|v\|, v\in H \\
\iff& ran T^*T\subset X^*, \|T^*Tf\|\lesssim \|f\|, f\in D\\
\Longrightarrow &T:X\to H, T^* T:X\to X^*.
\end{align*}$

If $T\in L_a(D, H),S\in L_a(F, H)$ are such operators, then $T^*S:X\to Y^*$.

*Proof.* $\|T^*v\|=\sup_{f\in D} |T^*v(f)|\lesssim \sup_f |\langle vTf\rangle|\lesssim \|v\|$...

*Remark.* $H$ can be replaced by $Y$ a Banach space that $Y\subset Y^*$, $|\tilde{v} (v)|=\|v\|^2$.


## Hilbert space

### Tikhonov reg. lemma
Suppose Hilbert space $H_1\hookrightarrow H$, let $M(x)=\|Tx-y\|^2_H+\|x\|^2_{H_1}, T\in L(H_1,H)$, if $\{\|x\|_{H_1}\leq C\}$ is compact in $H$ for all $C>0$, then there exists $x_n\to x\in H_1, M(x_n)\searrow \inf_x M(x)$.

