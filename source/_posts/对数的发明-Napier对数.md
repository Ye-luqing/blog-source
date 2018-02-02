title: "对数的发明:Napier对数"
date: 2015-07-12 23:02:28
categories:
- 数学
- 单元微积分
tags:
- 对数
- e

---
按照现行中学教材,对数这个概念是基于指数的概念而存在的.然而与中学教材的顺序不同的是,历史上对数的出现要早于指数.直到Euler才发现了指数和对数的互逆关系.John Napier是历史上第一个发明了对数并将之公开发表的人.当时,Napier的目的是通过制作一张对数表来简化当时在各行各业中大量出现的繁杂计算.通过对数,可以把乘除法运算转化为加减法运算,而加减法涉及的运算量比乘除法涉及的运算量远远要小.比如,要计算 $M\times N$,只用在对数表中查到 $M,N$ 分别对应的对数 $m,n$,然后把 $m$ 和 $n$ 相加得到 $m+n$,之后在对数表里查到对数 $m+n$ 所对应的指数,那个指数便是 $M\times N$.当然,通过查表会有误差,但是如果表格做的足够精细,那么计算误差是很小的.

Napier 是这样做的.如图1,画两条平行线,其中上面的是射线,下面的是线段.点 $Q,P$ 同时出发.点 $Q$ 在 $T\_1$ 处沿着射线方向匀速运动,而点 $P$ 在 $T$ 处沿着线段做减速运动,其中点 $P$ 在任意一点 $P\_{i}$ 处的速度与 $|P\_iS|$ 成正比.且当 $P$ 运动到 $P\_i$ 时 $Q$ 运动到 $Q\_i$.Napier把 $|T\_1Q\_{1}|$ 叫做 $|P_1S|$ 的Napier对数.这里之所以叫“Napier对数''而不直接以“对数''称呼,是因为Napier对于对数的定义与我们现代对数的概念有出入.

![图1](/img/对数的发明-Napier对数-1.png)
<!--
\begin{figure}[h]
\psset{xunit=1.0cm,yunit=1.0cm,algebraic=true,dotstyle=o,dotsize=3pt 0,linewidth=0.8pt,arrowsize=3pt 2,arrowinset=0.25}
\begin{pspicture*}(0,-6.5)(24.78,6.65)
\psplot{0}{24.78}{(--34.56-0*x)/8.64}
\psline(0,1)(10.42,1)
\begin{scriptsize}
\psdots[dotstyle=*](0,4)
\rput[bl](0.08,4.12){$T_1$}
\psdots[dotstyle=*](0,1)
\rput[bl](0.08,1.12){$T$}
\psdots[dotstyle=*](10.42,1)
\rput[bl](10.51,1.12){$S$}
\psdots[dotstyle=*](2.13,1)
\rput[bl](2.22,1.12){$P_1$}
\psdots[dotstyle=*](3.39,1)
\rput[bl](3.47,1.12){$P_2$}
\psdots[dotstyle=*](4.44,1)
\rput[bl](4.53,1.12){$P_3$}
\psdots[dotstyle=*](5.39,1)
\rput[bl](5.48,1.12){$P_4$}
\psdots[dotstyle=*](6.02,1)
\rput[bl](6.11,1.12){$P_5$}
\psdots[dotstyle=*](6.45,1)
\rput[bl](6.54,1.12){$P_6$}
\psdots[dotstyle=*](2.4,4)
\rput[bl](2.4,4.12){$Q_1$}
\psdots[dotstyle=*](4.4,4)
\rput[bl](4.4,4.12){$Q_2$}
\psdots[dotstyle=*](6.4,4)
\rput[bl](6.4,4.12){$Q_3$}
\psdots[dotstyle=*](8.4,4)
\rput[bl](8.4,4.12){$Q_4$}
\psdots[dotstyle=*](10.4,4)
\rput[bl](10.4,4.12){$Q_5$}
\psdots[dotstyle=*](12.4,4)
\rput[bl](12.4,4.12){$Q_6$}
\end{scriptsize}
\end{pspicture*}
  \caption{}
  \label{fig:1}
\end{figure}
-->

我们发现,点 $Q$ 的作用相当于用于代表匀速流逝的时间.因此就可以简化Napier 的定义如下:

>**定义(Napier对数):**如图2,点 $P$ 在 $0$ 时刻从 $T$ 出发向 $S$ 运动.在任意一点 $P\_i$ 的速度与 $|P\_iS|$ 成正比.经过时间 $t$ 后点 $P$ 到达 $P\_t$ 处.称$t$为$|P_tS|$ 的Napier对数.

![图2](/img/对数的发明-Napier对数-2.png)
<!--
\begin{figure}[h]
\psset{xunit=1.0cm,yunit=1.0cm,algebraic=true,dotstyle=o,dotsize=3pt 0,linewidth=0.8pt,arrowsize=3pt 2,arrowinset=0.25}
\begin{pspicture*}(-0.1,-6.5)(24.78,6.65)
\psline(0,1)(17.01,1)
\begin{scriptsize}
\psdots[dotstyle=*](0,1)
\rput[bl](0.08,1.12){$T$}
\psdots[dotstyle=*](17.01,1)
\rput[bl](17.1,1.12){$S$}
\psdots[dotstyle=*](3.48,1)
\rput[bl](3.58,1.12){$P_1$}
\psdots[dotstyle=*](5.53,1)
\rput[bl](5.61,1.12){$P_2$}
\psdots[dotstyle=*](7.26,1)
\rput[bl](7.34,1.12){$P_3$}
\psdots[dotstyle=*](8.81,1)
\rput[bl](8.89,1.12){$P_4$}
\psdots[dotstyle=*](9.83,1)
\rput[bl](9.91,1.12){$P_5$}
\psdots[dotstyle=*](10.53,1)
\rput[bl](10.62,1.12){$P_6$}
\end{scriptsize}
\end{pspicture*}
  \caption{}
  \label{fig:2}
\end{figure}
-->
我们用微积分的观念来分析一下Napier的定义(Napier那时微积分还没被发明).设$|P\_tS|=f(t)$,$|TS|=R$.则由 Napier的定义可以得到一个微分方程
\begin{equation}\label{eq:1}
\frac{df(t)}{dt}=-kf(t).
\end{equation}
其中 $k>0$ 是一个比例常数.可见,$f(t)$ 是关于 $t$ 的单调递减函数.将式\eqref{eq:1} 化为
\begin{equation}\label{eq:2}
\frac{d t}{d f(t)}=\frac{-1}{kf(t)}.
\end{equation}
将等式 \eqref{eq:2} 两边积分,可以化为
\begin{equation}\label{eq:3}
t=\int\_0^{f(t)}\frac{-1}{kf(t)}df(t)+C.
\end{equation}
其中 $C$ 是一个常数.当 $f(t)=R$ 时,可得 $t=0$.将该条件代入 式\eqref{eq:3},可得
$$
C=-\int\_0^R \frac{-1}{kf(t)}df(t),
$$
将之代进式 \eqref{eq:3} 可得
\begin{equation}\label{eq:4}
t=\int\_R^{f(t)}\frac{-1}{kf(t)}df(t)=\frac{1}{k}\int_{f(t)}^R \frac{1}{f(t)}df(t).
\end{equation}
可见,如果从微积分的角度来看,Napier 实际上是把 Napier 对数定义成了一个积分\eqref{eq:4},也即,Napier 对数实际上是曲线$x=f(t),x=R,y=\frac{1}{kx}$ 所围成的曲边梯形的面积.利用积分 \eqref{eq:4} 可以直接看到Napier对数的一个重要性质,就是把乘除运算简化为和差运算,更确切地说,是如下性质:

>**性质:**$f(t_1),f(t_2),f(t_3)$ 成等比,则 $t_1,t_2,t_3$ 成等差.

为了论证这个命题,我们画图.如图3所示.根据反比例函数的性质和定积分的定义,曲线$x=t\_1,x=at\_1,y=\frac{1}{kx}$ 所围成曲边梯形 $L\_{1}$的面积等于曲线$x=at\_1,x=at\_1^{2},y=\frac{1}{kx}$ 所围成的曲边梯形 $L\_2$的面积,这是因为 $L\_2$ 可以看作是在水平方向拉了 $a$ 倍,在竖直方向压缩了 $a$ 倍的$L\_1$,因此 $L\_1,L\_2$ 面积相同.这样就证明了性质.
![图3](/img/对数的发明-Napier对数-3.png)
<!--
\begin{figure}[h]
\psset{xunit=1.0cm,yunit=1.0cm,algebraic=true,dotstyle=o,dotsize=3pt 0,linewidth=0.8pt,arrowsize=3pt 2,arrowinset=0.25}
\begin{pspicture*}(-2.42,-6.28)(16.9,5.9)
\psaxes[labelFontSize=\scriptstyle,xAxis=true,yAxis=true,Dx=1,Dy=1,ticksize=-2pt 0,subticks=2]{->}(0,0)(-10.42,-6.28)(16.9,5.9)
\psplot[plotpoints=200]{-10.42}{16.9}{1/x}
\psline(10.26,-6.28)(10.26,5.9)
\rput[tl](10.36,3.3){$ x=R $}
\psline(2,-6.28)(2,5.9)
\psline(4,-6.28)(4,5.9)
\psline(8,-6.28)(8,5.9)
\rput[tl](1,3.3){$x=t_1$}
\rput[tl](2.7,3.3){$x=at_1$}
\rput[tl](6.7,3.3){$x=a^2t_1$}
\end{pspicture*}
  \caption{}\label{fig:3}
\end{figure}
-->
