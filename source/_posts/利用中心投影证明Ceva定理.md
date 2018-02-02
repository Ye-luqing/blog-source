---
title: 利用中心投影证明Ceva定理
date: 2016-08-06 16:26:51
categories:
- 数学
- 平面几何

tags:
- Ceva定理
- 中心投影
- Menelaus定理

---
平面几何中的Ceva定理叙述如下:如图1,平面$\pi$上有$\triangle ABC$.线段$BC,CA,AB$上分别有点$D,E,F$.且$AD,BE,CF$交于一点$G$.则有
\begin{equation}\label{eq:1}
\frac{AF}{FB}\cdot \frac{BD}{DC}\cdot \frac{CE}{EA}=1.
\end{equation}

![图1](/img/利用中心投影证明Ceva定理-1.png)
现在我们给出一个基于中心投影的证明.在平面$\pi$外选取一个点$I$,将平面$\pi$上的所有点以$I$为投影中心,中心投影到另外一个平面$\pi'$上,设任意一个被记为$X$的点经过中心投影后形成的点被记为$X'$.且点$A$是中心投影的没影点,即点$A$被中心投影到无限远处,同时让$B=B',D=D'C=C'$.

易得$AI\parallel BF'$,$AI\parallel CE'$.因此$\triangle AFI\sim \triangle BFF'$,$\triangle AEI\sim \triangle CEE'$.于是,
$$
\frac{AF}{FB}\cdot \frac{BD}{DC}\cdot
\frac{CE}{EA}=\frac{IA}{BF'}\cdot \frac{BD}{DC}\cdot
\frac{CE'}{IA}=\frac{CE'}{BF'}\cdot \frac{BD}{DC}=1.
$$
可见式\eqref{eq:1}成立.

> **注**:利用同样的方法也能证明Menelaus定理.对于同样的图,考虑$\triangle ABD$.易得
$$
\frac{AF}{FB}\cdot \frac{BC}{CD}\cdot \frac{DG}{GA}=\frac{IA}{BF'}\cdot \frac{BC}{CD}\cdot \frac{DG'}{IA}=\frac{DG'}{BF'}\cdot \frac{BC}{CD}=-1.
$$
此即Menelaus定理.