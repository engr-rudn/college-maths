# Re-proof

## Topology

### Lebesgue Lemma

If $X$ is a compact metric space and $\mathcal{U}$ is an open covering, then for small $A$ (in diameter) $\exists U\in\mathcal{U}, A\subset U$.

*Proof.* For $x\in X$ define $\delta_x:=\sup\{\delta: S(x,\delta)\subset U\in\mathcal{U}\}$. We have a finite open covering $S(x_i,\delta_i=\delta_{x_i}/2)$. Take $\delta=\frac{\min_i\delta_i}{2}$.

*Idea.* Definition of compactness, Triangle inequality.

### Uniform Continuity

$f\in C(X)\iff f\in UC(X)$ where $X$ is a compact uniform space.

*Proof.* construct $W=\bigcap_kV_k$, $V_kV_k\subset U_k, V_k=V_k^{-1}$ where $\forall \epsilon \forall (x, y_k)\in U_k |f(x)-f(x_k)|<\epsilon$.

*Remark.* It holds for $C(X,Y)$ where $X,Y$ are both uniform spaces.



## Set theory

### Bernstein Theorem
$M\leq N,N\leq M \to M=N$.

*Proof1.* construct "Berstein chain".

*Proof2.* let $\mathcal{A}=\{A\subset M| g[N\setminus f[A]]\subset M\setminus A\}$ and $F=\bigcup\mathcal{A}$. $\phi:A\mapsto M\setminus g[N\setminus f[A]]$. We have $\phi(F)=F$.

## Real Analysis

### Riemann integrable
$f\in RI[a,b]$ (Riemann integrable), then $m\{x\in[a,b]:\neg C(f,x)\}=0$

### Lemma
If $\phi_n(x_0)\nearrow, \psi_n(x_0)\searrow f(x_0)$, $loc(x_0)x\exists n,\psi_n(x_0)-\epsilon<f(x)<\phi_n(x_0)+\epsilon$, then $C(f,x_0)$.

### the diagonalization principle
$\mathcal{F}\subset C(X)$ u.b $M$ is a countable subset of $X$, then a subsequence $f_n(x)$ of $\mathcal{F}$ conv. on $M$.