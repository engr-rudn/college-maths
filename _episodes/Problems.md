
# Problems

* ?: not solved

# Topology
## 1. Topology, $\sigma$ compactness
If $A$ is $\sigma$ compact, then its closure $\bar{A}$ is $\sigma$ compact or not.

### remark
In topological space, a subset $A$ is $\sigma$ compact if $A=\bigcup_{i=1}^\infty K_i$, $K_i$ is compact.

### counterexample
$\mathbb{Q}[0,1] \subset C[0,1]$.

## closed subsets ?
$X$ is a topological space. $F$ is a closed subset, then there exists a $f\in C(X)$ that $F=f^{-1}[0]$ (or $=f^{-1}I$, $I$ is closed in $\mathbb{R}$).


# Analysis
## 2. Analysis, convergence a.e.
Assume $\mathscr{C}\subset\mathscr{A}$ is a subfamily of measure space $(X,\mathscr{A},\mu)$.
For any measurable subset $A$ there exists a sequence of sets $C_n\in \mathscr{C}$ that $\mu(A\triangle\bigcup_nC_n)=0$, then for any measurable function $f$ there exists simple functions $\phi_n=\sum_ic^{(n)}_i\chi_{C_i^{n}}\nearrow f$ a.e., where $C_i^{n}\in \mathscr{C}$.

### remark
$\forall \epsilon>0\exists\{C_i,i=1,\cdots,n\},\mu(A\triangle\bigcup_iC_i)<\epsilon$.


## 3. Real analysis
### series 1
Assume $f\in L^1$ and $\sum_n\frac{1}{a_n}<\infty$, then
$f(a_nx)\to 0$ a.e..

### remark
Levi theorem. To prove $\sum_n |f(a_nx)|$ is convergent, a.e..

### series 2 Kronecker lm
$x_n\in \mathbb{R}, a_n\nearrow \infty, \sum_k\frac{x_k}{a_k}$ conv, then $\frac{\sum_kx_k}{x_n}\to0$.

*Remark.* summation by parts.


## 5. Continous functions
$f_\lambda\in C(X)$ implies $\sup(\inf)_\lambda f_\lambda\in C(X)$? False

There exists $f_n\in C[0,1]\searrow f\not\in C[0,1]$.


## 6. Banach inditrix
Suppose $f\in C(X)$ where $X$ is a compact (Hausdorff) space and Banach Indicatrix $N(y)=card\{x\in X|f(x)=y\}$. Then $m\{y|N(y)=\infty\}=0$.

*Proof.* $A_\mu=f^{-1}[y_\mu]=\{x_{\lambda,\mu}\}$. $x_\mu\in A_\mu'$.



# Algebra

## Group

$S$ is an Abel semigroup with 0. $S_d=\{a\in S|\forall x, y\in S, x+a=y+a\to x=y\}$ generate a group $S_1$.

#### Fact

$S_d$ is an Abel semigroup with 0.

$a+b=c\in S,b,c\in S_d\to a\in S_d$ (let a=c-b, i.e. $(c-b)+b=c\in(S_d)$)

$S_1=S_d-S_d$.

$S_1, S$ generate Abel semigroup $S_2=S-S_d$.