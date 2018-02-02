# 利用射影几何基本定理证明Desargues定理

我们在博文[Desargues定理的证明](/2016/04/14/Desargues定理的证明)中证明了Desargues定理.下面我们使用射影几何基本定理来重新证明Desargues定理.

为了叙述连贯性,我们重新来叙述一下Desargues定理:

>**Desargues定理:**如图1,是平面上的两个三角形,$\triangle ABC$和$\triangle A'B'C'$.其中直线$BB'$,$AA'$,$CC'$交于一点$P$.且直线$AB$与直线$A'B'$交于点$X$,直线$BC$与直线$B'C'$交于点$Y$,直线$CA$与直线$C'A'$交于点$Z$.则点$X,Y,Z$共线.

![图1](/img/Desargues定理的证明-1.png)

**使用射影几何基本定理的证明:**设直线$B'C'$与直线$XZ$交于点$Y'$.透视$T\_1$如下:
$$T\_1:XY'Z\frac{B'}{\wedge}A'C'Z.$$
透视$T\_2$如下:
$$T\_2:A'C'Z\frac{P}{\wedge}ACZ.$$
透视$T\_1$与$T\_2$复合，可得映射$T\_3$.即,$T\_3=T\_2\circ T\_1$.且$T\_3$也是一个透视，这是因为透视$T\_2\circ T\_1$保持了点$Z$不变.于是
$$T\_3:XY'Z\frac{\Delta}{\wedge}ACZ.$$
下面来确定$T\_3$的透视中心$\Delta$.设直线$AP$与直线$ZX$交于点$G$.直线$ZC$与直线$PB'$交于点$J$，直线.则有$GXZ\frac{B}{\wedge}JAZ$.可见$\Delta=B$.

即直线$BC$也经过$Y'$.可见$Y'=Y$.于是$X,Y,Z$三点共线.