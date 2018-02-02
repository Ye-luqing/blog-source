title: 带Peano余项的Taylor公式
date: 2015-11-24 08:49:46
categories:
- 数学
- 单元微积分
tags:
- Taylor公式
- L'Hospital法则

---
带Peano余项的Taylor公式:

---
>若函数$f$在点$x\_0$存在直至$n$阶导数,则有
$$
f(x)=f(x\_0)+f'(x\_0)(x-x\_0)+\frac{f''(x\_0)}{2!}(x-x\_0)^2+\cdots+\frac{f^{(n)}(x\_0)}{n!}(x-x\_0)^n+o((x-x\_0)^n).
$$

---

下面我们采用积分的方法来证明该公式.为此,我们只证明$n=3$的特殊情形,一般情形完全可以类推.

---
>若函数$f$在点$x\_0$存在直至$3$阶导数,则有
\begin{equation}\label{eq:1}
f(x)=f(x\_0)+f'(x\_0)(x-x\_0)+\frac{f''(x\_0)}{2!}(x-x\_0)^2+\frac{f^{(3)}(x\_0)}{3!}(x-x\_0)^3+o((x-x\_0)^3).
\end{equation}

---

**证明**:由于$f$在$x\_0$处$3$阶可导,因此
\begin{equation}\label{eq:2}
f^{(2)}(x)=f^{(2)}(x\_0)+f^{(3)}(x\_0)(x-x\_0)+o\_{1}(x-x\_0),
\end{equation}
将\eqref{eq:2}两边从$x\_0$到$x$进行积分,可得
\begin{equation}
  \label{eq:3}
  \int\_{x\_0}^xf^{(2)}(t)dt=f^{(2)}(x\_{0})(x-x\_0)+\frac{1}{2}f^{(3)}(x\_{0})(x-x\_0)^{2}+\int\_{x\_0}^xo\_1(t-x\_0)dt.
\end{equation}
由微积分第一基本定理,\eqref{eq:3}可以化为
$$
  f'(x)-f'(x\_0)=f^{(2)}(x\_{0})(x-x\_0)+\frac{1}{2}f^{(3)}(x\_{0})(x-x\_0)^{2}+\int\_{x\_0}^xo\_1(t-x\_0)dt,
$$
也即,
\begin{equation}
  \label{eq:4}
  f'(x)=f'(x\_{0})+f^{(2)}(x\_{0})(x-x\_0)+\frac{1}{2}f^{(3)}(x\_{0})(x-x\_0)^{2}+\int\_{x\_0}^xo\_1(t-x\_0)dt,
\end{equation}
其中$\int\_{x\_0}^xo\_1(t-x\_0)dt$至少是关于$x-x\_0$的二阶无穷小量,这是因为由L'Hospital法则,
$$
\lim\_{x\to x\_0}\frac{\int\_{x\_0}^x
  o\_1(t-x\_0)dt}{(x-x\_0)^{2}}=\lim\_{x\to x\_0}\frac{o\_1(x-x\_0)}{2(x-x\_0)}=0.
$$
再将式\eqref{eq:4}两边积分,可得
\begin{equation}
  \label{eq:5}
  \int\_{x\_0}^xf'(t)dt=f'(x\_0)(x-x\_0)+\frac{1}{2}(x-x\_0)^2f^{(2)}(x\_0)+\frac{1}{6}(x-x\_0)^3f^{(3)}(x\_0)+\int\_{x\_{0}}^{x}\int\_{x\_0}^po\_1(t-x\_0)dtdp,
\end{equation}
由微积分第一基本定理,式\eqref{eq:5}可以写为
$$
f(x)-f(x\_0)=f'(x\_0)(x-x\_0)+\frac{1}{2}(x-x\_0)^2f^{(2)}(x\_0)+\frac{1}{6}(x-x\_0)^3f^{(3)}(x\_0)+\int\_{x\_{0}}^{x}\int\_{x\_0}^po\_1(t-x\_0)dtdp,
$$
即
$$
f(x)=f(x\_0)+f'(x\_0)(x-x\_0)+\frac{1}{2}(x-x\_0)^2f^{(2)}(x\_0)+\frac{1}{6}(x-x\_0)^3f^{(3)}(x\_0)+\int\_{x\_{0}}^{x}\int\_{x\_0}^po\_1(t-x\_0)dtdp.
$$
其中$\int\_{x\_{0}}^{x}\int\_{x\_0}^po\_1(t-x\_0)dtdp$至少是关于$x-x\_0$的三阶无穷小量,这是因为由L'Hospital法则,
$$
\lim\_{x\to
  x\_0}\frac{\int\_{x\_{0}}^{x}\int\_{x\_0}^po\_1(t-x\_0)dtdp}{(x-x\_0)^3}=\lim\_{x\to
x\_0}\frac{\int\_{x\_0}^xo\_1(t-x\_0)dt}{3(x-x\_0)^2}=\lim\_{x\to x\_0}\frac{o\_1(x-x\_0)}{6(x-x\_0)}=0.
$$
