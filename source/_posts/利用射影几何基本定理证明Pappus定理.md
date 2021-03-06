﻿---
title: 利用射影几何基本定理证明Pappus定理
date: 2017-06-25 10:55:33
categories:
- 数学
- 射影几何
tags:
- Pappus定理
- 射影几何基本定理

---
先重述Pappus定理.如图1所示,点$A\_1,A\_2,A\_3$共线,点$C\_1,C\_2,C\_3$共线.直线$A\_1C\_2$与直线$A\_2C\_1$交于点$B\_2$,直线$A\_1C\_3$与直线$A\_3C\_1$交于点$B\_3$,直线$A\_2C\_3$与直线$A\_3C\_2$交于点$D\_2$.则Pappus定理表明，点$B\_2,B\_3,D\_2$共线.


我们曾经[使用中心投影的方法证明Pappus定理(通过把直线$B\_2B\_3$当作没影线)](/2016/04/15/证明Pappus定理/)，现在，我们考虑使用射影几何基本定理证明Pappus定理.

首先，我们把命题转换一下.Pappus定理等价于：

> 如图1所示，点$A\_1,A\_2,A\_3$共线，点$C\_1,C\_2,C\_3$共线.直线$A\_1C\_2$与直线$A\_2C\_1$交于点$B\_2$,直线$A\_1C\_3$与直线$A\_3C\_1$交于点$B\_3$,设直线$B\_2B\_3$与直线$A\_3C\_2$交于点$D\_2$,则点$A\_{2},D\_2,C\_3$三点共线.

![图1](/img/利用射影几何基本定理证明Pappus定理-1.png)
下面我们来证明这个转换了的命题.为此我们需要在图1的基础上再添加一些点和线，变成图2.在图2中，点$B\_1$是直线$A\_1C\_1$与直线$B\_2B\_3$的交点,点$D\_3$是直线$A\_3B\_3$与直线$B\_2B\_3$的交点，点$A\_4$是直线$A\_1A\_2$与直线$B\_2B\_3$的交点,点$C\_4$是直线$A\_1A\_2$与直线$C\_1C\_2$的交点.

![图2](/img/利用射影几何基本定理证明Pappus定理-2.png)
如图2所示，
$$
T\_{1}:A\_1A\_2A\_3A\_{4} \frac{C\_1}{\wedge}B\_1B\_2B\_3A\_{4},
$$
以及
$$
T\_{2}:B\_1B\_2B\_3A\_{4} \frac{A\_1}{\wedge}C\_1C\_2C\_3C\_{4},
$$
$$
T\_{3}:C\_1C\_2C\_3C\_{4} \frac{A\_3}{\wedge}B\_{3}D\_2D\_3A\_{4},
$$
$$
T\_4:B\_3D\_{3}A\_4 \frac{C\_3}{\wedge} A\_1A\_3A\_4.
$$
考虑如上透视的复合
$$
T\_4\circ T\_3\circ T\_2\circ T\_1:A\_1A\_3A\_4\to A\_1A\_3A\_4.
$$
由于三个共线的点确定唯一一个射影，因此$T\_4\circ T\_3\circ T\_2\circ T\_1=I$，是个恒等映射.因此
$$
T\_4\circ T\_3\circ T\_2\circ T\_1:A\_2\to A\_2,
$$
而$T\_3\circ T\_2\circ T\_1:A\_2\to D\_2$,因此$T\_4:D\_2\to A\_2$.这样就证明了点$A\_2,D\_2,C\_3$三点共线.进一步就证明了Pappus定理.