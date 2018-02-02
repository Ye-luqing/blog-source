---
title: 利用Givens变换将实对称矩阵谱分解
date: 2017-12-30 20:43:47
categories:
- 数学
- 线性代数
tags:
- 对称矩阵
- 谱分解
- Givens变换
- 二次型

---
在博文[逐步转轴法化二次型为标准型](/2017/12/26/逐步转轴法化二次型为标准型/)中,我们通过对变量逐步施行Givens变换,最终将二次型化为标准型.由于二次型与对称矩阵有密不可分的关系,因此这篇文章启示我们,可以利用Givens变换将实对称矩阵化为对角矩阵.

以二次型$f(x,y,z)=2x^{2} + 5y^{2} +5z^{2}+4xy-4xz - 8yz$为例,该二次型可以表达成
$$
\begin{pmatrix}
  x&y&z
\end{pmatrix}
\begin{pmatrix}
  2&2&-2\\\
  2&5&-4\\\
  -2&-4&5
\end{pmatrix}
\begin{pmatrix}
  x\\\
  y\\\
  z
\end{pmatrix}
$$
在博文[逐步转轴法化二次型为标准型](/2017/12/26/逐步转轴法化二次型为标准型/)中,我们使用正交替换
$$
\begin{pmatrix}
  x'\\\
  y'\\\
  z'
\end{pmatrix}=\begin{pmatrix}
  \frac{2 \sqrt{5}}{15}&\frac{4 \sqrt{5}}{15}&\frac{\sqrt{5}}{3}\\\
  -\frac{2 \sqrt{5}}{5}&\frac{\sqrt{5}}{5}&0\\\
  -\frac{1}{3}&-\frac{2}{3}&\frac{2}{3} \end{pmatrix}
\begin{pmatrix}
  x\\\
  y\\\
  z
\end{pmatrix}.
$$把上述二次型化为标准型
\begin{align\*}
  x'^2+y'^2+10z'^2&=
                    \begin{pmatrix}
                      x'&y'&z'
                    \end{pmatrix}
                             \begin{pmatrix}
                               1&0&0\\\
                               0&1&0\\\
                               0&0&10
                             \end{pmatrix}
                                    \begin{pmatrix}
                                      x'\\\
                                      y'\\\
                                      z'
                                    \end{pmatrix}
  \\\&=
      \begin{pmatrix}
        x&y&z
      \end{pmatrix}
             \begin{pmatrix}
               \frac{2 \sqrt{5}}{15}&\frac{4 \sqrt{5}}{15}&\frac{\sqrt{5}}{3}\\\
               -\frac{2 \sqrt{5}}{5}&\frac{\sqrt{5}}{5}&0\\\
               -\frac{1}{3}&-\frac{2}{3}&\frac{2}{3}
             \end{pmatrix}^T
                                          \begin{pmatrix}
                                            1&0&0\\\
                                            0&1&0\\\
                                            0&0&10
                                          \end{pmatrix}
                                                 \begin{pmatrix}
                                                   \frac{2 \sqrt{5}}{15}&\frac{4 \sqrt{5}}{15}&\frac{\sqrt{5}}{3}\\\
                                                   -\frac{2 \sqrt{5}}{5}&\frac{\sqrt{5}}{5}&0\\\
                                                   -\frac{1}{3}&-\frac{2}{3}&\frac{2}{3}
                                                 \end{pmatrix}
                                                                              \begin{pmatrix}
                                                                                x\\\
                                                                                y\\\
                                                                                z
                                                                              \end{pmatrix}.
\end{align\*}
可见,将二次型化为标准型的过程,就是将对称矩阵进行谱分解的过程.而在博文[逐步转轴法化二次型为标准型](/2017/12/26/逐步转轴法化二次型为标准型/)中,正交矩阵$\begin{pmatrix}
  \frac{2 \sqrt{5}}{15}&\frac{4 \sqrt{5}}{15}&\frac{\sqrt{5}}{3}\\\
  -\frac{2 \sqrt{5}}{5}&\frac{\sqrt{5}}{5}&0\\\
  -\frac{1}{3}&-\frac{2}{3}&\frac{2}{3}
\end{pmatrix}$是若干个代表Givens旋转的矩阵的复合,这启发我们,可以使用逐步的Givens旋转矩阵将对称矩阵谱分解.下面举一个例子.


> **例:** 将三阶实对称矩阵$A=
  \begin{pmatrix}
    0&\frac{1}{2}&\frac{1}{2}\\\
    \frac{1}{2}&0&\frac{1}{2}\\\
    \frac{1}{2}&\frac{1}{2}&0
  \end{pmatrix}
$谱分解.


**解**:令$G\_1=
\begin{pmatrix}
  \cos\theta\_1&-\sin\theta\_1&0\\\
  \sin\theta\_1&\cos\theta\_1&0\\\
   0&0&1
\end{pmatrix},
$令
\begin{align\*}
S\_{1}&=G\_1AG\_1^{-1}
\\\&=\begin{pmatrix}
  \cos\theta\_1&-\sin\theta\_1&0\\\
  \sin\theta\_1&\cos\theta\_1&0\\\
   0&0&1
\end{pmatrix}
        \begin{pmatrix}
          0&\frac{1}{2}&\frac{1}{2}\\\
        \frac{1}{2}&0&\frac{1}{2}\\\
        \frac{1}{2}&\frac{1}{2}&0
        \end{pmatrix}
                                 \begin{pmatrix}
                                   \cos\theta\_1&\sin\theta\_1&0\\\
                                   -\sin\theta\_1&\cos\theta\_1&0\\\
                                   0&0&1
                                 \end{pmatrix}
\\\&=
    \begin{pmatrix}
      -\sin\theta\_{1}\cos\theta\_{1}&-\frac{1}{2}\sin^{2}\theta\_{1}+\frac{1}{2}\cos^2\theta\_{1}&\frac{1}{2}\cos\theta\_1-\frac{1}{2}\sin\theta\_1\\\
      -\frac{1}{2}\sin^{2}\theta\_{1}+\frac{1}{2}\cos^{2}\theta\_{1}&\sin\theta\_{1}\cos\theta\_{1}&\frac{1}{2}\sin\theta\_1+\frac{1}{2}\cos\theta\_1\\\
      \frac{1}{2}\cos\theta\_1-\frac{1}{2}\sin\theta\_1&\frac{1}{2}\sin\theta\_1+\frac{1}{2}\cos\theta\_1&0
    \end{pmatrix}.
\end{align\*}
令$\cos\theta\_1=\sin\theta\_{1}=\frac{\sqrt{2}}{2}$,则$S\_{1}$化为矩阵$S\_{1}=
\begin{pmatrix}
  -\frac{1}{2}&0&0\\\
   0&\frac{1}{2}&\frac{\sqrt{2}}{2}\\\
  0&\frac{\sqrt{2}}{2}&0
\end{pmatrix}
$.再令$G\_2=
\begin{pmatrix}
  1&0&0\\\
  0&\cos\theta\_2&-\sin\theta\_2\\\
  0&\sin\theta\_2&\cos\theta\_2
\end{pmatrix},
$令
\begin{align\*}
S\_2&=
G\_2S\_1G\_2^{-1}=
\begin{pmatrix}
  1&0&0\\\
  0&\cos\theta\_2&-\sin\theta\_2\\\
  0&\sin\theta\_2&\cos\theta\_2
\end{pmatrix}
\begin{pmatrix}
  -\frac{1}{2}&0&0\\\
  0&\frac{1}{2}&\frac{\sqrt{2}}{2}\\\
  0&\frac{\sqrt{2}}{2}&0
\end{pmatrix}
\begin{pmatrix}
  1&0&0\\\
  0&\cos\theta\_2&\sin\theta\_2\\\
  0&-\sin\theta\_2&\cos\theta\_2
\end{pmatrix}
\\\&=
    \begin{pmatrix}
      -\frac{1}{2}&0&0\\\
0&\frac{1}{2}\cos^{2}\theta\_2-\sqrt{2}\sin\theta\_2\cos\theta\_2&\frac{1}{2}\sin\theta\_2\cos\theta\_2-\frac{\sqrt{2}}{2}\sin^{2}\theta\_2+\frac{\sqrt{2}}{2}\cos^{2}\theta\_2\\\
0&\frac{1}{2}\sin\theta\_2\cos\theta\_2-\frac{\sqrt{2}}{2}\sin^{2}\theta\_2+\frac{\sqrt{2}}{2}\cos^{2}\theta\_2&\frac{1}{2}\sin^2\theta\_2+\sqrt{2}\sin\theta\_2\cos\theta\_2
    \end{pmatrix}.
\end{align\*}
令$\cos\theta\_{2}=\frac{\sqrt{3}}{3},\sin\theta\_{2}=\frac{\sqrt{6}}{3}$,可得$\frac{1}{2}\sin\theta\_{2}\cos\theta\_{2}-\frac{\sqrt{2}}{2}\sin^{2}\theta\_{2}+\frac{\sqrt{2}}{2}\cos^2\theta\_{2}=0$.此时,矩阵
$$
S\_2=
\begin{pmatrix}
  -\frac{1}{2}&0&0\\\
  0&-\frac{1}{2}&0\\\
  0&0&1
\end{pmatrix}.
$$
因此,
$$
A=G\_1^{-1}S\_1G\_1=G\_1^{-1}G\_2^{-1}S\_2G\_2G\_1=
\begin{pmatrix}
  \frac{\sqrt{2}}{2}&\frac{\sqrt{6}}{6}&\frac{\sqrt{3}}{3}\\\
  -\frac{\sqrt{2}}{2}&\frac{\sqrt{6}}{6}&\frac{\sqrt{3}}{3}\\\
  0&-\frac{\sqrt{6}}{3}&\frac{\sqrt{3}}{3}
\end{pmatrix}
\begin{pmatrix}
  -\frac{1}{2}&0&0\\\
  0&-\frac{1}{2}&0\\\
  0&0&1
\end{pmatrix}
\begin{pmatrix}
  \frac{\sqrt{2}}{2}&-\frac{\sqrt{2}}{2}&0\\\
  \frac{\sqrt{6}}{6}&\frac{\sqrt{6}}{6}&-\frac{\sqrt{6}}{3}\\\
  \frac{\sqrt{3}}{3}&\frac{\sqrt{3}}{3}&\frac{\sqrt{3}}{3}
\end{pmatrix}.
$$