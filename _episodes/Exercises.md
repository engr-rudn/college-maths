Exercises
=========

# Real analysis

## AC
$f\in AC \iff$ $\forall\epsilon>0\exists C>0\forall [a_i,b_i],i=1,\cdots n$ (unjoined) that 
$$\sum_i |f(b_{i})-f(a_{i})|\leq C\sum_i |b_{i}-a_{i}|+\epsilon.$$


## SC
Define $R(a,b):=\{a\leq |x|\leq b\}$.

Suppose $g\in L^1(R(a,b))$, $f(r)\in C[a,b]$, where $0\leq a<b<\infty$, Let
$$G(r)=\int_{R(a,r)} g(x) dx,$$
then 
$$\int_{R(a,b)} g(x)f(|x|)dx=\int_a^b f(r)dG(r)$$


## SC'
Suppose $g\in L^1$, $f(r)\in C[a,b]$, Let
$$G(r)=\int_{R(0,r)} g(x) dx,$$
then 
$$\int g(x)f(|x|)dx=\int f(r)dG(r)$$



## rearrangement

$f^*=\sup\{f(x)\leq y\}$ (or $f^*=\inf\{f(x)\geq y\}$)

discusss the properties of $f^*$, when $f$ is inc.

* $f^*$ is inc
* $f$ inc $\Rightarrow$ $f^*$ inc, rc (or lc)

*Proof.*
$\alpha(\beta)=\sup_x\{f(x)\leq y_0(<y_1)\}$. $\exists x_1,y_0<f(x_1)< y_1, \alpha<x_1<\beta$. (intrivial case)
If $f$ is inc, then $\gamma:=f^*(y_2)=\sup\{f(x) \leq y_2< f(x_1)>y_0\}>\alpha,x_1=\alpha+$.