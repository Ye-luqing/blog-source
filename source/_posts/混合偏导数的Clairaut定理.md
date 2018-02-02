title: 混合偏导数的Clairaut定理
date: 2015-02-23 20:29:44
categories:
- 数学
- 多元微积分
tags:
- Clairaut定理
- Lagrange中值定理
- Fubini定理
- Green定理

---
混合偏导数的Clairaut定理叙述如下:
> **(Clairaut定理)**设$E$是$\mathbf{R}^n$的开子集合,并设$f:\mathbf{E}\to\mathbf{R}^{m}$是$E$上的二次连续可微函数.那么对于一切$x\_0\in E$和$1\leq i,j\leq n$,$$\frac{\partial }{\partial x\_j}\frac{\partial f}{\partial x\_i}(x\_0)=\frac{\partial }{\partial x\_i}\frac{\partial f}{\partial x\_j}(x\_0).$$

------------
>**证明:**不妨设 $j<i$.设 $x\_0$ 在 $\mathbf{R}^n$ 中的坐标为$(a\_1,a\_2,\cdots,a\_n)$.我们主要来看表达式\begin{equation}\label{eq:1}\frac{\frac{f(a\_1,\cdots,a\_j+\Delta x\_j,\cdots,a\_i+\Delta x\_i,\cdots,a\_n)-f(a\_1,\cdots,a\_j+\Delta x\_j,\cdots,a\_i,\cdots,a\_n)}{\Delta x\_i}-\frac{f(a\_1,\cdots,a\_j,\cdots,a\_i+\Delta x\_i,\cdots,a\_n)-f(a\_1,\cdots,a\_i,\cdots,a\_n)}{\Delta x\_i}}{\Delta x\_j}.\end{equation}如果先让$\Delta x\_i$趋于$0$,再让$\Delta x\_j$趋于$0$,得到的结果是$\frac{\partial}{\partial x\_j}\frac{\partial f}{\partial x\_i}$.如果先让$\Delta x\_j$趋于$0$,再让$\Delta x\_i$趋于$0$,得到的结果会是$\frac{\partial}{\partial x\_i}\frac{\partial f}{\partial x\_j}$.我们来证明后者等于前者.这是因为,当$\Delta x\_i$固定,而让$\Delta x\_j$趋于$0$时,根据Lagrange中值定理,存在位于$a\_i+\Delta x\_i$和$a\_i$之间的数$a\_i'$,使得式\eqref{eq:1}等于\begin{equation}\label{eq:2}\frac{\frac{\partial f}{\partial x\_i}(a\_1,\cdots,a\_j+\Delta x\_j,\cdots,a\_i',\cdots,a\_n)-\frac{\partial f}{\partial x\_i}(a\_1,\cdots,a\_j,\cdots,a\_i',\cdots,a\_n)}{\Delta x\_j}.\end{equation}再次使用Lagrange中值定理,可得存在位于$a\_{j}$和$a\_{j}+\Delta\_j$之间的数,使得式\eqref{eq:2}等于\begin{equation}\label{eq:3}\frac{\partial f}{\partial x\_j}\frac{\partial f}{\partial x\_i}(a\_1,\cdots,a\_j',\cdots,a\_i',\cdots,a\_n).\end{equation}由于二阶偏导数连续,因此当$\Delta x\_i,\Delta x\_{j}$趋于$0$,即$a\_j'$趋于$a\_j$,$a\_i'$趋于$a\_i$时,式\eqref{eq:3}确实会趋于$\frac{\partial }{\partial x\_j}\frac{\partial f}{\partial x\_i}$.这样就完成了证明.


上面的证明是基于Lagrange中值定理的.下面我们再给出一个基于定积分的证明.为此,我们先叙述一个引理.这个引理根据微积分第二基本定理是显然的.

>**引理:** 定义在闭区间$I=[a,b]$上的实值连续函数$f$和$g$.$f=g$当且仅当$\forall t\in [a,b]$,$$\int\_a^tf(x)dx=\int\_a^tg(x)dx.$$

有了这个引理之后我们再来证明Clairaut定理.

>**第二个证明:**将函数$\frac{\partial }{\partial x\_j}\frac{\partial f}{\partial x\_i}(x)$沿着$x\_j$方向积分,积分的范围是$x\_j\in [a\_j,b\_j]$,根据微积分第一基本定理,我们会得到\begin{equation}\label{eq:4}\int\_{a\_j}^{b\_j}\frac{\partial}{\partial x\_j}\frac{\partial f}{\partial x\_i}(x)dx\_j=\frac{\partial f}{\partial x\_i}(x\_1,\cdots,b\_j,\cdots,x\_i,\cdots,x\_n)-\frac{\partial f}{\partial x\_i}(x\_1,\cdots,a\_j,\cdots,x\_i,\cdots,x\_n).\end{equation}再将$$\frac{\partial f}{\partial x\_i}(x\_1,\cdots,b\_j,\cdots,x\_i,\cdots,x\_n)-\frac{\partial f}{\partial x\_i}(x\_1,\cdots,a\_j,\cdots,x\_i,\cdots,x\_n)$$沿着$x\_i$方向积分,积分的范围是$[a\_i,b\_i]$,可得\begin{align\*}&\int\_{a\_{i}}^{b\_{i}}\left[\frac{\partial f}{\partial x\_i}(x\_1,\cdots,b\_j,\cdots,x\_i,\cdots,x\_n)-\frac{\partial f}{\partial x\_i}(x\_1,\cdots,a\_j,\cdots,x\_i,\cdots,x\_n)\right]dx\_i\\\&=f(x\_1,\cdots,b\_j,\cdots,b\_i,\cdots,x\_n)-f(x\_1,\cdots,b\_j,\cdots,a\_i,\cdots,x\_n)\\\&-f(x\_1,\cdots,a\_j,\cdots,b\_i,\cdots,x\_n)+f(x\_1,\cdots,a\_j,\cdots,a\_i,\cdots,x\_n).\end{align\*}由于定积分和求导可以互相交换,因此我们对函数$\frac{\partial }{\partial x\_i}\frac{\partial f}{\partial x\_j}(x)$进行和函数$\frac{\partial }{\partial x\_j}\frac{\partial f}{\partial x\_i}(x)$同样的操作(即先对$x\_j$积分,再对$x\_i$积分)会得到同样的结果.由于这两个函数都连续,因此根据引理,可得这两个函数在定义域上相等.

注意到第二种使用积分的证明本质上是用到了二重积分,因此可以将第二种证明化简如下.首先是一个简单的引理.

>**引理2:**设$G$是$\mathbf{R}^2$中的任意一个非空开集,$f,g$都是从$G$到$\mathbf{R}$的二元连续函数.$f,g$在$G$中的任意一个闭矩形上的二重积分都相等,当且仅当$f=g$.

--------
> **第三种证明:**我们来看由$x\_i$轴和$x\_j$轴张成的二维坐标平面.在这个二维坐标平面上随意选取一个矩形,且该矩形位于$E$中.根据Fubini定理,函数$\frac{\partial }{\partial x\_j}\frac{\partial f}{\partial x\_i},\frac{\partial }{\partial x\_i}\frac{\partial f}{\partial x\_j}$在这个矩形上的积分相等.由于两个函数都连续,借助于引理2,便可得两个函数相等.

在最后,我们利用Green定理给出Clairaut定理的特殊情形的一种证明.

>**Clairaut定理的特殊情形:**设$E$是$\mathbf{R}^2$的开子集合,并设$f:\mathbf{E}\to\mathbf{R}$是$E$上的二次连续可微函数.那么对于一切$x\_0\in E$,$$\frac{\partial }{\partial x}\frac{\partial f}{\partial y}(x\_0)=\frac{\partial }{\partial y}\frac{\partial f}{\partial x}(x\_0).$$

----------------

> **证明:**令$\frac{\partial f}{\partial x}=P(x,y)$,$\frac{\partial f}{\partial y}=Q(x,y)$,其中$P,Q$都是从$\mathbf{R}^2$到$\mathbf{R}$的连续可微函数.为了证明Clairaut定理,只用证明$$\frac{\partial P}{\partial y}=\frac{\partial Q}{\partial x}.$$由[Green定理](/2015/02/18/Green定理),也就是证明$\\{(P(x,y),Q(x,y)):(x,y)\in E\\}$是保守力场.这是显然的,因为存在函数$f$,$df=(P,Q)\cdot (dx,dy)$.

--------
>**练习1:**请由上述的Clairaut定理的特殊情形,推导出一般情形的Clairaut定理.
