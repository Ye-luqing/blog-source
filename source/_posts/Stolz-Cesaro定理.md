title: Stolz-Cesàro定理
date: 2015-11-24 23:50:46
categories:
- 数学
- 单元微积分
tags:
- Stolz-Cesàro定理

---
>**Stolz-Cesàro定理**:递增数列$b\_0,b\_1,...,b\_n,\cdots$与数列$a\_0,a\_1,\cdots，a\_n,\cdots$其中$\lim\_{n\to\infty}b\_n=\infty$而且$\lim\_{n\to\infty}\frac{a\_n-a\_{n-1}}{b\_n-b\_{n-1}}$存在(有限或无穷),则$$\lim\_{n\to\infty}\frac{a\_n}{b\_n}=\lim\_{n\to\infty}\frac{a\_n-a\_{n-1}}{b\_n-b\_{n-1}}$$

**证明**:把数列
$$a\_0,a\_1-a\_0,a\_2-a\_1,a\_3-a\_2,...a\_n-a\_{n-1},\cdots$$
记为
$$x\_0,x\_1,x\_2,x\_3,\cdots,x\_n,\cdots$$
把数列
$$b\_0,b\_1-b\_0,b\_2-b\_1,b\_3-b\_2,\cdots b\_n-b\_{n-1},\cdots$$
记为
$$y\_0,y\_1,y\_2,y\_3,...，y\_n,\cdots$$
则定理可以改写为：

>数列$x\_0,x\_1,x\_2,x\_3,\cdots,x\_n,\cdots$与从第二项开始各项为正的数列$y\_0,y\_1,y\_2,y\_3,\cdots,y\_n,\cdots$,其中$\displaystyle\sum\_{i=0}^\infty y\_i=\infty$,且$\lim\_{n\to\infty}\frac{x\_n}{y\_n}$存在（有限或无限）.则$$\lim\_{n\to\infty}\frac{x\_0+x\_1+...x\_n}{y\_0+y\_1+...y\_n}=\lim\_{n\to\infty}\frac{x\_n}{y\_n}$$(这样子变换一下，Stolz定理是不是就显得更直观了呢?)

当$\lim\_{n\to\infty}\frac{x\_n}{y\_n}$存在且有限时，设为$L$.则对于任意给定的正实数$\varepsilon$,都存在正整数$N$,当$n\geq N$时都有$|\frac{x\_n}{y\_n}-L|<\varepsilon$.我们可以放心地把$$\lim\_{n\to\infty}\frac{x\_0+x\_1+...x\_n}{y\_0+y\_1+...y\_n}$$(不管该极限存在与否)改写成$$\lim\_{n\to\infty}\frac{x\_N+x\_{N+1}+...x\_n}{y\_N+y\_{N+1}+...y\_n}$$这是因为$\displaystyle\sum\_{i=0}^\infty y\_i=\infty$,删去$\lim\_{n\to\infty}\frac{x\_0+x\_1+...x\_n}{y\_0+y\_1+...y\_n}$中的$y\_0,y\_1,...y\_{N-1}$与$x\_0,x\_1,...x\_{N-1}$不会影响极限计算结果.下面我们看$$\frac{x\_N+x\_{N+1}+...+x\_n}{y\_N+y\_{N+1}+...+y\_n}$$的几何意义：

设$\overrightarrow{A\_i}=(y\_i,x\_i)(i=N,N+1,...n)$,则$$\frac{x\_N+x\_{N+1}+...+x\_n}{y\_N+y\_{N+1}+...+y\_n}$$的几何意义是向量$\overrightarrow{B}=\overrightarrow{A\_1}+\overrightarrow{A\_2}+...+\overrightarrow{A\_n}$所在直线的斜率.而且$\overrightarrow{A\_i}=(y\_i,x\_i)(i=N,N+1,...n,y\_i>0)$所在直线的斜率全都限制在区间$(L-\varepsilon,L+\varepsilon)$内.


让我们想像一下直观图景：一个个斜率在区间$(L-\varepsilon,L+\varepsilon)$内的向量扎成了一束马尾辫

![图1](/img/Stolz-Cesaro定理-1.png)

最上面的虚线代表斜率为$L+\varepsilon$的向量，最下面的虚线代表着斜率为$L-\varepsilon$的向量.下面看向量$\overrightarrow{B}$,$\overrightarrow{B}$的斜率我们采用数学归纳法（其实明眼人一眼就看得出来）易得仍在区间$(L-\varepsilon,L+\varepsilon)$内.这样，我们就证完了斯笃兹定理当$\lim\_{n\to\infty}\frac{x\_n}{y\_n}$为有限数时的情形.


对于$\lim\_{n\to\infty}\frac{x\_n}{y\_n}$为无限数时的情形，也就是$L=\infty$时，其实那一束束直线是紧密围绕在$y$轴附近的，按照与以上一样的方法也可以很容易证明.$\Box$

---- 
**注1**:观察上面的证明，我们发现，其实如果我们把“递增数列$b\_0,b\_1,...,b\_n,\cdots$”这个条件改为"递减数列$b\_0,b\_1,...,b\_n,\cdots$",则结论照样成立.
