title: "D'Alembert如何解弦振动方程"
date: 2015-04-12 13:18:32
categories:
- 数学
- 微分方程
tags:
- D'Alembert公式
- 波方程
- Laplace方程
- 弦振动
- 矩阵对角化
---
在1747年,D'Alembert发表了他的论文《张紧的弦振动时形成的曲线的研究》(Recherches sur la courbe que forme une corde tendue mise en vibration).这篇文章的节选中译本可以在李文林主编的《数学珍宝:历史文献精选》中找到.在这篇文章里,他研究了弦振动并推导出了弦振动方程,用今天的话来说,该方程是\begin{equation}\label{eq:1}
\frac{\partial^2 u}{\partial t^2}=\frac{\partial^2 u}{\partial x^2}.
\end{equation}其中$u(x,t)$是二阶连续可微函数.下面,我们遵照D'Alembert的精神,求解偏微分方程\eqref{eq:1}.当然,涉及矩阵对角化的那一段,是我自己帮他加上的(因为D'Alembert那个时候没有矩阵的概念,当然,他自己心里应该有类似目的,即便矩阵的概念还没诞生).这种解法和当今的多数教材在形式上有所差别.令$\frac{du}{dt}=p(x,t)$,$\frac{du}{dx}=q(x,t)$,则我们有全微分方程\begin{equation}\label{eq:2} du=pdt+qdx.\end{equation}弦振动方程\eqref{eq:1}等价于
\begin{equation}
  \label{eq:3}
  \frac{\partial p}{\partial t}=\frac{\partial q}{\partial x}=k\_1(x,t)
\end{equation}
设
$$
设\frac{\partial p}{\partial x}=k\_{2}(x,t),
$$
则我们有全微分方程
\begin{equation}
  \label{eq:4}
  dp=k\_1dt+k\_2dx,
\end{equation}
以及
\begin{equation}
  \label{eq:5}
  dq= k\_2dt+k\_1dx.
\end{equation}
全微分方程\eqref{eq:4}和\eqref{eq:5}之所以共享同一个$k\_2$,乃是因为[混合偏导数的Clairaut定理](/2015/02/23/混合偏导数的Clairaut定理/)(该定理当然并非Clairaut发现).而且这两个全微分方程已经包含了所有信息.\eqref{eq:4}和\eqref{eq:5}合起来,可以写为
\begin{equation}
  \label{eq:6}
  \begin{pmatrix}
    dp\\\
    dq
  \end{pmatrix}=
  \begin{pmatrix}
    k\_1&k\_2\\\
    k\_2&k\_1
  \end{pmatrix}
  \begin{pmatrix}
    dt\\\
    dx
  \end{pmatrix}.
\end{equation}
我们很幸运地发现
$$
  \begin{pmatrix}
    k\_1&k\_2\\\
    k\_2&k\_1
  \end{pmatrix}
$$
是一个实对称矩阵,为此要好好谢谢混合偏导数的Clairaut定理.我们将该实对称矩阵对角化,对角化的最终目的是为了便于积分.易得
$$
  \begin{pmatrix}
    k\_1&k\_2\\\
    k\_2&k\_1
  \end{pmatrix}=
  \begin{pmatrix}
    1&1\\\
    1&-1
  \end{pmatrix}^{-1}
  \begin{pmatrix}
    k\_1+k\_2&0\\\
0&k\_1-k\_2
  \end{pmatrix}
  \begin{pmatrix}
    1&1\\\
1&-1
  \end{pmatrix},
$$
代入式\eqref{eq:6}可得
\begin{equation}\label{eq:7}
\begin{pmatrix}
  1&1\\\
  1&-1
\end{pmatrix}
\begin{pmatrix}
  dp\\\
  dq
\end{pmatrix}=\begin{pmatrix}
    k\_1+k\_2&0\\\
0&k\_1-k\_2
  \end{pmatrix}
  \begin{pmatrix}
    1&1\\\
1&-1
  \end{pmatrix}
  \begin{pmatrix}
    dt\\\
    dx
  \end{pmatrix}.
\end{equation}
式\eqref{eq:7}也就是
\begin{equation}
  \label{eq:8}
  \begin{cases}
       d(p+q)=(k\_1+k\_2)d(t+x),\\\
    d(p-q)=(k\_1-k\_2)d(t-x)
  \end{cases}.
\end{equation}
令$t+x=\xi\_1,t-x=\xi\_2,p+q=P,p-q=Q$,则\eqref{eq:8}变为
\begin{equation}
  \label{eq:9}
\begin{cases}
  dP=l\_{1}(\xi\_1,\xi\_2)d\xi\_1,\\\
  dQ=l\_2(\xi\_1,\xi\_2)d\xi\_2
\end{cases},
\end{equation}
其中函数
$$l\_1(\xi\_1,\xi\_2)=k\_1(x,t)+k\_{2}(x,t)=k\_1(\frac{\xi\_1-\xi\_2}{2},\frac{\xi\_1+\xi\_2}{2})+k\_2(\frac{\xi\_1-\xi\_2}{2},\frac{\xi\_1+\xi\_2}{2}),$$
$$l\_{2}(\xi\_1,\xi\_2)=k\_1(x,t)-k\_{2}(x,t)=k\_1(\frac{\xi\_1-\xi\_2}{2},\frac{\xi\_1+\xi\_2}{2})-k\_2(\frac{\xi\_1-\xi\_2}{2},\frac{\xi\_1+\xi\_2}{2}).$$对\eqref{eq:9}积分可得
$$
P=\int l\_1d\xi\_1,Q=\int l\_2d\xi\_2.
$$
于是,
\begin{equation}\label{eq:10}
p=\frac{P+Q}{2}=\frac{\int l\_1d\xi\_1+\int l\_2d\xi\_2}{2}=\frac{f(\xi\_{1})+g(\xi\_{2})}{2},q=\frac{P-Q}{2}=\frac{\int l\_1d\xi\_1-\int l\_2d\xi\_2}{2}=\frac{f(\xi\_{1})-g(\xi\_{2})}{2},
\end{equation}
其中$f=\int l\_1d\xi\_{1},g=\int l\_2d\xi\_{2}$.将\eqref{eq:10}代入\eqref{eq:2},可得
\begin{equation}
  \label{eq:11}
  du=\frac{f(\xi\_1)}{2}d\xi\_1+\frac{g(\xi\_2)}{2}d\xi\_2.
\end{equation}
对式\eqref{eq:11}积分,可得
$$
u=F(\xi\_1)+G(\xi\_2)=F(t+x)+G(t-x).
$$
这样就给出了偏微分方程\eqref{eq:1}的解.

>*注*:同样的方法对于椭圆型偏微分方程——Laplace方程失效.下面是我的一次失败尝试.

>我们尝试用类似的方法来研究著名的Laplace方程
\begin{equation}\label{eq:2.1}
\frac{\partial^2 u}{\partial x^2}=-\frac{\partial^2 u}{\partial y^2}.
\end{equation}
之所以想要研究这个方程,是因为这个方程和弦振动方程形式上的相似性,Laplace方程只不过比弦振动方程多了个负号.我们照样假设$u$是二阶连续可微的函数.令$\frac{du}{dx}=p(x,y),\frac{du}{dy}=q(x,y)$,则我们有全微分方程
\begin{equation}
  \label{eq:2.2}
du=pdx+qdy.
\end{equation}
而且,方程\eqref{eq:2.1}变成
\begin{equation}
  \label{eq:2.3}
  \frac{\partial p}{\partial x}=-\frac{\partial q}{\partial y}=k\_1(x,y).
\end{equation}
设
$$
\frac{\partial p}{\partial y}=k\_2(x,y),
$$
则我们有全微分方程
\begin{equation}
  \label{eq:2.4}
  dp=k\_1dx+k\_2dy,
\end{equation}
以及
\begin{equation}
  \label{eq:2.5}
  dq=k\_2dx-k\_1dy.
\end{equation}
同样,全微分方程\eqref{eq:2.4}和\eqref{eq:2.5}之所以共享同一个$k\_{2}$,乃是因为混合偏导数的Clairaut定理.将\eqref{eq:2.4}和\eqref{eq:2.5}合起来,可得
\begin{equation}
  \label{eq:2.6}
  \begin{pmatrix}
    dp\\\
    dq
  \end{pmatrix}=
  \begin{pmatrix}
    k\_1&k\_2\\\
    k\_2&-k\_1
  \end{pmatrix}
  \begin{pmatrix}
    dx\\\
    dy
  \end{pmatrix}.
\end{equation}
将实对称矩阵
$$
  \begin{pmatrix}
    k\_1&k\_2\\\
    k\_2&-k\_1
  \end{pmatrix}
$$
对角化,可得
\begin{equation}
  \label{eq:2.7}
  \begin{pmatrix}
    k\_1&k\_2\\\
    k\_2&-k\_1
  \end{pmatrix}=
    \begin{pmatrix}
\frac{-k\_2}{2 \sqrt{k\_1^2+k\_2^2}}&\frac{k\_1}{2
  \sqrt{k\_1^2+k\_2^2}}+\frac{1}{2}\\\
\frac{k\_2}{2 \sqrt{k\_1^2+k\_2^2}}&\frac{-k\_1}{2 \sqrt{k\_1^2+k\_2^2}}+\frac{1}{2}
  \end{pmatrix}^{-1}
  \begin{pmatrix}
    -\sqrt{k\_1^2+k\_2^2}&0\\\
    0& \sqrt{k\_1^2+k\_2^2}
  \end{pmatrix}
  \begin{pmatrix}
\frac{-k\_2}{2 \sqrt{k\_1^2+k\_2^2}}&\frac{k\_1}{2
  \sqrt{k\_1^2+k\_2^2}}+\frac{1}{2}\\\
\frac{k\_2}{2 \sqrt{k\_1^2+k\_2^2}}&\frac{-k\_1}{2 \sqrt{k\_1^2+k\_2^2}}+\frac{1}{2}
  \end{pmatrix}.
\end{equation}
将\eqref{eq:2.7}代入\eqref{eq:2.6},可得
\begin{equation}
  \label{eq:2.8}
   \begin{pmatrix}
\frac{-k\_2}{2 \sqrt{k\_1^2+k\_2^2}}&\frac{k\_1}{2
  \sqrt{k\_1^2+k\_2^2}}+\frac{1}{2}\\\
\frac{k\_2}{2 \sqrt{k\_1^2+k\_2^2}}&\frac{-k\_1}{2 \sqrt{k\_1^2+k\_2^2}}+\frac{1}{2}
  \end{pmatrix}
  \begin{pmatrix}
    dp\\\
    dq
  \end{pmatrix}=  \begin{pmatrix}
    -\sqrt{k\_1^2+k\_2^2}&0\\\
    0& \sqrt{k\_1^2+k\_2^2}
  \end{pmatrix}
  \begin{pmatrix}
\frac{-k\_2}{2 \sqrt{k\_1^2+k\_2^2}}&\frac{k\_1}{2
  \sqrt{k\_1^2+k\_2^2}}+\frac{1}{2}\\\
\frac{k\_2}{2 \sqrt{k\_1^2+k\_2^2}}&\frac{-k\_1}{2 \sqrt{k\_1^2+k\_2^2}}+\frac{1}{2}
  \end{pmatrix}
  \begin{pmatrix}
    dx\\\
    dy
  \end{pmatrix}.
\end{equation}
然后就做不下去了.
