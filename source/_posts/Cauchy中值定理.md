title: Cauchy中值定理
date: 2015-11-28 21:45:41
categories:
- 数学
- 单元微积分

tags:
- Cauchy中值定理

---
>**Cauchy中值定理:**设$x=x(t)$和$y=y(t)$是闭区间$[a,b]$上的连续,在开区间$(a,b)$上可微的函数.那么存在点$\eta\in (a,b)$,使得
\begin{equation}\label{eq:1}
\begin{vmatrix}
  x'(\eta)&x(b)-x(a)\\\
y'(\eta)&y(b)-y(a)
\end{vmatrix}=0.
\end{equation}
>如果对于任意$t\in (a,b)$ 有$x'(t)\neq 0$,则$x(a)\neq x(b)$且成立等式
\begin{equation}\label{eq:2}
\frac{y(b)-y(a)}{x(b)-x(a)}=\frac{y'(\eta)}{x'(\eta)}.
\end{equation}

----

**证明**:首先,我们证明,集合$A=\\{((x(t),y(t)):t\in [a,b]\\}$是$\mathbf{R}^2$上的闭集.也就是证明集合$A$的任意极限点$P$仍然属于集合$A$,也即证明,若存在$A$中的点列
$$
(x(t\_1),y(t\_1)),(x(t\_2),y(t\_2)),\cdots,((x(t\_n),y(t\_n)),\cdots
$$
使得$\lim\_{n\to\infty}((x(t\_n),y(t\_n))=P$,则有$P\in A$.为此我们只要证明存在$t\_0\in [a,b]$,使得$f((x\_0,y\_0))=P$即可.取集合
$$
\\{t\_1,t\_2,\cdots,t\_n,\cdots\\}
$$
的一个极限点$t\_0$,由于$[a,b]$是$\mathbf{R}$上的闭集,因此$t\_0\in [a,b]$.由于$x=x(t),y=y(t)$是连续函数,因此$(x(t\_0),y(t\_0))=\lim\_{n\to\infty}((x(t\_n),y(t\_n))=P$.因此$A$是$\mathbf{R}^2$上的闭集.

考虑闭集合$A$和闭集合$B=\\{t(x(a),y(a))+(1-t)(x(b),y(b)):t\in [0,1]\\}$.集合$A$上必定存在到集合$B$距离最大的点$F$.若这个最大距离为$0$,则$A=B$,此时$A$就是一条线段,命题肯定成立.否则,$A$上与$B$距离最大的点必定为$(x(\eta),y(\eta))$,其中$\eta\in (a,b)$.

向量$(x'(\eta),y'(\eta))$必与向量$(x(b)-x(a),y(b)-y(a))$共线.否则,$(x(\eta),y(\eta))$不会是与线段$B$距离最大的点.这就有式\eqref{eq:1}成立.

下面我们证明式\eqref{eq:2}.由式\eqref{eq:1},我们其实只用证明当$x'(t)\neq 0$时,$x(a)\neq x(b)$即可.若$x(a)=x(b)$,则结合$x'(t)\neq 0$和式\eqref{eq:1},必有$y(a)=y(b)$,这表明集合$A$是封闭闭曲线,该封闭闭曲线最右端和最左端处,横坐标关于$t$的导数是零,矛盾.因此$x(a)\neq x(b)$.
