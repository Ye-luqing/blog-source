---
title: Apollonius圆与反演
date: 2016-02-12 22:36:32
categories:
- 数学
- 平面几何
tags:
- Apollonius圆
- 反演

---
我们来看这么一个轨迹问题:

**问题**:已知平面上有两个不同的定点$A,B$,设$|AB|=d$.有一个动点$C$,其到点$A$的距离$|AC|$与其到点$B$的距离$|BC|$之比为$\lambda$,即
\begin{equation}\label{eq:1}
|AC|=\lambda|BC|,
\end{equation}
其中$\lambda>0$且$\lambda\neq 1$.求动点$C$的轨迹.
![图1](/img/Apollonius圆与反演.png)
我们利用反演变换来研究动点$C$的轨迹.如图所示,以点$B$为圆心作一个半径为$d$的圆$B$,可得圆$B$过点$A$.并作点$C$关于圆$B$的反演点$C'$.可得
\begin{equation}\label{eq:2}
  |BC'|\cdot |BC|=d^2.
\end{equation}
由式\eqref{eq:2}可得,
$$
\begin{cases}
  \frac{|BC'|}{|BA|}=\frac{|BA|}{|BC|},\\\
\angle C'BA=\angle ABC
\end{cases},
$$
因此$\triangle C'BA\sim\triangle ABC$.结合式\eqref{eq:1}可得
\begin{equation}
  \label{eq:3}
  |AC'|=\lambda |AB|=\lambda d.
\end{equation}
可见,点$C'$始终位于以定点$A$为圆心,以定值$\lambda d$为半径的圆$A$上.再作圆$A$关于圆$B$的反演圆$D$.圆$D$即为点$C$的运动轨迹.且圆$D$的圆心$D$位于直线$AB$上.圆心$D$的确切位置的确定是容易的,在此略述.我们把圆$D$叫做Apollonius圆.
