---
title: 利用Lagrange恒等式推导三面角的余弦定理
date: 2016-03-03 22:14:34
categories:
- 数学
- 解析几何

tags:
- Lagrange恒等式
- 三面角的余弦定理

---
三面角的余弦定理如下:

**定理**:如图,是三棱锥$O-ABC$.$\overrightarrow{OA}$与$\overrightarrow{OB}$的夹角为$\alpha$.$\overrightarrow{OB}$与$\overrightarrow{OC}$的夹角为$\beta$,$\overrightarrow{OC}$与$\overrightarrow{OA}$的夹角为$\gamma$.设二面角$C-OA-B$的大小为$\theta$,则
$$
\cos\theta=\frac{\cos\beta-\cos\alpha\cos\gamma}{\sin\alpha\sin\gamma}.
$$

![图](/img/利用Lagrange恒等式推导三面角的余弦定理-1.png)
**证明**:平面$OAB$的一个法向量为
$$
\overrightarrow{u}=\overrightarrow{OA}\times\overrightarrow{OB},
$$
平面$OAC$的一个法向量为
$$
\overrightarrow{v}=\overrightarrow{OA}\times\overrightarrow{OC}.
$$
向量$\overrightarrow{u}$与向量$\overrightarrow{v}$的夹角就是$\theta$.则
\begin{align\*}
\cos\theta&=\frac{\overrightarrow{u}\cdot\overrightarrow{v}}{|\overrightarrow{u}||\overrightarrow{v}|}
\\\&=\frac{(\overrightarrow{OA}\times\overrightarrow{OB})\cdot(\overrightarrow{OA}\times\overrightarrow{OC})}{|\overrightarrow{OA}\times\overrightarrow{OB}|\cdot|\overrightarrow{OA}\times\overrightarrow{OC}|}
\\\&=\frac{\overrightarrow{OA}^2(\overrightarrow{OB}\cdot\overrightarrow{OC})-(\overrightarrow{OA}\cdot\overrightarrow{OC})(\overrightarrow{OB}\cdot\overrightarrow{OA})}{|\overrightarrow{OA}\times\overrightarrow{OB}|\cdot|\overrightarrow{OA}\times\overrightarrow{OC}|}\mbox{(Lagrange
  恒等式)}
\\\&=\frac{\overrightarrow{|OA|}^2|\overrightarrow{OB}|\overrightarrow{OC}|\cos\beta-|\overrightarrow{OA}|^2|\overrightarrow{OB}||\overrightarrow{OC}|\cos\alpha\cos\gamma}{|\overrightarrow{OA}|^2|\overrightarrow{OB}||\overrightarrow{OC}|\sin\alpha\sin\gamma}
\\\&=\frac{\cos\beta-\cos\alpha\cos\gamma}{\sin\alpha\sin\gamma}.
\end{align\*}
