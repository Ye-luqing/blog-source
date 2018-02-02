---
title: 直观理解正交矩阵Q的公式QQ^T=I
date: 2017-12-12 16:28:50
categories:
- 数学
- 线性代数
tags:
- 正交矩阵
- 射影矩阵

---
我们知道,若$Q$是一个$n$阶正交方阵,则有$Q^TQ=I$.这是正交矩阵的定义.由此定义,可得$Q(Q^TQ)=Q$,即
\begin{equation}\label{eq:1}(QQ^T)Q=Q.\end{equation}
在方程\eqref{eq:1}的两边同时右乘$Q^{-1}$,可得$(QQ^T)QQ^{-1}=QQ^{-1}=I$,即$QQ^T=I$.这样我们就用代数方法简洁地说明了$QQ^T=I$.

下面我们用几何观点更好地理解为什么$QQ^T=I$.这里主要是受到了Gilbert Strang的《线性代数及其应用》中文第二版练习3.3.3的启发.记$Q=
\begin{pmatrix}
  a\_{11}&a\_{12}&\cdots&a\_{1n}\\\
  a\_{21}&a\_{22}&\cdots&a\_{2n}\\\
  \vdots&\vdots&\cdots&\vdots\\\
  a\_{n1}&a\_{n2}&\cdots&a\_{nn}
\end{pmatrix},
$且记$P\_i=
\begin{pmatrix}
  a\_{i1}\\\
  a\_{i2}\\\
  \vdots\\\
 a\_{in}
\end{pmatrix}
$.则
$$
QQ^{T}=P\_1P\_1^T+P\_2P\_2^T+\cdots+P\_nP\_n^T.
$$
对于任意一个$n$维向量$x=
\begin{pmatrix}
  x\_1\\\
x\_2\\\
\vdots\\\
x\_n
\end{pmatrix}
$来说,
$$
QQ^{T}x=P\_1P\_1^Tx+P\_2P\_2^Tx+\cdots+P\_nP\_n^Tx.
$$
而对于任意$1\leq i\leq n$来说,$P\_iP\_i^Tx$的意思是向量$x$在单位向量$P\_i$上的射影向量.由于向量$P\_1,P\_2,\cdots,P\_n$是互相正交的单位向量,它们张成$\mathbf{R}^n$,因此$x$在$P\_1,P\_2,\cdots,P\_n$上的投影向量的和必为$x$本身,即对于任意$x\in \mathbf{R}^{n}$,
$$
QQ^Tx=P\_1P\_1^Tx+P\_2P\_2^Tx+\cdots+P\_nP\_n^Tx=x.
$$
因此$QQ^T$只能是单位矩阵$I$.