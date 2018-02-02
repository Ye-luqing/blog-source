title: 角动量、力矩与Kepler第二定律
date: 2015-03-13 12:55:17
categories:
- 物理
- 经典力学
tags:
- 角动量
- 力矩
- 向量积
- Kepler第二定律
- 有心力
---
![图1](/img/角动量、力矩与Kepler第二定律-1.png) 

设$O$是空间中的一个固定点.质点$P$对于点$O$的角动量定义为$$\mathbf{L}:=\mathbf{r}\times m\mathbf{v}.$$其中向量$\mathbf{r}$是从点$O$到质点$P$的矢径,$\mathbf{v}$是质点$P$的速度,$m$是质点的质量.

角动量的向量积定义表明了,当把质点$P$的速度分解为沿着向径的速度和垂直于向径的速度,那么沿着向径的速度对于角动量是没有影响的,只有垂直于向径的速度才对角动量有影响.也就是说,沿着向径的速度,只对线动量产生影响,对于物体的转动,是没有贡献的.对物体转动产生贡献的是垂直于向径$\mathbf{r}$的速度.

而我们知道,力是和速度息息相关的.即,力正比于速度随时间的变化率.因此不难想到,作用在质点上的力,将其分解为沿着向径方向的力,和垂直于向径方向的力后,沿着向径方向的力对质点的转动是没有影响的,只有垂直于向径方向的力才对质点的转动有影响.事实上,考虑角动量关于时间的导数,$$
\lim\_{t\to 0}\frac{(\mathbf{r}+\Delta \mathbf{r})\times m(\mathbf{v}+\Delta
    \mathbf{v})-\mathbf{r}\times m\mathbf{v}}{\Delta t}=\lim\_{t\to
    0}\frac{\mathbf{r}\times m\Delta \mathbf{v}+m\Delta
    \mathbf{r}\times \mathbf{v}+m\Delta \mathbf{r}\times \Delta
    \mathbf{v}}{\Delta t}=\mathbf{r}\times \mathbf{F}.
$$其中$\mathbf{F}$是作用在质点$P$上的力.定义$\mathbf{r}\times\mathbf{F}$为力矩.可见,只有垂直于$\mathbf{r}$的力才对力矩有影响,而沿着$\mathbf{r}$的力对力矩无影响.

对于质点的[有心力](http://zh.wikipedia.org/wiki/有心力)运动来说,作用在质点上的合力总指向一个固定点$O$.因此如果我们以这个固定点到质点的向径为$\mathbf{r}$,则作用在质点上的力始终对质点的角动量没有影响.此时,质点的角动量守恒.也即$\frac{1}{2}\mathbf{r}\times\mathbf{v}$守恒,也即,质点在单位时间内,相对于固定点而划过的面积始终相等.在天文学上,这表现为行星运动的[Kepler第二定律](http://zh.wikipedia.org/wiki/开普勒定律):

> 在相等时间内,太阳和运动着的行星的连线所扫过的面积都是相等的.

