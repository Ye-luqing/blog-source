# 轴向仿射的不变直线
在[一般情形下轴向仿射造像方程式之推导](/analytic-geometry-huangyouxun/p377/)和[利用轴向仿射的平面作图法推导仿射造像方程式](/analytic-geometry-huangyouxun/p386/)里, 我们推导出了轴向仿射的造像方程式
\begin{equation}\label{eq:1}
\begin{cases}
  \overline{x}=x+ ry\\\
\overline{y}=ky
\end{cases}.
\end{equation}
其中$r=\frac{c}{a}$,$k=\frac{b}{a}$.下面我们来研究在轴向仿射下不变的直线.不妨设直线$Ax+By+C=0$($A,B$不全为零)在该轴向仿射造像下不变，即，若点$(x\_0,y\_0)$满足
$$
Ax\_0+By\_0+C=0,
$$
则点$(x\_0+ry\_0,ky\_0)$也满足直线方程，即
$$
A(x\_0+ry\_0)+Bky\_0+C=0.
$$
于是,关于$x\_0,y\_0$的方程组
$$
\begin{cases}
  Ax\_0+By\_0+C=0\\\
Ax\_0+(Bk+Ar)y\_0+C=0
\end{cases}
$$
有无数组解.也即，关于$x\_0,y\_0$的方程组
$$
\begin{cases}
  Ax\_0+By\_0+C=0\\\
[B(k-1)+Ar]y\_0=0
\end{cases}.
$$
有无数组解.

当$B(k-1)+Ar\neq 0$时，$y\_{0}=0$.此时为了保证有无数组解，必须有$A=C=0$.即$x$轴在轴向仿射下不变.

当$B(k-1)+Ar=0$时，显然有无数组解.此时,若$r\neq 0$或$k\neq 1$,则直线的方向向量是$(r,k-1)$.即，所有方向向量为$(r,k-1)$的直线在该轴向仿射下也不变.若$r=0$且$k=1$,则此轴向仿射是恒等映射，所有直线在该仿射下保持不变.


# 利用直线的方向向量寻找轴向仿射的不变直线

下面我们利用直线的方向向量寻找轴向仿射的不变直线.设直线$l$经过点$P(x\_0,y\_0)$,且直线的方向向量是$(m,n)$.则直线$l$上任意一点$Q$都可以表示为
$$
(x\_0,y\_0)+t(m,n),t\in\mathbf{R}.
$$
点$Q$在该轴向仿射作用下变成点
$$
\begin{pmatrix}
  1&r\\\
0&k
\end{pmatrix}
\begin{pmatrix}
  x\_0\\\
y\_0
\end{pmatrix}+t
\begin{pmatrix}
  1&r\\\
0&k
\end{pmatrix}
\begin{pmatrix}
  m\\\
n\\\
\end{pmatrix}.
$$
直线$l$在该轴向仿射作用下不变，当且仅当，对于任意的实数$t\neq 0$时，都存在实数$\lambda\_1,\lambda\_{2}$,使得
$$
t
\begin{pmatrix}
  1&r\\\
0&k
\end{pmatrix}
\begin{pmatrix}
  m\\\
n
\end{pmatrix}=\lambda\_{1}
\begin{pmatrix}
  m\\\
n
\end{pmatrix},
$$
且
$$
\begin{pmatrix}
  1&r\\\
0&k
\end{pmatrix}
\begin{pmatrix}
  x\_0\\\
y\_0
\end{pmatrix}-
\begin{pmatrix}
  x\_0\\\
y\_0
\end{pmatrix}=\lambda\_2
\begin{pmatrix}
  m\\\
n
\end{pmatrix}.
$$
即对于任意的实数$t\neq 0$,都存在实数$\lambda\_1,\lambda\_2$,使得
$$
\begin{pmatrix}
  1&r\\\
0&k
\end{pmatrix}
\begin{pmatrix}
  m\\\
n
\end{pmatrix}
=\frac{\lambda\_{1}}{t}
\begin{pmatrix}
  m\\\
n
\end{pmatrix},
$$
且
$$
\begin{pmatrix}
  0&r\\\
0&k-1
\end{pmatrix}
\begin{pmatrix}
  x\_0\\\
y\_0
\end{pmatrix}=\lambda\_2
\begin{pmatrix}
  m\\\
n
\end{pmatrix}.
$$
解得,

+ 当$r\neq 0$或$k\neq 1$时，$(m,n)$可以等于$(r,k-1)$或者$(1,0)$.


> 当$(m,n)$等于$(r,k-1)$时，$(x\_0,y\_0)$可以等于任意实数对.


> 当$(m,n)=(1,0)$且$k=1$时，$(x\_0,y\_0)$也可以等于任意实数对.


> 当$(m,n)=(1,0)$且$k\neq 1$时，$(x\_0,y\_0)$必须位于$x$轴上，即$y\_0$必须为$0$.


+ 当$r=0$且$k=1$时，仿射造像是恒等映射，此时，任意直线在恒等映射下保持不变.