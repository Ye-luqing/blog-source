title: Green定理
date: 2015-02-18 02:36:58
categories:
- 数学
- 多元微积分
tags:
- Green定理
- 功

----
在介绍一般的,复杂的Green定理之前,我们先介绍特殊的Green定理:矩形上的Green定理.
###矩形Green定理
> **(矩形Green定理)** 设 $D$ 是 $xy$ 平面直角坐标系上的矩形区域,且矩形的边都与相应的坐标轴平行.函数 $P(x,y)$ 和$Q(x,y)$ 是在包含 $D$ 的一个开集上的从$\mathbf{R}^2$到$\mathbf{R}$的连续可微函数,则有$$\iint\_D \left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)dxdy=\oint\_l Pdx+Qdy.$$这里右端为沿$D$的边界的积分,积分路径的方向是和趋于正向联系的,即当一个点沿着边界运动时区域 $D$ 恒在其左边(亦即服从右手法则).
 
![图1](/img/Green定理-1.png)

矩形Green定理是一个物理意义很强的定理.我们先利用力与作功的概念给出其物理意义.证明也是在物理背景下开展的.

> **矩形Green定理的物理意义与证明:**将$\\{(P(x,y),Q(x,y)):(x,y)\in D\\}$看成区域 $D$ 上的力场.粒子在力场中沿着矩形$D$的边界循环运动.粒子的运动方向使得矩形 $D$ 始终位于粒子的左边.$\oint\_l Pdx+Qdy$表示粒子完成一个周期的运动后,力场对粒子所作的功.

> 当粒子水平运动时,作用在粒子上的力分解为水平方向的力$P$和竖直方向的力$Q$.竖直方向的力对水平运动的粒子不作功.如图1,是一个边与坐标轴平行的矩形.点$B$的坐标是$(x\_A+\Delta x,y\_A)$,点$C$的坐标是$(x\_A+\Delta x,y\_A+\Delta y)$.当粒子从A运动到B时,力场对粒子作功为$$\int\_{x\_A}^{x\_A+\Delta x}P(x,y\_A)dx$$当粒子从C运动到D时,力场对粒子作功为$$\int\_{x\_A+\Delta x}^{x\_A}P(x,y\_A+\Delta y)dx=-\int\_{x\_A}^{x\_A+\Delta x}P(x,y\_A+\Delta y)dx.$$可见,当粒子水平运动时,力场对粒子作的总功为\begin{align\*}\int\_{x\_A}^{x\_A+\Delta x}P(x,y\_A)dx- \int\_{x\_A}^{x\_A+\Delta x}P(x,y\_A+\Delta y)dx &=\int\_{x\_A}^{x\_A+\Delta x}[P(x,y\_A)-P(x,y\_A+\Delta y)]dx\\\&=-\int\_{x\_A}^{x\_A+\Delta x}\int\_{y\_A}^{y\_A+\Delta y} \frac{\partial P}{\partial y}dydx.\end{align\*}

> 当粒子竖直运动时,水平方向的力对粒子不作功.当粒子从B运动到C时,力场对粒子作功为$$\int\_{y\_A}^{y\_A+\Delta y}Q(x\_A+\Delta x,y)dy.$$当粒子从D运动回A时,力场对粒子作功为$$\int\_{y\_A+\Delta y}^{y\_A}Q(x\_A,y)dy=-\int\_{y\_A}^{y\_A+\Delta y}Q(x\_A,y)dy.$$可见,当粒子竖直运动时,力场对粒子作的总功为$$\int\_{y\_A}^{y\_A+\Delta y}Q(x\_A+\Delta x,y)dy-\int\_{y\_A}^{y\_A+\Delta y}Q(x\_A,y)dy=\int\_{y\_A}^{y\_A+\Delta y}\int\_{x\_A}^{x\_A+\Delta x}\frac{\partial Q}{\partial x}dxdy.$$

> 综上,力场对运动一周的粒子作的总功为$$\int\_{y\_A}^{y\_A+\Delta y}\int\_{x\_A}^{x\_A+\Delta x}\frac{\partial Q}{\partial x}dxdy-\int\_{x\_A}^{x\_A+\Delta x}\int\_{y\_A}^{y\_A+\Delta y} \frac{\partial P}{\partial y}dydx=\iint\_D \left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)dxdy.$$这样就证明了矩形上的Green定理.

--------

其实,矩形Green定理的物理意义不止一种.上面的证明的物理意义基于力与作功.下面我们给出一种基于流体运动的物理意义和证明.个人认为从流体的角度来理解矩形Green定理比从力与作功的角度来理解更好.

![图2](/img/Green定理-2.png)


> **矩形Green定理的另一种证明:**将$\\{(P(x,y),Q(x,y)):(x,y)\in D\\}$看成区域 D 上的流体的速度场,由于每个速度都可以分解为平行于$x$轴方向的速度和平行于$y$轴方向的速度,因此速度场可以表达为横速度场和纵速度场的叠加.如图2,其中区域$D$是矩形$OA'B'C'$,其中矩形的两条边都与坐标轴平行.将矩形以点$O$为旋转中心,顺时针旋转一个直角,得到另外一个矩形$OABC$.且点$B$的坐标是$(x\_A+\Delta x,y\_A)$,点$C$的坐标是$(x\_A+\Delta x,y\_A+\Delta y)$.我们先考虑纵速度场,积分$\int\_{y\_A+\Delta y}^{y\_A}Q(x\_A,y)dy$等于通过$OA'$而流出区域D的流体的流通量(若$\int\_{y\_A+\Delta y}^{y\_A}Q(x\_A,y)dy<0$则流体实际上经过$OA'$而流进区域D.下同).积分$\int\_{y\_A}^{y\_A+\Delta y}Q(x\_A+\Delta x,y)dy$等于通过$B'C'$而流出区域$D$的流体的流通量.总的效应是\begin{align\*}\int\_{y\_A+\Delta y}^{y\_A}Q(x\_A,y)dy+\int\_{y\_A}^{y\_A+\Delta y}Q(x\_A+\Delta x,y)dy&=\int\_{y\_A}^{y\_A+\Delta y}[Q(x\_A+\Delta x,y)-Q(x\_A,y)]dy\\\&=\int\_{y\_{A}}^{y\_A+\Delta y}\int\_{x\_A}^{x\_A+\Delta x}\frac{\partial Q}{\partial x}dxdy,\end{align\*}其中$\frac{\partial Q}{\partial x}$表示纵向流体速度沿着向量$\overrightarrow{A'B'}$的梯度.

> 同理,可以给出\begin{align\*}\int\_{x\_A}^{x\_A+\Delta x}P(x,y\_A)dx- \int\_{x\_A}^{x\_A+\Delta x}P(x,y\_A+\Delta y)dx &=\int\_{x\_A}^{x\_A+\Delta x}[P(x,y\_A)-P(x,y\_A+\Delta y)]dx\\\&=-\int\_{x\_A}^{x\_A+\Delta x}\int\_{y\_A}^{y\_A+\Delta y} \frac{\partial P}{\partial y}dydx.\end{align\*}的流体运动解释.

###矩形的合并
在叙述并证明Green定理之前,我们先给出一个概念:矩形的合并.并叙述与之相关的一个结论.

> **定义(矩形的合并):**平面上若干个内部互不相交的矩形,将这些矩形互相重合的线段都去掉.剩下的线段围成的区域叫做这些矩形的合并区域.

-----
![图3](/img/Green定理-3.png)

> **例 2.1:**如图3中的区域A-B-E-F-G-H-C-D-A就是由矩形A-B-C-D和矩形E-F-G-H合并而得到的.

--------
下面这个引理作为矩形Green定理的推广.

> **引理1:**设$G\_1,G\_2,\cdots,G\_n$是平面直角坐标系上的矩形,且这些矩形的边与相应的坐标轴平行.这些矩形的边界分别为$w\_1,w\_2,\cdots,w\_n$.这些矩形合并成一个单连通区域$D$,$D$的边界为$l$.函数 $P(x,y)$ 和$Q(x,y)$ 是在包含 $D$ 的一个开集上的从$\mathbf{R}^2$到$\mathbf{R}$的连续可微函数,则$$\iint\_D \left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)dxdy=\oint\_l Pdx+Qdy.$$这里右端为沿$D$的边界的积分,积分路径的方向是和趋于正向联系的,即当一个点沿着边界运动时区域 $D$ 恒在其左边(亦即服从右手法则).

----------
###Green定理

> **(Green 定理)** 设 $D$ 是被逐段光滑简单闭曲线 $l$ 所包围的平面区域.函数 $P(x,y)$ 和$Q(x,y)$ 在包含 $D$ 的一个开集上连续并具有对 $x$ 和 $y$ 的连续偏导数,则有$$\iint\_D \left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)dxdy=\oint\_l Pdx+Qdy.$$这里右端为沿有向闭路的积分,积分路径的方向是和趋于正向联系的,即当一个人沿着曲线 $l$ 行走时区域 $D$ 恒在其左边(亦即服从右手法则).

------------

> **注:**简单曲线就是指只有首尾相交,中间不自交的曲线,比如8字形的曲线不是简单曲线.光滑曲线的概念来自小平邦彦的《微积分入门》(人民邮电出版社2008年第410页):从实直线上的闭区间$I=[a,b]$到$\mathbf{R}^2$的连续映射$\gamma:t\to \gamma(t)=(\phi\_1(t),\phi\_2(t))$称为$\mathbf{R}^2$内的曲线.当$\phi\_1(t),\phi\_2(t)$连续可微且在$I$上恒有$\phi\_1'(t)^2+\phi_2'(t)^2>0$时,称$\gamma$为光滑曲线.在这里,我们把曲线和曲线的像混淆使用.根据隐函数定理,对于光滑曲线 $\gamma(t)$ 上的任意一点$(\gamma\_1(t),\gamma\_2(t))$ 来说,都存在 $\varepsilon(t)>0$,使得在$(t-\varepsilon(t),t+\varepsilon(t))$ 之内,$\gamma\_1(t)$ 和$\gamma\_2(t)$ 存在连续可微的函数关系,这样就明确了光滑曲线的性状.

--------
> **证明:**对于足够大的自然数$n$,在平面直角坐标系上作直线$y=\cdots,-\frac{2}{n},-\frac{1}{n},0,\frac{1}{n},\frac{2}{n},\cdots$以及直线$x=\cdots,-\frac{2}{n},-\frac{1}{n},0,\frac{1}{n},\frac{2}{n},\cdots$这样就把坐标平面分成了很多长和宽均为$\frac{1}{n}$的正方形.区域D自然也被很多长和宽均为$\frac{1}{n}$的正方形覆盖.把坐标平面上与区域D不相交的正方形都去掉,这样就得到覆盖区域D的数目最少的正方形.这些正方形合并成一个新的图形$D\_n$,其中$D\_n$的边界为$l\_n$.易得\begin{equation}\label{eq:1}\lim\_{n\to\infty}\oint\_{l\_n}Pdx+Qdy=\oint\_l Pdx+Qdy,\end{equation}且\begin{equation}  \label{eq:2}\lim\_{n\to\infty}\iint\_{D\_n}\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)dxdy=\iint\_{D}\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)dxdy.\end{equation}注意一下,虽然式\eqref{eq:1}中,当$n\to\infty$时,$l_n$不会越来越接近曲线$l$(前者一直呈锯齿状),但是式\eqref{eq:1}仍然成立.由式\eqref{eq:1}和式\eqref{eq:2},结合引理1,可得Green定理的确成立.
