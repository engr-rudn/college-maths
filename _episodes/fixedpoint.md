# Fixed points

## Lattice

### Basic Lemma
Suppose $L$ is a poset, $f:L\to L$ is monotonic, let $a=\sup G\in L,G=\{x\in L, x\leq f(x)\}\neq\emptyset$, then $a\in G$ is a fixed point of $f$.

*Proof.*
Let $G=\{x\in L, x\leq f(x)\}$. It is easy to see $f[G]\subset G$, $G\leq a\leq f(a)$, and $a\in G$, then $f(a)\in G$, thus $f(a)\leq a$. We get $f(a)=a$.

*Remark.* Specially $G=L, a=\sup L$, then $f(a)=a$.

### Lemma
Suppose $L$ is a poset closed in the sence that if $x_n\in L,x_n\nearrow x$ then $x\in L$, and $f:L\to L$ is monotonic. If $fix(f)=\{a\}$ and $f$ is continous, then $a=\sup G$ and $f^n(x)\nearrow a, x\in G$. ($G\neq\emptyset$)

*Proof.*
Let $(x)=\{f^n(x),n\in\mathbb{N}\},x\in G$ that is a sublattice (chain) of $L$. Let $f^n(x)\nearrow a(x)=\sup(x)\in G$, then $f(a(x))\in G$. And $f(a(x))=a(x)$, since $f$ is continous. $a(x)=a$.


### Theorem
Suppose $L$ is a *$\sigma$-completed lattice* with a lower bound $0\leq L$, $f:L\to L$ is monotonic, let $a=\sup G$, then $a$ is a fixed point of $f$. 

If $fix(f)=\{a\}$ ($a\in G$) and $f$ is continous, then $a=\sup G$ and $f^n(x)\nearrow a, x\in G$.

*Remark.* $0\in G, f^n(0)\nearrow a$.

*Application.* Gronwall's inequality.

### Corollary
Suppose $L$ is a completed lattice, $f:L\to L$ is monotonic, let $a=\sup G$, then $a$ is a fixed point of $f$. 

If $fix(f)=\{a\}$ and $f$ is continous, then $a=\sup G$ and $f^n(x)\nearrow a, x\in G$.

*Remark.* $\inf L\in G$.
