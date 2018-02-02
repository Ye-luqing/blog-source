title: 利用Abel分部求和法算一个组合恒等式
date: 2015-06-01 00:38:24
categories:
- 数学
tags:
- Abel分部求和法
- 组合恒等式

---
下面这道题是第23届Putnam数学竞赛A5试题.下面采用[Abel分部求和法](http://zh.wikipedia.org/wiki/分部求和法)算它.

**题目:**求和$$1^{2}{n\choose 1}+2^2{n\choose 2}+\cdots+n^2{n\choose n}.$$

------
![图1](/img/利用Abel分部求和法算一个组合恒等式-1.png)
**解:**我们先来做一个可能比较简单的问题.求和
\begin{equation}
  \label{eq:1}
  1{n\choose 1}+2{n\choose 2}+\cdots+n{n\choose n}.
\end{equation}
设
$$
  1{n\choose 1}+2{n\choose 2}+\cdots+n{n\choose n}=f(n),
$$
则由差分图1可得$f(n+1)-f(n)=f(n)+2^{n}$,且$f(1)=1$(差分图的原理见[高阶等差数列的通项公式与杨辉三角](/2015/05/26/高阶等差数列的通项公式与杨辉三角)).解得$f(n)=n2^{n-1}$.再对式\eqref{eq:1}使用Abel分部求和法,可得
\begin{align\*}
&1{n\choose 1}+2{n\choose 2}+\cdots+n{n\choose n}={n\choose
  n}(1+2+\cdots+n)
\\\&-\left[1\left({n\choose 2}-{n\choose 1}\right)+(1+2)\left({n\choose 3}-{n\choose 2}\right)+\cdots+(1+2+\cdots+(n-1))\left({n\choose n}-{n\choose n-1}\right)\right].
\end{align\*}
而
\begin{align\*}
 (1+2+\cdots+k)\left({n\choose k+1}-{n\choose
     k}\right)&=\frac{k(k+1)}{2}\cdot
 \left(\frac{n-k}{k+1}-1\right){n\choose k}
\\\&=\frac{k(n-2k-1)}{2}{n\choose k},
\end{align\*}
因此
\begin{align\*}
1{n\choose 1}+2{n\choose 2}+\cdots+n{n\choose
  n}&=\frac{(n+1)n}{2}-\frac{1}{2}\sum\_{k=1}^{n-1}{n\choose
  k}(kn-2k^2-k)
\\\&=\frac{(n+1)n}{2}-\frac{n-1}{2}\sum\_{k=1}^{n-1}k{n\choose
  k}+\sum\_{k=1}^{n-1}k^2{n\choose k}.
\end{align\*}
可见,
\begin{align\*}
  \sum\_{k=1}^{n-1}k^2{n\choose k}&=n(n+1)2^{n-2}-n^{2},
\end{align\*}
于是,
$$
1^{2}{n\choose 1}+2^2{n\choose 2}+\cdots+n^2{n\choose n}=n(n+1)2^{n-2}.
$$
