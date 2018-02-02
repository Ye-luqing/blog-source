# 一般情形下轴向仿射造像方程式之推导
这是黄有训译，徐氏基金会出版的《解析几何学》下的第19章，习题6.在这里，我们致力于推导一般情形下轴向仿射的造像方程式.

![图1](/analytic-geometry-huangyouxun/p377/1.png)
在平面$E$内取单位向量$\overrightarrow{e\_{1}}$和$\overrightarrow{e\_{2}}$.其中向量$\overrightarrow{e\_{1}}$和$\overrightarrow{e\_{2}}$不是自由向量，而是固定向量，它们的起始点都位于点$O$处.且向量$\overrightarrow{e\_{1}}$的方向与$x$轴正方向相同,向量$\overrightarrow{e\_{2}}$的方向与$y$轴正方向相同.

设向量$\overrightarrow{e\_{2}}$在平行投影作用下，投影到平面$\overline{E}$上的向量为$\overrightarrow{m}$.且在平面$\overline{E}$上还有一个单位向量$\overrightarrow{e\_{3}}$,$\overrightarrow{e\_{3}}$是一个固定向量，它的起始点是$O$,方向与$\overline{y}$轴的正方向相同.

则
$$
\overrightarrow{OP}=x\overrightarrow{e\_{1}}+y\overrightarrow{e\_{2}},\overrightarrow{O\overline{P}}=x\overrightarrow{e\_{1}}+y\overrightarrow{m}.
$$
且
$$\overrightarrow{m}=\frac{1}{a}\overrightarrow{O\overline{P\_{0}}}=\frac{1}{a}\left(c\overrightarrow{e\_{1}}+b\overrightarrow{e\_{3}}\right),$$
因此
$$
\overrightarrow{O\overline{P}}=x\overrightarrow{e\_1}+y\overrightarrow{m}=x\overrightarrow{e\_1}+y(\frac{c}{a}\overrightarrow{e\_{1}}+\frac{b}{a}\overrightarrow{e\_3})=(x+\frac{c
}{a}y)\overrightarrow{e\_1}+\frac{b}{a}y\overrightarrow{e\_3}.
$$
可见，$\overline{x}=x+\frac{c}{a}y,\overline{y}=\frac{b}{a}y$.