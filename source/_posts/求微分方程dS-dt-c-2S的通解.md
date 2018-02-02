title: 求微分方程$\frac{dS}{dt}=-\frac{c^2}{m}S$的通解
date: 2015-04-10 18:53:22
categories:
- 数学
- 微分方程
tags:
- 简谐运动
- 圆周运动
---
让我们来看一个物理问题.在水平位置放置一个弹簧.弹簧的一段固定在墙壁上.另外一段绑着一个质点.以质点的平衡位置为位移的原点,即规定在质点的平衡位置,弹簧的位移为$0$.然后给质点一个初始速度,然后质点开始在弹簧的弹性范围内进行周期运动.
![图1](/img/求微分方程dS-dt-c-2S的通解-1.png)
根据Hooke定律,作用在弹簧上的力${F}$与弹簧的位移${S}$之间的关系是${F}=-c^{2}{S}$,其中$c^{2}>0$是弹性系数.而且根据Newton第二运动定律,${F}=m\frac{d^2{S}}{dt^2}$,其中$t$是时间,$t$增大表明时间在流逝.由此我们可以消去力${F}$,而得到只含${S}$和$t$的运动学微分方程
\begin{equation}
  \label{eq:1}
  \frac{d^2{S}}{dt^2}=-\frac{c^{2}}{m}{S}.
\end{equation}
微分方程\eqref{eq:1}等价于微分方程组
\begin{equation}\label{eq:2}
\begin{cases}
  \frac{dS}{dt}=-\frac{c}{\sqrt{m}}K\\\
\frac{dK}{dt}=\frac{c}{\sqrt{m}}S.
\end{cases}
\end{equation}
其中$K$是引入的辅助实函数.而微分方程组\eqref{eq:2}等价于复微分方程
\begin{equation}
  \label{eq:3}
  \frac{dP}{dt}=i\frac{c}{\sqrt{m}}P,
\end{equation}
其中$i$是虚数单位,且复函数$P=S+Ki$.而微分方程\eqref{eq:2}的解的形式只能为
$$
S=Ae^{i\frac{c}{\sqrt{m}}t},
$$
其中$A\in \mathbf{C}$为任意复数.这是因为,假设微分方程\eqref{eq:2}还有另外一种形式的解 $f(t)$,则考虑$g(t)=f(t)e^{-i\frac{c}{\sqrt{m}}t}$,
$$
g'(t)=f'(t)e^{-i\frac{c}{\sqrt{m}}t}-i\frac{c}{\sqrt{m}}f(t)e^{-i\frac{c}{\sqrt{m}}t}=i\frac{c}{\sqrt{m}}f(t)e^{-i\frac{c}{\sqrt{m}}t}-i\frac{c}{\sqrt{m}}f(t)e^{-i\frac{c}{\sqrt{m}}t}=0.
$$
可见$g(t)$是常值函数.可见,$f(t)$只能是形如$Ae^{i\frac{c}{\sqrt{m}}t}$.这样,就可以推得微分方程\eqref{eq:1}的解只能形如
$$
a\cos \frac{c}{\sqrt{m}}t+b\sin \frac{c}{\sqrt{m}}t,
$$
其中$a,b\in \mathbf{R}$由初值条件确定.可见,弹簧振子在做简谐运动.上面的所有推导只不过是反映了这么一个事实,就是,简谐运动只不过是圆周运动的一个侧面.
