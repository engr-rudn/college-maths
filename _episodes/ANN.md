# ANN

## Perceptron



### Perceptron Convergence thm

If $\exists w^*, f(w^*p(q)) = t(q), \forall q$, then $w\to w^*$ (finite steps)

*Proof.* $X_1:C_1,X_2:C_2$

1. $w^Tp>0, p\in C_1$
2. $w^Tp<0, p\in C_2$ 




## BP net

但我们引入可调节的参数$a,b$, 定义

$$
\phi(x,a,b)=\phi(2\frac{x-a}{b-a}-1),
$$

此时函数支撑集在$[a,b]$上, 通过调整$a,b$两个参数, 可以移动或收缩函数图像------实际上是$\phi$通过伸缩平移得到的. 因此神经网络不再需要阈值, 而且引入了收缩这种变形-----增加了一个参数, 使得网络有更好的适应性. 新激活函数就是建立在这种bump形函数上.

$$
f(x,a,b)=\Phi(2\frac{x-a}{b-a}-1)=\frac{2}{b-a}\int_{a}^x\phi(t,a,b)d t.\\
=\int_{-\infty}^x\phi(t,a,b)d t
$$

### 算法

本节构造改进激活函数的BP算法, 关键是对误差函数求偏导. 网络结构由下面的公式给出
$$
y_k=f(\sum_iW_{ki}x_{i}, a_k,b_k),k=1,\cdots,m.
$$
注意到
$$
\left\{\begin{array}{ll}
{f}_{x}(x,a,b)&=\frac{2}{b-a}\phi(x,a,b),\\
{f}_{a}(x,a,b)&=2\frac{x-b}{(b-a)^2}\phi(x,a,b)=\frac{x-b}{b-a}{f}_{x}(x,a,b),\\
{f}_{b}(x,a,b)&=2\frac{a-x}{(b-a)^2}\phi(x,a,b)=\frac{a-x}{b-a}{f}_{x}(x,a,b).
\end{array}\right.
$$

定义误差函数
$$
E(W,a,b)=\frac{1}{2}\sum_j\|t_j-y_j\|^2, y_{kj}=f(\sum_iW_{ki}x_{ij},a_k,b_k),
$$

其中$\{(x_j,t_j),j=1,\cdots,N\}$是样本$y_j$为$x_j$的输出, 变量第二个下标是样本编号, 第一个下标是变量分量, 根据这两个下标可以样本和输出写成矩阵的形式$X=\{x_{ij}\},T=\{t_{ij}\},y=\{y_{ij}\}$. 根据求导法则, 不难证明
$$
\begin{equation}\label{pd}
\left\{\begin{array}{ll}
{E}_{W}(W,a,b)&=-((T-Y)\circ Y_1)X^T,\\
{E}_{a}(W,a,b)&=-\sum_j((T-Y)\circ Y_2)_j,\\
{E}_{b}(W,a,b)&=-\sum_j((T-Y)\circ Y_3)_j,
\end{array}\right.
\end{equation}
$$

其中矩阵$Y_1=\{{f}_{x}(x_{ij},a_i,b_i)\},Y_2=\{{f}_{a}(x_{ij},a_i,b_i)\},Y_3=\{{f}_{b}(x_{ij},a_i,b_i)\}$. 这里$\circ$表示矩阵的点乘运算（矩阵的Hamadard积）. 有了(\ref{pd}), 我们就可以实现BP 算法了. 为了简化, 可令$D=(T-Y)\circ Y_1$, 则
$$
\begin{equation}\label{simple}
\left\{\begin{array}{ll}
{E}_{W}(W,a,b)&=-DX^T,\\
{E}_{a}(W,a,b)&=-\frac{1}{b-a}\circ\sum_j(D\circ\{x_{ij}-b_i\})_j,\\
{E}_{b}(W,a,b)&=-\frac{1}{b-a}\circ\sum_j(D\circ\{a_i-x_{ij}\})_j.
\end{array}\right.
\end{equation}
$$
