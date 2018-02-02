---
title: 使用质心的观点理解Ceva定理
date: 2016-12-27 15:56:22
categories:
- 数学
- 平面几何
tags:
- Ceva定理
- 质心

---
Ceva定理的中心投影证明请见博文[利用中心投影证明Ceva定理](/2016/08/06/利用中心投影证明Ceva定理).为了完整起见，重新叙述Ceva定理如下:

> 如图,是$\triangle ABC$.线段$BC,CA,AB$上分别有点$D,E,F$.且$AD,BE,CF$交于一点$G$.则有$$\frac{AF}{FB}\cdot \frac{BD}{DC}\cdot \frac{CE}{EA}=1.$$

![图1](/img/使用质心的观点理解Ceva定理-1.png)
**证明**：设在点$A$处放置一个质量为$\alpha$的质点，在点$B$处放置一个质量为$\beta$的质点,使得质点组$A,B$的质心在点$F$处.再在点$C$处放置一个质量为$\gamma$的质点,使得质点组$A,C$的质心在点$E$处.则质点组$A,B,C$的公共质心必定既在直线$FC$上，又在直线$BE$上.即，质点组$A,B,C$的质心必定在直线$FC$和$BE$的交点$G$处.因此，质点组$B,C$的质心必定在直线$AG$的延长线上,即在点$D$处.由杠杆原理,必有$\frac{AF}{FB}=\frac{\beta}{\alpha}$,$\frac{BD}{DC}=\frac{\gamma}{\beta}$,$\frac{CE}{EA}=\frac{\alpha}{\gamma}$.因此$\frac{AF}{FB}\cdot \frac{BD}{DC}\cdot\frac{CE}{EA}=\frac{\beta}{\alpha}\cdot \frac{\gamma}{\beta}\cdot \frac{\alpha}{\gamma}=1$.$\Box$

另外，使用质心方法，我们还可以得到一些额外的结论.比如，$\frac{AG}{GD}=\frac{\beta+\gamma}{\alpha}=\frac{AF}{FB}+\frac{AE}{EC}$.

