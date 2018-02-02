这是黄友训译，徐氏基金会出版的《解析几何学》下的第20章，习题1的三个作图文件.
[a](/analytic-geometry-huangyouxun/p386/1.ggb)[b](/analytic-geometry-huangyouxun/p386/2.ggb)[c](/analytic-geometry-huangyouxun/p386/3.ggb)

# 利用轴向仿射的平面作图法推导仿射造像方程式
在[一般情形下轴向仿射造像方程式之推导](/analytic-geometry-huangyouxun/p377/)里, 我们利用向量法推导出了轴向仿射的造像方程式.只是那里我们是借助于空间中的两个平面进行推导的.在这里,我们利用轴向仿射的平面作图法，再次来推导轴向仿射的造像方程式.

![图1](/analytic-geometry-huangyouxun/p386/4.png)
如图，平面上的仿射造像以$x$轴为仿射轴，它把点$P\_0(0,a)$映射为点$\overline{P\_0}(c,b)$.该仿射造像把任意一点$P(x,y)$变成点$\overline{P}(\overline{x},\overline{y})$.下面我们来研究$(x,y)$和$(\overline{x},\overline{y})$之间的关系.

由直线方程的相关知识，可以求得直线$PP\_{0}$与$x$轴的交点$T$的坐标为$(\frac{ax}{a-y},0)$.由于直线$P\overline{P}$和直线$P\_0\overline{P\_0}$平行，因此存在实数$\lambda$,使得
$$
\overrightarrow{P\overline{P}}=\lambda \overrightarrow{P\_0\overline{P\_{0}}},
$$
即
\begin{equation}\label{eq:1}
(\overline{x}-x,\overline{y}-y)=\lambda(c,b-a).\iff
\begin{cases}
  \overline{x}=x+\lambda c\\\
\overline{y}=y+\lambda (b-a)
\end{cases}
\end{equation}
下面我们来求$\lambda$.易得$\overrightarrow{TP}=\lambda\overrightarrow{TP\_0}$,即
$$
(x-\frac{ax}{a-y},y)=\lambda(-\frac{ax}{a-y},a),
$$
解得$\lambda a=y$.将其代入关系\eqref{eq:1},可得
$$
\begin{cases}
  \overline{x}=x+\frac{c}{a}y\\\
\overline{y}=\frac{b}{a}y
\end{cases}.
$$