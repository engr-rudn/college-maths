# Sampling Theory

## Assumption/Notations

1. $H$: Hilbert space

2. $M$: diff manifold (i.e. a domain of $\C$)

3. $k:M\to H$

4. $T_k(u)=\lambda z. \langle u, k(z)\rangle: H\to C^\infty(M)$.

5. $\mathscr{H}_k= ran T_k $ : RKHS.

6. $S_n(z)=\langle k(z), x_n\rangle$ sample functions

   

## Results

### Basic Fact

$T_k:H\leftrightarrow \mathscr{H}_k \iff \{k(z),z\in M\}$: completed.



### Analytic principle

$k\in H(M,H)$ iff $k\in H_w(M,H)$ iff $\langle x_n, k(x)\rangle\in H(M)$, $\{x_n\}$: s.o.b (of frame) and $k$ is bounded.

$k(z)=\sum a_n(z)x_n$ unif. $z\in M$.

*Proof* $k(z)=\sum_n \langle k(z), y_n\rangle x_n$, $\|k(z)\|^2\sim \sum_n|\langle k(z), y_n\rangle|^2$.



### Sampling Principle

Suppose $k\in H(M,H)$ and bounded.

If $\{k(z_n)\}$: $H$-s.o.b.,  then $f(z)=\sum_n f(z_n)\langle k(z_n), k(z)\rangle=\sum_nf(z_n)k(z_n,z)$, $f\in \mathscr{H}_k$.

Moreover, $c\in \ell^2$, then $\exists f\in\mathscr{H}, f(z_n)=c_n$.



*Remark* $k(x_m, y_n)=\langle k(x_m),k(y_n)\rangle=\delta_{mn}$, interpolation condition.



## Examples

####Whittaker-Shannon-Kotel'nikov Sampling Theorem

$H=L^2[0,1], \mathscr{H}=PW[0,1]$.

$k(z):=e^{2\pi i zt}$, $k(z_n)=e^{2\pi i n t}$: s.o.b. of $L^2[0,1]$. $S_n(z)=\frac{\sin \pi (z-n)}{\pi(z-n)}$.

$f(z)=\sum_n f(n)(-1)^n e^{-\pi i z}\frac{\sin \pi(n-z)}{\pi (n-z)}$.



#### $H=H^1[0,1]$

$k(z)=(z-a)e^{2 \pi it}+\sin \pi z\sinh 2\pi x, x\in[0,1]$.

$f(z)=(1-i(z-a))\frac{\sin\pi z}{\sin \pi a}f(a)+\sum_n f(n)\frac{z-a}{n-a}\frac{1+zn}{1+n^2}\sin(z-n)$.

