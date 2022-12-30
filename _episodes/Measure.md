# Measure

## Infinite product space
Suppose $(X,\mathcal{A}_i)$ are measurable spaces. Let product measurable space $\prod_i\mathcal{A}_i:=\sigma\{\prod_iA_i,A_i\in\mathcal{A}_i, almost, A_i=X_i\}$.

$\mathcal{D}_n:=\{A\times\prod_{i> n}X_i,A\in\prod_{i=1}^n\mathcal{A}_i\},\mathcal{A}=\sigma\mathcal{D}=\sigma\{\mathcal{D}_{n},n=1,\cdots\}$.

$\mathcal{D}_{n,m}:=\{A\times\prod_{i>m}X_i,A\in\prod_{n<i\leq m}\mathcal{A}_i\},\mathcal{A}_{n}=\sigma\{\mathcal{D}_{n,m},m\geq n\}$.

$\mu_i$ is probability on $X_i$.

Let $A=A'\times \prod_{i>m}X_i\in\mathcal{D},A'\in\prod_{i\leq m}\mathcal{A}_i$.

$$
\mu(A(w_1,\cdots,w_n))=\int \prod_{n<i\leq m}\mu_i(A'(w_1,\cdots,w_n))d\prod_{i\leq n}\mu_i\\
=\int\mu(A(w_1,\cdots,w_n))d\prod_{i\leq n}\mu_i.
$$
Similarly, for $A\in\mathcal{D}_n$,

$$
\mu(A(w_{n+1},\cdots,w_m))
=\int\mu(A(w_{n+1},\cdots,w_m))d\prod_{n<i\leq m}\mu_i.
$$


### $\mu$ is a measure.

### $A_j=A_j'\times\prod_{i>n_j}X_i\to\emptyset\in\mathcal{D}$ then $\mu A_j\to 0$.

*Main idea.* $\mu A_j>\epsilon$ then $\mu A_j(v_1)>\frac{\epsilon}{2}$.

*Proof (proof by contradiction).* $B_1^{(j)}:=\{w_1\in X_1, \mu(A_j(w_1))>\frac{\epsilon}{2}\}$.

Since $\mu A_j=\int \mu A(w_1)d\mu_1$, 
$0<\epsilon<\mu A_j\leq \mu_1 B_1+\frac{\epsilon}{2}$.
Thus $\mu_1 B_1^{(j)}>\frac{\epsilon}{2}$.
There exists $v_1\in\bigcap_jB_1^{(j)}$, i.e. $\mu A_j(v_1)>\frac{\epsilon}{2}$.

We get
$\mu A_j(v_1,\cdots,v_{n_j})>\frac{\epsilon}{2^{n_j}}>0$.
$(v_1,\cdots)\in A_j$.


## transitive measure

### theorem
Suppose $(X_i,\mathcal{A}_i)$ are measurable spaces. $\mu_1$ is $\sigma$-finite measure on $X_1$, $\mu_k$ is the $\sigma$-finite transitive measure $X$ to $Y$. Then
$$\mu B=\int \chi_B(w_1,\cdots,w_n)\mu_n(w_1,\cdots,dw_n)\cdots\mu_1(dw_1)$$
is a measure. If $\mu_i$ is uniformly $\sigma$-finite, then $\mu$ is $\sigma$-finite.

*Proof.*
In case $n=2$.
$\mu(A_l\cap B_m\times C_k)\leq \sup_{w_1}\mu_2(w_1,C_k)\mu_1(A_l\cap B_m)<\infty$.