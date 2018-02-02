title: 一阶线性常微分方程与Fourier变换的关系
date: 2015-03-29 20:38:18
categories:
- 数学
- 微分方程
tags:
- Fourier变换
---
我们来看一阶线性常微分方程的初值问题
\begin{equation}
  \label{eq:1}
  \frac{dx}{dt}-2\pi in x=f(t),x(0)=0.
\end{equation}
其中$i$是虚数,$n$是整数.为了解这个初值问题,我们先来给出微分方程
\begin{equation}
  \label{eq:2}
  \frac{dx}{dt}-2\pi inx=f(t)
\end{equation}
的通解.将微分方程\eqref{eq:2}化为
\begin{equation}
  \label{eq:3}
  dx-[2\pi in x+f(t)]dt=0.
\end{equation}
在微分方程\eqref{eq:3}两边同时乘以一个函数$u(t)$,可得
\begin{equation}
  \label{eq:4}
  udx-[2\pi in x+f(t)]udt=0.
\end{equation}
设\eqref{eq:4}是一个恰当微分方程,即
$$
\frac{\partial u}{\partial t}=-2\pi inu.
$$
则解得$u(t)=e^{-2\pi in t}$.因此恰当方程\eqref{eq:4}变为
\begin{equation}
  \label{eq:5}
  e^{-2\pi in t}dx-[2\pi in x+f(t)]e^{-2\pi in t}dt=0.
\end{equation}
设恰当方程\eqref{eq:5}的解为$\phi(x,t)=0$,则
$$
\frac{\partial \phi}{\partial x}=e^{-2\pi int},
$$
于是$\phi(x,t)=e^{-2\pi int}x+g(t)$.而且有
$$
\frac{\partial \phi}{\partial t}=-[2\pi in x+f(t)]e^{-2\pi in t},
$$
即
$$
-2\pi in e^{-2\pi int}x+g'(t)=-[2\pi in x+f(t)]e^{-2\pi in t},
$$
解得
$$
g'(t)=-f(t)e^{-2\pi int} \iff g(t)=-\int\_{0}^{t} f(s)e^{-2\pi ins}ds+C.
$$
其中$C$是常数.因此可得微分方程\eqref{eq:2}的通解为
\begin{equation}\label{eq:6}
x+Ce^{2\pi int}=\int\_{0}^{t} f(s)e^{-2\pi i(n-1)s}ds.
\end{equation}
将初值问题\eqref{eq:1}的初值$x(0)=0$代入通解\eqref{eq:6},可得$C=0$.因此初值问题\eqref{eq:1}的解为
\begin{equation}\label{eq:7}
x=\int\_0^tf(s)e^{-2\pi i(n-1)s}ds.
\end{equation}
由\eqref{eq:7}式可见,$t=1$时的$x$值就是函数$f$的第$n-1$个Fourier系数.

下面我们给出初值问题\eqref{eq:1}的物理意义,这样就能赋予Fourier系数以物理意义了.一复平面上有一个大圆盘.圆盘的圆心位于复平面的原点.圆盘以圆心为中心顺时针相对于复平面以角速度$2\pi n$匀速转动.一质点从复平面原点出发,出发的那一刻时间$t$记为$0$,随着时间流逝,$t$增大.质点相对于复平面的速度是时间的函数,用复数来描述,为$f(t)$.质点的位置用复数记为$x$.由于圆盘以圆心为中心顺时针相对于复平面以角速度$2\pi n$匀速转动,因此平面相对于质点所在的圆盘上的点的速度为$2\pi in x$.根据速度的叠加原理,质点相对于圆盘的速度为$2\pi inx+f(t)$.于是,
$$
\int\_0^1f(s)e^{-2\pi i(n-1)s}ds
$$
的物理意义就是从质点出发经过时间$1$后,质点相对于圆盘的位移.
