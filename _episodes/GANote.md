# 遗传算法

## 介绍

### 基本概念:

基因、个体、种群

### 种群空间:

个体$x \in G_1\times\cdots\times G_n$, 其中$G_i$是$I$的第$i$位基因集合.

$H=G_1\times\cdots\times G_n$或符合一定条件的子集为个体空间. 它的子集、或定义其上的序列称为种群.

形如$(x,x,x,\cdots)$的种群称为齐次种群.

母体: $P^2$.

### 适应度函数

种群适应度$F(P)=\sum_{x_i} F(x_i),P=(x_1,\cdots,x_n)$, 对应的集合依然用$P$表示.

## 比例选择算子

$S(x_1,\cdots,x_m)=(X_1,\cdots,X_n):P^m\to R(P)$, 其中$X_k$的分布为
$$P\{X_k=x_i\}=\frac{N_iF(x_i)}{F(x)},$$
$N_i:=\sharp\{x_j\in P|x_j=x_i\}$.

最优个体$B(P)=\{x\in P, f(x)=\max f(P)\}$,
$n(P):=\sharp\{x_j\in B(P)\}$. $B^*=B(S)$.

广义最优个体$B(P,\epsilon)=\{x\in P, f(x)\geq \max f(P)-\epsilon\}$, $B^*(\epsilon)=B(S,\epsilon)$.

### 选择压

$\rho(P):=\max\{\frac{f(x_i)}{f(x_j)},f(x_i)<f(x_j),x_i,x_j\in P\}$. 

### 基本性质

设$\sharp P=m$,

1. $F(P)=n(P)f^*(P)+\sum_{x\not\in B(P)}f(x)$.

2. $P(S(x)\subset B(I))=(\frac{n(P)f^*(P)}{F(x)})^n\geq(1-\frac{m-n(x)\rho}{n(x)+(m-n(x))\rho})^n$.


### 杂交算子

单点杂交操作$c(a_1\cdots a_l,b_1\cdots b_l, i)=a_1\cdots a_i b_{i+1}\cdots b_l$. 多点形式.


1. 单点杂交算子,

   $$P\{C(x,y)=z\}=\begin{cases}\frac{ap}{l}, &z\neq x,\\ (1-p)+\frac{ap}{l},&z=x,\end{cases}$$

   其中$a(i,j,k)$杂交生成$k$的基因位数.

2. 均匀杂交算子. $c(a_1\cdots a_l,b_1\cdots b_l)=c_1\cdots c_l$, $c_i=a_i$ 或 $b_i$.

### 变异算子

单点变异操作$m(a_1\cdots a_l, i, b)=a_1\cdots a_{i-1}ba_{i+1}\cdots a_l$.

### 基本性质

均匀变异$P\{M(x)=y\}=p^d(1-p)^{l-d}=\prod_i(0.5+(\delta_{x_i,y_i}-0.5)(1-2\mu)), d=d(x,y)$. Hammin距离.

## GA 过程分析

### 选择过程

$F:X\mapsto X$.
$P\{F(X)=x\}=\frac{f(x)p(x)}{F(X)},F(X)=\sum_x f(x)p_x=Ef(X)$.
根据$F$选择$n$代后的个体分布$X_n$为
$P(X_n=x)=F^{(n)}(X)_x=\frac{f^n(x)p(x)}{\sum_xf^n(x)p_x}$.

#### 定理 1

令$P_0:=\{x\in P,p(x)>0\},P_1:=\{x\in P_0|f(x)=\max f(P_0)\}$.

$\bar{p}(x)=\lim_n P(X_n=x)=\begin{cases}\frac{p_x}{\sum_{x\in P_1}p_x}, &x\in P_1,\\ 0,&x\not\in P_1.\end{cases}$
$\sum_x|P(X_n=x)-\bar{p}(x)|\leq c\lambda^{n}$, 其中$\lambda=\max\{f(x),x\not\in P_1\}/f^*$（最优选择压）.

可取$c=2\frac{\sum_{x\not\in P_1}p(x)}{\sum_{x\in P_1}p(x)}$.

#### 定理 2

$X\in U(P), \sharp P=N$.

$\bar{p}(x)=\begin{cases}\frac{1}{\sharp P_1}, &x\in P_1,\\ 0,&x\not\in P_1.\end{cases}​$
$\sum_x|P(X_n=x)-\bar{p}(x)|=2-2\sharp P_1\frac{(f^*)^n}{\sum_{x\in P_0}f^n(x)}\leq 2(\frac{N}{\sharp P_1}-1)\lambda^n$.

### 变异过程

$M:X\mapsto MX$.

$P\{X_n=x\}=\sum_{y\in P}\prod_{s=1}^l(0.5+(\delta_{x_s,y_s}-0.5)(1-2\mu)^n)$.