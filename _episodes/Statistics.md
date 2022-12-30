# Statistics

## Linear Regression Analysis

### model
$$Y=\beta_0+\sum_{i=1}^m\beta_iX_i+\epsilon,\epsilon\sim N(0,\sigma^2).$$

### samples
$Y=(Y_1,\cdots,Y_n).$
$Y=X\beta+\epsilon, rank Y=m.$ (assume $X$ is col full rank)

### LSE
$$\min_\beta \|Y-X\beta\|^2$$

$\hat{\beta}=(X^TX)^{-1}X^TY, \hat{Y}=X\hat{\beta}$.

$\hat{\sigma^2}=\frac{\|e\|^2}{n-p},e=Y-\hat{Y}$.


### statistics

#### SS table
$SST=SSE+SSR$:
$SST:=\sum_i(Y_i-\bar{Y})^2, SSE :=\sum_i(Y_i-\hat{Y}_i)^2, SSR=\sum_i(\bar{Y}-\hat{Y}_i)^2$. $MSR=\frac{SSR}{p-1},MSE=\frac{SSE}{n-p}$.

freedom: $(n-1)=(n-p)+(p-1)$.

#### test 1 $H: \beta_1=\cdots=\beta_{p-1}=0$
$F=\frac{MSR}{MSE}\sim F(p-1,n-p)$.


#### test 2 $H: \beta_k=0$
$S(\hat{\beta}):=MSE(X^TX)^{-1}$.
$\frac{\hat{\beta_k}-\beta_k}{\sqrt{S_{kk}}}\sim t(n-p)$.


#### prediction
$S(\hat{Y_0}):=MSE(1+x_0^T(X^TX)^{-1})x_0$.
$\frac{\hat{Y_0}-Y_0}{\sqrt{S}}\sim t(n-p)$.
$Y_0\sim \hat{Y_0}\pm t_{\frac{\alpha}{2}}(n-p)\sqrt{S(\hat{Y_0})}$.

### General test method

#### test $H_0$: conditions of $\beta_i$ hold

$F=\frac{SSE(R)-SSE(F)}{f_R-f_F}/\frac{SSE(F)}{f_F}\sim F(f_R-f_F, f_F)$.

$SSR(B|A)=SSE(A)-SSE(A,B)$.

### programming

[ordinary least squares](http://www.statsmodels.org/stable/regression.html)



### error analysis

MSE is est. of $\sigma^2$. $\frac{e_i}{\sqrt{MSE}}\to N(0,1),n\to\infty$.

$(q_i,e_i)$: normal prob graph.

### opt regression eq

#### Introduction
Select a subset $\{X_{i_k}\}$ from $\{X_i\}$

#### $R^2$ & Adj. $R^2$
$R^2_p=\frac{SSR_p}{SST}=1-\frac{SSE_p}{SST}, R^2_p=1-\frac{n-1}{n-p}\frac{SSE_p}{SST}$.

* $\max R_p$, add $X_i$ until $R_p$ increases insignificantly
* $\max R_a$

#### Mallows' $C_p$
$C_p;=\frac{SSE_p}{MSE(\{X_{i_k}\})}-(n-2p), EC_p\sim p$

#### Allen's $PRESS_p$

$PRESS_p=\sum_id_i^2$,
$d_i=\frac{e_i}{1-h_{ii}}$




## PCA

### pca of pop.
cov matrix: $\Sigma=Cov(X,X)\geq 0$. $\Gamma =e^T\Sigma e$.

### Def of PC
$$
\max Var Y_i, Y_i=Xl_i, 
\\
\|l_i\|=1, Cov(Y_i, Y_k)=0 (l_i\perp_\Sigma l_k),k<i, i=1, \cdots, p.
$$

$i$-PC $Y_i=Xe_i$. PCs $Y=Xe$.

### Def of contribution

$\lambda_i=Var(Y_i)=e_i^T\Sigma e_i$

$\frac{\lambda_k}{\sum_i\lambda_i},\frac{\sum_{i\leq m}\lambda_i}{\sum_i\lambda_i}$.

### with corr
cov matrix: $\rho=corr(X,X)\geq 0$. $\rho =e^T\Sigma e$.
contribution: $\frac{\lambda_i}{p},\frac{\sum_i\lambda_i}{p}$.

### pca of sample, estimate of Y

$\hat{Y}=X\hat{e}, \hat{S}=Cov(x,x)$. $\Gamma =\hat{e}^T \hat{S} \hat{e}$. contribution: $\frac{\hat{\lambda}_k}{\sum_i\hat{\lambda}_i},\frac{\sum_{i\leq m}\hat{\lambda}_i}{\sum_i\hat{\lambda}_i}$.

### programming

[statsmodels for pca](http://www.statsmodels.org/stable/generated/statsmodels.multivariate.pca.PCA.html)

[wiki for pca](https://en.wikipedia.org/wiki/Principal_component_analysis)

```python
# data: n X p - array
# not standardized, not normalized
# data: Variables in columns, observations in rows
pc = PCA(data, ncomp=p:int, standardize=False, normalize=False) # Y=Xe
pc.loadings: e^
pc.factors: Y^
# pc.factors == data (demean) * pc.loadings
# pc.coeff = pc.loadings ^ -1

# principle of matrix analysis:  U S V' = D
U, s, V = LA.svd(np.cov(data.T), full_matrices=True)
PC = data @ V.T
# V.T == loadings
```



## canonical corr analysis

### canonical  corr of pop

### Theorem
$Cov(X)=\Sigma_{11},Cov(Y)=\Sigma_{22},Cov(X,Y)=\Sigma_{12},Cov(Y,X)=\Sigma_{21}$.

$$U_k=e_k^T\Sigma_{11}^{-\frac{1}{2}}X, V_k=f_k^T\Sigma_{22}^{-\frac{1}{2}}Y,$$
and canonical corr: $\rho_{U_k,V_k}=\rho_k$, where $\rho_k^2\in \sigma(A)$ (wrt $e_k$), and $f_k$ is eigvec of $B$,

$$A=\Sigma_{11}^{-\frac{1}{2}}\Sigma_{12}\Sigma_{22}^{-1}\Sigma_{21}\Sigma_{11}^{-\frac{1}{2}},B=\Sigma_{22}^{-\frac{1}{2}}\Sigma_{21}\Sigma_{11}^{-1}\Sigma_{12}\Sigma_{22}^{-\frac{1}{2}}.$$

### canonical corr (estimate)

estimate $\hat{e},\hat{f}$ with cov of samples.

### Bartlett testing
$H_k:\rho_k=0$, $A_1\sim \chi^2((p-k+1)(q-k+1))$
$$W_1=\prod_{i=k}^p(1-\hat{\rho}_i^2),A_k=-(n-k-(p+q+1)/2)\ln W_1$$


## ANOVA

### principle
$TSS=FSS+ESS=\sum_{ij}(y_{ij}-\bar{y})^2, ESS=\sum_{ij}(y_{ij}-\bar{y}_j)^2, FSS=\sum_{j}N_j(\bar{y}_{j}-\bar{y})^2$

$H_0:\mu_j=\mu$ then $F=\frac{MSR}{MSE}\sim F(M-1,N-M)$.

## Inference

### inference quantile (sign)

* $H_0:M_p=M_0$, test: $2P(K\leq k|n',p)\leq \alpha$
* $H_0:M_p\leq M_0$, test: $P(S^-< k|n',p)\leq \alpha$
* $H_0:M_p\geq M_0$, test: $P(S^+< k|n',p)\leq \alpha$

### Cox-Staut test

$H_0$: no trend, test: $2P(K\leq k)\leq \alpha, K=\min\{S^+,S^-\}$,
$S^{+(-)}=\sharp\{i,x_i>(<)x_{i+c}\}$.

## Rank method

### Def. of Rank

$R_i=\sharp\{X_j \leq X_i, j=1,\cdots\}, \bar{R}_i =R_{i-1} +\frac{G_i+1}{2}$.

$R_i^*=\sharp\{X_j< X_i, j=1,\cdots,\lor X_i=X_j, j\leq i\}$.

where $G_i=\sharp \{X_j=X_{(\tau_j)}\}$.



### U stat.

$\theta - UE\to h(X_1,\cdots, X_k) - mean \to U(X_1,\cdots, X_n)$



### Wilcoxon rank test

rank of 1th group: $S_1<\cdots <S_n$, rank of 2nd: $R_1<\cdots <R_m$, $m+n=N$. $W=\sum_i S_i$ (Wilcoxon's rank sum)

$H_0: P(W=w)=\frac{\sharp\{W=w\}}{C_N^n}$

### Brown-Mood test

$H_0: med_X=med_Y$,

$A=\sharp\{X_i>M_{XY}\}\sim HG(m+n,m,t)$.

### Wilcoxon rank-sum statistic
$W_Y=\sum_iR_i, R_i=\sharp\{X_k<Y_i\}+\sharp\{Y_k<Y_i\}+1$ rank in $X_i, Y_i$.

### Mann-Whitney statistic
$W_Y=W_{XY}+\frac{n(n+1)}{2}$;
$W_{XY}=\sharp\{X_i<Y_j\},W_{YX}=\sharp\{Y_j<X_i\}$.

#### Facts
$W_{XY}+W_{YX}=mn$.

