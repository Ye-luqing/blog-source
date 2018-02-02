title: Cauchy-Riemann方程
date: 2016-01-01 17:08:51
categories:
- 数学
- 复分析
tags:
- Cauchy-Riemann方程

---
设$f:\mathbf{C}\to \mathbf{C}$是一个复函数.我们说$f$在点$z\_0\in \mathbf{C}$处复可微,当且仅当存在复数$f'(z\_0)$,使得
\begin{equation}
  \label{eq:1}
  f(z)-f(z\_0)=f'(z\_0)(z-z\_0)+o(z-z\_0),
\end{equation}
其中$\lim\_{z\to z\_0}\frac{o(z-z\_0)}{z-z\_0}=0$.称$f'(z\_0)$为函数$f$在点$z\_0$处的导数.

记$z=x+iy$,$z\_0=x\_0+iy\_0$,$f(z)=u(x,y)+iv(x,y)$,$f'(z\_0)=a+ib$.其中$u(x,y),v(x,y)$为从$\mathbf{R}^2$到$\mathbf{R}$的函数,$x,y,x\_0,y\_0,a,b\in \mathbf{R}$.则式\eqref{eq:1}等价于
\begin{equation}
  \label{eq:2}
  \begin{pmatrix}
    u(x,y)-u(x\_0,y\_0)\\\
v(x,y)-v(x\_0,y\_0)
  \end{pmatrix}=
  \begin{pmatrix}
    a&-b\\\
    b&a
  \end{pmatrix}
  \begin{pmatrix}
    x-x\_0\\\
y-y\_0
  \end{pmatrix}+
  \begin{pmatrix}
    o\_1(x-x\_0,y-y\_0)\\\
o\_2(x-x\_0,y-y\_0)
  \end{pmatrix},
\end{equation}
其中$o\_1(x-x\_0,y-y\_0)+io\_2(x-x\_0,y-y\_0)=o((x-x\_0)+i(y-y\_0))$.式\eqref{eq:2}说明,从$\mathbf{R}^2$到$\mathbf{R}^2$的函数$F:(x,y)\to (u(x,y),v(x,y))$是可微的,且
$$
\begin{pmatrix}
  \frac{\partial u}{\partial x}(x\_0,y\_0)&\frac{\partial u}{\partial y}(x\_0,y\_{0})\\\
\frac{\partial v}{\partial x}(x\_{0},y\_{0})&\frac{\partial v}{\partial y}(x\_0,y\_0)
\end{pmatrix}=
\begin{pmatrix}
  a&-b\\\
b&a
\end{pmatrix}.
$$
可见,
\begin{equation}
  \label{eq:3}
  \frac{\partial u}{\partial x}(x\_0,y\_0)=\frac{\partial v}{\partial
    y}(x\_0,y\_0),\frac{\partial u}{\partial y}=-\frac{\partial v}{\partial x}(x\_0,y\_0).
\end{equation}
这就是Cauchy-Riemann方程.

反之,如果$F:(x,y)\to (u(x,y),v(x,y))$在点$(x\_0,y\_0)$可微,且偏导数满足Cauchy-Riemann方程\eqref{eq:3},则$f$在$z\_0$处复可微.
