---
title: 证明Ker A^TA=Ker A
date: 2017-11-26 12:05:22
tags:
---
在博文[$A^TA$的秩等于$A$的秩](/2017/09/30/A-TA的秩等于A的秩)中,我们利用初等变换的方法,证明了$A^TA$的秩等于$A$的秩.在这篇博文里,我们说明为什么矩阵$A^TA$的化零空间等于矩阵$A$的化零空间.


**证明**:设矩阵$A$是$m\times n$矩阵.则矩阵$A^T$是$n\times m$矩阵.所以$A^TA$是$n\times n$矩阵.记矩阵$A$的第$i(1\leq i\leq n)$个列向量为$P\_{i}=\begin{pmatrix}
  a\_{1i}\\\
a\_{2i}\\\
\vdots\\\
a\_{mi}
\end{pmatrix}$,矩阵$A^TA$的第$j(1\leq j\leq n)$个列向量为$Q\_j=
\begin{pmatrix}
  b\_{1j}\\\
b\_{2j}\\\
\vdots\\\
b\_{nj}
\end{pmatrix}
$.则由矩阵乘法的定义,$b\_{ki}=P\_k^TP\_i$.设对于实数$\lambda\_1,\lambda\_2,\cdots,\lambda\_n$来说,使得
$$
\lambda\_1Q\_1+\lambda\_2Q\_2+\cdots+\lambda\_nQ\_n=\mathbf{0},
$$
则所有满足上式的$(\lambda\_1,\lambda\_2,\cdots,\lambda\_n)$形成矩阵$A^{T}A$的化零空间.上式可化为
$$
\lambda\_1
\begin{pmatrix}
  P\_1^TP\_1\\\
P\_2^TP\_1\\\
\vdots\\\
P\_n^TP\_1
\end{pmatrix}+\lambda\_2
\begin{pmatrix}
  P\_1^TP\_2\\\
P\_2^TP\_2\\\
\vdots\\\
P\_n^TP\_2
\end{pmatrix}+\cdots+\lambda\_n
\begin{pmatrix}
  P\_1^TP\_n\\\
P\_2^TP\_n\\\
\vdots\\\
P\_n^TP\_n
\end{pmatrix}=
\begin{pmatrix}
  0\\\
0\\\
\vdots\\\
0
\end{pmatrix},
$$
即
$$
\begin{cases}
  P\_1^T(\lambda\_1P\_1+\lambda\_2P\_2+\cdots+\lambda\_nP\_n)=0\\\
  P\_2^T(\lambda\_1P\_1+\lambda\_2P\_2+\cdots+\lambda\_nP\_n)=0\\\
\vdots\\\
P\_n^T(\lambda\_1P\_1+\lambda\_2P\_2+\cdots+\lambda\_nP\_n)=0\\\
\end{cases}.
$$
可见,向量$\lambda\_1P\_1+\lambda\_2P\_2+\cdots+\lambda\_nP\_n$与矩阵$A$的列空间正交,又因为向量$\lambda\_1P\_1+\lambda\_2P\_2+\cdots+\lambda\_nP\_n$属于矩阵$A$的列空间,因此只能有
$$
\lambda\_1P\_1+\lambda\_2P\_2+\cdots+\lambda\_nP\_n=\mathbf{0}.
$$
因此向量$(\lambda\_1,\lambda\_2,\cdots,\lambda\_n)$也属于矩阵$A$的化零空间.所以$\ker A^TA\subset \ker A$.且易得$\ker A\subset \ker A^TA$,因此$\ker A^TA=\ker A$.
