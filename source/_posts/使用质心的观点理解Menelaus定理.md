---
title: 使用质心的观点理解Menelaus定理
date: 2016-12-27 23:40:03
categories:
- 数学
- 平面几何
tags:
- Menelaus定理
- 质心

---
Menelaus定理叙述如下：

> 已知，如图，一直线分别截$\triangle ABC$的边$AC,BC$及$AB$的延长线于点$D,E,F$.求证：$\frac{AD}{DC}\cdot \frac{CE}{EB}\cdot \frac{BF}{FA}=1$.

![图1](/img/使用质心的观点理解Menelaus定理-1.png)
下面，我们从质心的角度来证明Menelaus定理.

**证明**:在点$C$处放置一个质量为$|AD|$的质点$\gamma\_1$.在点$A$处放置一个质量为$|DC|$的质点$\alpha$.则由杠杆原理，质点$\gamma\_1$和$\alpha$形成的质点组的质心在点$D$处.在点$C$处再放置一个质量为$|EB|$的质点$\gamma\_2$,在点$B$处放置一个质量为$|CE|$的质点$\beta$.则由杠杆原理,质点$\gamma\_2$和质点$\beta$形成的质点组的质心在点$E$处.这样，质点$\gamma\_1,\gamma\_2,\alpha,\beta$形成的质点组的质心必定在线段$DE$上.

最后，在$F$处放一个质量为$x$的质点$f$,使得质点$\gamma\_1,\gamma\_2,\alpha,\beta,f$形成的质点组的质心恰好位于点$E$处.我们来求$x$的值.由于所有质点形成的质点组的质心在点$E$处，于是所有质点形成的质点组的质心位于质心$BC$上.因此，质点$\alpha,f$形成的质点组的质心必须在点$B$处.这样，质点$\alpha,f,\beta$形成的质点组的质心也位于点$B$.由杠杆原理,
$$
\frac{\alpha\mbox{的质量}+\beta\mbox{的质量}+f\mbox{的质
    量}}{\gamma\_1\mbox{的质量}+\gamma\_2\mbox{的质量}}=\frac{|CE|}{|EB|},
$$
即
$$
\frac{|DC|+|CE|+x}{|AD|+|EB|}=\frac{|CE|}{|EB|},
$$
解得$x=|AD|\cdot\frac{|CE|}{|EB|}-|DC|$.因此，由杠杆原理，$\frac{|AB|}{|BF|}=\frac{f\mbox{的质量}}{\alpha\mbox{的质
量}}=\frac{|AD|}{|DC|}\cdot \frac{|CE|}{|EB|}-1$.因此$$\frac{|AF|}{|FB|}=\frac{|AB|+|BF|}{|FB|}=\frac{|AD|}{|DC|}\cdot\frac{|CE|}{|EB|}.$$所以$\frac{|AD|}{|DC|}\cdot \frac{|CE|}{|EB|}\cdot \frac{|BF|}{|FA|}=1$.