---
title: 利用Desargues构型理解交比在射影下不变
date: 2017-06-21 21:03:32
categories:
- 数学
- 射影几何
tags:
- Desargues定理
- Menelaus定理
- 交比

---
如图1所示，$C\_1A\_1A\_2 \frac{C\_3}{\wedge }C\_2A\_3A\_{2}$,$C\_1B\_1B\_2\frac{C\_3}{\wedge} C\_2B\_3B\_2$.则Desargues定理表明，点$A\_2,B\_2,Z$共线,其中$Z$是直线$A\_1B\_1$与直线$A\_3B\_3$的交点.因此
![图1](/img/一个问题的若干解法及其推广-2.png)
由Menelaus定理，
  \begin{equation}
    \label{eq:1}
    \frac{C\_1A\_1}{A\_1A\_2}\cdot \frac{A\_2Z}{ZB\_2}\cdot \frac{B\_2B\_1}{B\_1C\_1}=-1,
  \end{equation}
  \begin{equation}
    \label{eq:2}
    \frac{A\_2A\_3}{A\_3C\_2}\cdot \frac{C\_2B\_3}{B\_3B\_2}\cdot \frac{B\_2Z}{ZA\_2}=-1.
  \end{equation}
上面两个方程等号的左右两边分别相乘，得到
\begin{equation}
  \label{eq:3}
  \frac{C\_1A\_1}{A\_1A\_2}\cdot \frac{A\_2A\_3}{A\_3C\_2}\cdot
  \frac{C\_2B\_3}{B\_3B\_2}\cdot \frac{B\_2B\_1}{B\_1C\_1}=1.
\end{equation}
即
\begin{equation}
  \label{eq:4}
\left.\frac{C\_1A\_1}{A\_1A\_2}\middle/
\frac{C\_1B\_1}{B\_1B\_2}\right.=\left.\frac{C\_2A\_3}{A\_3A\_2}\middle/
\frac{C\_2B\_3}{B\_3B\_2}\right.\iff \left.\frac{A\_1C\_1}{A\_1A\_2}\middle/
\frac{B\_1C\_1}{B\_1B\_2}\right.=\left.\frac{A\_3C\_2}{A\_3A\_2}\middle/ \frac{B\_3C\_2}{B\_3B\_2}\right.
\end{equation}
然后取极限情形，让点$B\_2$与点$A\_2$重合，则图1会变成图2.
![图2](/img/利用Desargues构型理解交比在射影下不变-2.png)
相应的，式\eqref{eq:4}就会变成
\begin{equation}
  \label{eq:5}
\left.\frac{A\_1C\_1}{A\_1Z}\middle/
  \frac{B\_1C\_1}{B\_1Z}\right.=\left.\frac{A\_3C\_2}{A\_3Z}\middle/ \frac{B\_3C\_2}{B\_3Z}\right.
\end{equation}
此即交比在射影下不变.