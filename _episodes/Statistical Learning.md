# Statistical Learning



## Logistic Regression

$$
logit(P(1|X))=\alpha +\sum_j f_j(X_j)\\

\max L(f,\alpha) = \prod_ip(y_i|x_i, f,\alpha)
$$

$logit (y) =\alpha +\sum_j w_jx_j $ equiv. to single layer neural network，with cross-entropy as error function.



### Codes

```python
from sklearn.linear_model import LogisticRegression
lr = LogisticRegression(C=C, penalty='l1', tol=0.01, solver='saga')
lr.fit(X, y)
lr.score(X, y)
lr.predict(X)
```



## Max Entropy

$$
\max_{P\in \mathcal{P}} H(Y|X)\\
E_P(f)=E_{\tilde{P}}(f)
$$

$P_w(y|x)=\frac{1}{Z_w(x)}e^{\sum_iw_if_i(x,y)}$ solution of max $L(P, w)$ Laplace function of (2).
$$
\max_w \Psi(w), \Psi(w)=L(P_w,w).
$$

*Remark*. $\Psi(w)=L_{\tilde{P}(P_w)},L_{\tilde{P}(P)}=\ln \prod_{x,y}p(y|x)^{\tilde{p}(x,y)}$.



## AdaBoost Algorithm

A special additive model.

### AdaBoost

**Algorithm**

input training data $(x_j, y_j)$, output classifier $G(x):X\to \{-1,1\}$

1. weights of data $D_1=(w_{11},\cdots , w_{1j}, \cdots)$, $w_{ij}=\frac{1}{N}$

2. * get $G_m$ according $D_m$
   * $e_m=P(G_m(x_j)\neq y_j)=\sum_{G_{m}(x_j)\neq y_j} w_{mj}$
   * coef of $G_m(x)$,  $\alpha_m=\frac{1}{2}\ln \frac{1-e_m}{e_m}$
   * get $D_{m+1}$ where $w_{m+1,j}=\frac{w_{mj}}{Z_m}e^{\alpha_my_iG_m(x_i)}$

3. $G(x)=sign(f(x))=sign(\sum_m \alpha_mG_m(x))$

$D_1\to G_1\to (e_1\to \alpha_1)\to D_2\to G_2\to\cdots G$.



for 2-classes problem:

$Z_m=2\sqrt{e_m(1-e_m)}=\sum_jw_{mj}e^{\pm\alpha_m}$

#### Bound of Error

$$
E=\frac{1}{N}\sharp\{G(x_j)\neq y_j\}\leq\frac{1}{N}\sum_i e^{-y_if(x_i)}=\prod_mZ_m.
$$

$$
E=\prod_m2\sqrt{e_m(1-e_m)}\leq e^{-2\sum_m(1/2-e_m)^2} (2-classes)
$$

*Remark*. It is a sort of **forword stagewise algorithm**, with $L(y, f)=e^{-yf}$.

*See also* Boosting tree, with $L(y,f)=(y-f)^2$.



## EM algorithm



### Algorithm

model with latent rv

**Algorithm**

input $Y,Z$ distribution $P(Y,Z|\theta), P(Z|Y,\theta)$, output $\theta$

1. set $\theta_0$

2. E:

   $Q(\theta,\theta_i)=E_Z(logP(Y,Z|Y,\theta_0)|Y, \theta_0)$, $Q$-function

   M:

   $\theta_{i+1}=\arg\max_{\theta} Q(\theta,\theta_i)$

3. repeat 2 until convergence



**Theorem** in EM

$P(Y|\theta_i)\nearrow$, $L(\theta_i)\to L^*$ if $P(Y|\theta)$ is ub; $\theta_i\to \theta^*$ stable point of $L$, in most cases.

*proof*. $\log P(Y|\theta_{i+1})-\log P(Y|\theta_i)=Q(\theta_{i+1}, \theta_i)-Q(\theta_i, \theta_i)+d$ where $d$ is the [Kullback–Leibler divergence](https://en.wikipedia.org/wiki/Kullback%E2%80%93Leibler_divergence) of $Y,Z|\theta$ and  $Y,Z|\theta_i$.



*Remark*. EM sloves $\max L(\theta)$.
$$
L(\theta)-L(\theta_0)\geq B(\theta,\theta_0)-L(\theta_0)=\Delta\\
\arg\max_\theta B(\theta,\theta_0) = \arg\max_\theta Q(\theta,\theta_0)
$$

### Examples

* 3-coins model

* Gaussian misture model



### GEM

**Definition(F function)**

$F(p,\theta)=E_Z(\ln P(Y, Z|\theta))+H(p)$.

## HMM

a time series version of EM model, $\theta=(A,B,\pi)$

### Assumption

1. $P(x_t|x_{t-1},y_{t-1},\cdots)=P(x_t|x_{t-1})$

2. $P(y_t|\cdots) = P(y_t|x_t)$



$\gamma_t(i)=P(x_t=i|y, \theta),\xi_t(i,j)=P(x_t=i,x_{t+1}=j|y,\theta)$

### Algorithm

**Definition(forward prob)**

$\alpha_t(x)=P(Y_1,\cdots,Y_t,X_t=x|\theta)$



**Algorithm**

input $\theta, y$

output $P(Y|\theta)$

1. $\alpha_1(i)=\pi_ip(y_1|x_i)$
2. $\alpha_{t+1}(i)=\sum_j\alpha_t(j)a_{ji}P(y_{t+1}|x_i)$
3. $P(Y|\theta)=\sum_i\alpha_T(i)$

**Definition(backward prob)**

$\beta_t(x) = P(Y_{t+1},\cdots,Y_T|X_t=x,\theta)$

**Algorithm**

input $\theta, y$

output $P(Y|\theta)$

1. $\beta_T(i)=1$
2. $\beta_{t}(i)=\sum_j\beta_{t+1}(j)a_{ij}p(y_{t+1}|x_j)$
3. $P(Y|\theta)=\sum_i\pi_ip(y_1|x_i)\beta_1(i)$.

### Learning Algorithm

$\max Q(\theta,\theta')=-H(P,P')$ cross-entroy of $X, Y$.

**Baum-Welch Algorithm**

input: $x$, output: $\theta$

1. initialize $\theta_0 = (A_0,B_0,\pi_0)$
2. $a_{ij} :=  \frac{\sum_t\xi_t(i,j)}{\sum_t\gamma_t(i)},b_{jk} :=  \frac{\sum_{t,x_t=k}\gamma_t(i,j)}{\sum_t\gamma_t(i)},\pi:=\gamma_1$
3. until $\theta_{n+1}$



### Predict Algorithm

$\delta_t(i)=\max_{x_1,\cdots,x_{t-1}}P(x_t=i,x_{t-1},\cdots,x_1,y|\lambda)$

$\delta_{t+1}(i)=\max_j(\delta_t(j)a_{ji})p(y_{t+1}|x_i)$

**Viterbi Algorithm**

input: $\theta,y$

output: $x^*$





## CRF



### PGM



pairwise/local/global Markov property.