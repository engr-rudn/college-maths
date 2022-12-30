# Group action

## Definition

### semigroup action

$ax:S\times X\to X$ that $(ab)x=a(bx)$ and $1x=x$ if $1\in S$.

$\phi(ab)=\phi(a)\phi(b):S\to X^X$ (sub semigroup).

$ker(\phi)=\{a\in S: ax=x,\forall x\in X\}, ran(\phi)=Inn(S)\leq S_X$

*Remark* semigroup action == algebra of monoid $S\times X$.

### group action

$ax:G\times X\to X$ that $(ab)x=a(bx)$ and $1x=x$ if $1\in G$.

$\phi(ab)=\phi(a)\phi(b):G\to  ran(\phi)=Inn(G)\triangleleft G_X$.



### Concepts

* Orbits: $O(x)=\{ax: a\in S\},Orb(G)=\{O(x)\}, Orb^*(G)=\{O(x), |S(x)|>1\}$
* Stability: $S(x)=\{a\in S: ax=x\}\leq S, ker(\phi)=\bigcap_xS(x)$
* tran: $O(x)=X$
* feithful: $\ker\phi=\{1\}$

### Facts

* $Orb(G),\{fix(G)\}\cup Orb^*(x)\in\pi_X$ (orbit partition)

* $S(x)\triangleleft G, ax\mapsto aS(x):O(x)\sim G/S(x)$

* $ax=bx \iff a^{-1}b\in S(x) \iff a\sim_{S(x)} b$

* $[G:S(x)]=|O(x)|, (|O(x)| \mid |G|<\infty)$.

* $|X| = |fix(G)| + \sum_{O(x)\in Orb^*}|G|/|S(x)|$

* $x\sim_G y (O(x)=O(y)) \iff S(x)\simeq S(y)$

* $D=\{x:S(x)=\{1\}\}$, $\{fix(G), D\}\cup Orb^+(x)\in\pi_X$

  

### Theorems

* $\sum_{y\in O(x)}|S(y)|=|G|=|O(x)||S(x)|$ (Burnside Lemma)

* $|G||Orb|=\sum_x|S(x)|=\sum_{x,a}\delta_{x,ax}=\sum_a|fix(a)|=|X|+\sum_{a\neq 1}|fix(a)|$. (Burnside Thm)

* $G$:$p$-Group then $|X|=|fix(G)| (\mod p)$

  

  

### Examples

| Name            | $G$                                    | $X$                  | Action             | Stability                                    | Orbits                |
| --------------- | -------------------------------------- | -------------------- | ------------------ | -------------------------------------------- | --------------------- |
| Translation     | $G$                                    | $G$                  | $\phi(a)x=ax$      | $S(x)=1$                                     | $O(x)=G$              |
| conjugation     | $G$                                    | $G$                  | $axa^{-1}$         | $N(x)$                                       |                       |
| left-coset      | $G$                                    | $H$-LCS              | $axH$              | $S(xH)=xHx^{-1}$                             | $O(xH)=X$             |
| powerset        | $G$                                    | $\mathscr{P}(X)$     | $aS=\{ax,x\in S\}$ |                                              |                       |
| finite subsets  | $G$                                    | $\mathscr{P}_n(X)$   | $aS$               |                                              |                       |
| sylow           | $G$                                    | $\mathscr{P}_n(G)$   | $aS$               |                                              |                       |
| cycle           | $(\alpha),\alpha\in S_X$               | $X$                  | $\alpha^i x$       | $\{1,\alpha^r,\cdots\}, \min_r \alpha^r x=x$ |                       |
| production      | $G$                                    | $\prod_iX_i$         | $\{gx_i\}$         | $\bigcap_iS(x_i)$                            |                       |
| wheel           | $(\alpha),\alpha=\beta_1\cdots\beta_t$ | $\{x_1,\cdots,x_n\}$ | $\alpha^nx$        |                                              | $O(x_{ij})=[\beta_i]$ |
| coloring        | $G$                                    | $C^X$                | $af(x)=f(ax)$      |                                              |                       |
|                 | $G\leq S_X$                            | $\{c_1,\cdots,c_n\}$ | $ac=\{c_{ai}\}$    |                                              |                       |
| power           | $G$                                    | $X^n$                | $\{g(x_n)\}$       |                                              |                       |
|                 | $G$                                    | $(X,*)$              | $g(x*y)=gx*gy$     |                                              |                       |
|                 | $G$                                    | $X$                  | $g:X\simeq X$      |                                              |                       |
| subgroups       | $G$                                    | $L(G)$               | $aGa^{-1}$         | $N_A$                                        |                       |
| normal subgroup | $G$                                    | $N\triangleleft G$   | $axa^{-1}$         |                                              |                       |



### Coloring

$f:X\to C,c\in C$

#### Theorem

$X_{c}:=\{f(x)=c\}$: $a(/S)$-不变子集 iff $f\in fix(a)(/fix(S))$.

$a\in S(f) \iff f\in fix(a) \iff f(ax)=f(x)$ fixed-point eq.

