title: 什么函数的有界导函数非Riemann可积
date: 2015-03-18 23:24:15
categories:
- 数学
- 实分析
tags:
- Riemann积分
- volterra函数

---
有一个数学分析书上很少提到的事实,就是:
> 一个可微函数的有界导函数在闭区间上未必Riemann可积.

这可能违反了很多人的臆测.[Volterra函数](http://en.wikipedia.org/wiki/Volterra%27s_function)就是一个例子.Volterra函数是在定义域上处处可微的函数,而且Volterra函数在定义域上的导函数有界,但是导函数却在一个正Lebesgue测度的集合上不连续,这就违反了Riemann可积性的判别法则:

>一个有界函数在闭区间$[a,b]$上Riemann可积,当且仅当,有界函数在闭区间上不连续点的集合的Lebesgue测度是$0$.

这个事实其实说明了Riemann积分的局限性.

Volterra函数构造的关键是使用了一个构造过程类似于 [Cantor三分集](http://zh.wikipedia.org/wiki/康托尔集) 的集合,姑且叫它类Cantor集.类Cantor集合构造如下:

+ 把区间$[0,1]$的正中间长度占整个区间$\frac{1}{4}$比例的开区间挖掉.
+ 对剩下的2个闭区间分别进行和第一步中的操作相同的操作.
+ 对剩下的4个闭区间分别进行和第一步中的操作相同的操作.
+ 对剩下的8个闭区间分别进行和第一步中的操作相同的操作.
+ $\vdots$

这样不断地操作下去,**最终**剩下的点集就是类Cantor三分集.只不过Cantor三分集的Lebesgue测度为$0$,而类Cantor集通过调整,其Lebesgue测度为正.这是事实一.

我们发现随着操作的进行,被挖掉的单个区间会越来越小,被挖掉的单个区间的数目也越来越多.最终,类Cantor集合中任意一个点的任意一个邻域都会与被挖掉的某个区间相交,因此也包含被挖掉的那个区间的一个端点.这是事实二.

而且在构造类Cantor集时,凡是被挖掉的区间上都放置了一个在区间端点处导函数不连续,但是却处处可导的函数.函数的大小和被挖掉的区间大小相适应.这是事实三.

通过这三个事实的综合,保证了Volterra函数的导函数的不连续点集合的Lebesgue测度是正的.这样就完成了Volterra函数的构造.
<iframe scrolling="no" src="https://tube.geogebra.org/material/iframe/id/57530/width/1247/height/444/border/888888/rc/true/ai/true/sdz/true/smb/true/stb/false/stbh/true/ld/true/sri/true/at/auto" width="800px" height="500px" style="border:0px;"> </iframe>
