title: 利用矩阵的Jordan分解求线性递推数列的通项公式
date: 2015-05-25 15:20:08
categories:
- 数学
- 线性代数
tags:
- Jordan标准型
- 线性递推数列
- 叶立军《初等数学研究》
---
下面这道题目改编自叶立军主编的《初等数学研究》例4.3.3(原题叙述啰嗦,我简化了).

>已知数列$\\{a\_n\\}$满足条件$$a\_{n+2}=3a\_{n+1}-3a\_n+a\_{n-1},n=2,3,4,\cdots$$且$a\_1=1$,$a\_2=4$,$a\_3=9$.求数列$\\{a\_n\\}$的通项公式.

--------
>**解**:题目中涉及线性递推关系式.将递推关系用矩阵表达为
\begin{equation}
  \label{eq:1}
  \begin{pmatrix}
    a\_{n+2}\\\
a\_{n+1}\\\
a\_n
  \end{pmatrix}=
  \begin{pmatrix}
    3&-3&1\\\
    1&0&0\\\
    0&1&0
  \end{pmatrix}
  \begin{pmatrix}
    a\_{n+1}\\\
a\_n\\\
a\_{n-1}
  \end{pmatrix}.
\end{equation}
>下面我们将矩阵
$$
A=  \begin{pmatrix}
    3&-3&1\\\
    1&0&0\\\
    0&1&0
  \end{pmatrix}
$$
>进行Jordan分解成$A=M^{-1}JM$的形式,其中$J$是Jordan块.下面我们参照文章[幂零自同态分解定理](/2015/05/21/幂零自同态分解定理)的原理和文章[幂零自同态的结构](/2015/05/25/幂零自同态的结构)的步骤将矩阵进行Jordan分解.为此,首先求矩阵$A$的特征值.易得其特征值只有一个,为$1$.它的特征多项式为
$$
p(x)=(1-x)^3.
$$
>$\mathbf{C}^3$的一个三维线性子空间是$\ker (T-I)^3$,其中$A$是线性变换$T$在标准正交基下的矩阵.于是$\mathbf{C}^{3}=\ker (T-I)^{3}$.于是,$(A-I)^3$是个零矩阵,且对于一切$(A-I)^p=\mathbf{0}$,$p$的最小值为$3$.


>我们先求$\ker (T-I)$.为此我们来看线性方程组
$$
\begin{pmatrix}
  2&-3&1\\\
  1&-1&0\\\
  0&1&-1
\end{pmatrix}
\begin{pmatrix}
  x\\\
  y\\\
 z
\end{pmatrix}=
\begin{pmatrix}
  0\\\
0\\\
0\\\
\end{pmatrix}.
$$
>解得$\dim\ker (T-I)=1$,且$\mathbf{v}\_{1}=(1,1,1)\in \ker (T-I)$.


>然后我们来看$\mathbf{C}^3$的一组基$\\{\mathbf{v}\_1=(1,1,1),\mathbf{v}\_2=(1,0,0),\mathbf{v}\_3=(0,1,0)\\}$.$\\{(T-I)\mathbf{v}\_2,(T-I)(\mathbf{v}\_3)\\}=\\{(2,1,0),(-3,-1,1)\\}$线性无关,是$(T-I)(\mathbf{C}^3)$的一组基.而且$(T-I)(\mathbf{C}^3)$的另外一组基为$\\{\mathbf{v}\_1^{(1)},\mathbf{v}\_2^{(1)}\\}$,其中$\mathbf{v}\_1^{(1)}=\mathbf{v}\_1=(1,1,1)$,$\mathbf{v}\_2^{(1)}=(-1,0,1)$.


>$(T-I)^2(\mathbf{C}^3)$的一组基为$\\{(T-I)(\mathbf{v}\_2^{(1)})\\}=\\{(-1,-1,-1)\\}$.$(T-I)^2(\mathbf{C}^3)$的另外一组基为$\\{\mathbf{v}\_{1}^{(2)}\\}=\\{\mathbf{v}\_1\\}=\\{(1,1,1)\\}$.


>下面,我们寻找向量$\mathbf{w}\_1$,使得$(T-I)(\mathbf{w}\_1)=\mathbf{v}\_1^{(2)}=\mathbf{v}\_1=(1,1,1)$.易得$\mathbf{w}\_1$可以为$(2,1,0)$.再寻找$\mathbf{w}\_2$,使得$(T-I)(\mathbf{w}\_2)=\mathbf{w}\_1$,解得$\mathbf{w}\_2$可以为$(1,0,0)$.


>于是,线性变换$T-I$在有序基$\alpha=(\mathbf{v}\_1,\mathbf{w}\_1,\mathbf{w}\_2)$下的矩阵为
$$
[T-I]\_{\alpha}^{\alpha}=\begin{pmatrix}
  0&1&0\\\
 0&0&1\\\
0&0&0
\end{pmatrix}.
$$
>于是线性变换$T$在有序基$\alpha$下的矩阵就是Jordan块
$$
J=\begin{pmatrix}
  1&1&0\\\
 0&1&1\\\
0&0&1
\end{pmatrix}.
$$
>下面我们来求$[I]\_{\alpha}^{\beta}$,其中$\beta=((1,0,0),(0,1,0),(0,0,1))$是标准正交基.易得
$$
M^{-1}=[I]\_{\alpha}^{\beta}=
\begin{pmatrix}
  1&2&1\\\
  1&1&0\\\
  1&0&0
\end{pmatrix}.
$$
>且
$$
M=[I]\_{\beta}^{\alpha}=
\begin{pmatrix}
  0&0&1\\\
  0&1&-1\\\
 1&-2&1
\end{pmatrix}.
$$
>这样我们就得到了矩阵的分解
$$
\begin{pmatrix}
  3&-3&1\\\
  1&0&0\\\
  0&1&0
\end{pmatrix}=
\begin{pmatrix}
  1&2&1\\\
  1&1&0\\\
  1&0&0
\end{pmatrix}
\begin{pmatrix}
  1&1&0\\\
 0&1&1\\\
0&0&1
\end{pmatrix}
\begin{pmatrix}
  1&2&1\\\
  1&1&0\\\
  1&0&0
\end{pmatrix}^{-1}.
$$
>于是,表达式\eqref{eq:1}变为
\begin{equation}
  \label{eq:2}
  \begin{pmatrix}
      a\_{n+2}\\\
      a\_{n+1}\\\
      a\_n
  \end{pmatrix}=
\begin{pmatrix}
  1&2&1\\\
  1&1&0\\\
  1&0&0
\end{pmatrix}
\begin{pmatrix}
  1&1&0\\\
 0&1&1\\\
0&0&1
\end{pmatrix}
\begin{pmatrix}
  1&2&1\\\
  1&1&0\\\
  1&0&0
\end{pmatrix}^{-1}
\begin{pmatrix}
  a\_{n+1}\\\
  a\_n\\\
  a\_{n-1}
\end{pmatrix}.
\end{equation}
>因此,$\forall n\geq 1$,
\begin{equation}
  \label{eq:3}
  \begin{pmatrix}
    a\_{n+2}\\\
    a\_{n+1}\\\
    a\_n
  \end{pmatrix}=\begin{pmatrix}
  1&2&1\\\
  1&1&0\\\
  1&0&0
\end{pmatrix}
\begin{pmatrix}
  1&1&0\\\
 0&1&1\\\
0&0&1
\end{pmatrix}^{n-1}
\begin{pmatrix}
  1&2&1\\\
  1&1&0\\\
  1&0&0
\end{pmatrix}^{-1}
\begin{pmatrix}
  a\_3\\\
a\_2\\\
a\_1
\end{pmatrix}.
\end{equation}
而
$$
\begin{pmatrix}
  1&1&0\\\
  0&1&1\\\
  0&0&1
\end{pmatrix}^{n}=
\begin{pmatrix}
  1&n&\frac{(n-1)n}{2}\\\
  0&1&n\\\
  0&0&1
\end{pmatrix}.
$$
>因此,最终可得$a\_n=n^2$.
