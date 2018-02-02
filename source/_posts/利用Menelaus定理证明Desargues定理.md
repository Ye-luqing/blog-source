---
title: 利用Menelaus定理证明Desargues定理
date: 2017-06-20 19:03:15
categories:
- 数学
- 射影几何
tags:
- Menelaus定理
- Desargues定理

---
下面我们使用Menelaus定理证明Desargues定理.Desargues定理叙述如下：

> **Desargues定理:**如图1所示，直线$A\_1B\_1,A\_2B\_2,A\_3B\_3$交于点$Z$.且直线$A\_1A\_2$交$B\_1B\_2$于点$C\_1$,直线$A\_2A\_3$交于$B\_2B\_3$于点$C\_2$,直线$A\_3A\_1$交$B\_3B\_1$于点$C\_3$.则点$C\_1,C\_{2},C\_{3}$共线.

![图1](/img/一个问题的若干解法及其推广-2.png)
**使用Menelaus定理的证明:**由Menelaus定理，
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
  \frac{C\_1A\_1}{A\_1A\_{2}}\cdot
  \frac{A\_2A\_3}{A\_3C\_2}=\frac{C\_1B\_1}{B\_1B\_2}\cdot \frac{B\_2B\_3}{B\_3C\_2}.
\end{equation}
设直线$A\_1A\_3$与直线$C\_1C\_2$交于点$C\_3'$,直线$B\_1B\_3$与直线$C\_1C\_2$交于点$C\_3''$.下面我们证明点$C\_3'$和点$C\_3''$重合.这是因为，由Menelaus定理，
$$
\frac{C\_1A\_1}{A\_1A\_2}\cdot \frac{A\_2A\_{3 }}{A\_3C\_2}\cdot \frac{C\_2C\_3'}{C\_3'C\_1}=-1,
$$
且
$$
\frac{C\_1B\_1}{B\_1B\_2}\cdot \frac{B\_2B\_3}{B\_3C\_2}\cdot \frac{C\_2C\_3''}{C\_3''C\_1}=-1.
$$
结合方程\eqref{eq:4}可得
$$
\frac{C\_2C\_3'}{C\_3'C\_1}=\frac{C\_2C\_3''}{C\_3''C\_1}.
$$
因此点$C\_3'$与点$C\_3''$重合.即三条直线$A\_1A\_3,B\_1B\_3,C\_1C\_2$交于一点,这一点既是$C\_3'$,又是$C\_3''$,统一记为$C\_3$.$\Box$