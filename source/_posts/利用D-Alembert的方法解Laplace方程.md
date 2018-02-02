title: "利用D'Alembert的方法解Laplace方程"
date: 2015-04-14 19:42:34
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
在文章[D'Alembert如何解弦振动方程](/2015/04/12/D-Alembert如何解弦振动方程)里,我们利用矩阵对角化的方法解出了弦振动方程.在那篇文章的注里,我们还试图用同样的方法来解Laplace方程,但是失败了.今天睡醒之后我又想了一下,然后成功了.现在我们就用解弦振动方程的方法来解Laplace方程\begin{equation}\label{eq:1}\frac{\partial^2 u}{\partial x^2}=-\frac{\partial^2 u}{\partial y^2}.\end{equation}之所以想要研究这个方程,是因为这个方程和弦振动方程形式上的相似性,Laplace方程只不过比弦振动方程多了个负号.我们照样假设$u$是二阶连续可微的函数.令$\frac{du}{dx}=p(x,y),\frac{du}{dy}=q(x,y)$,则我们有全微分方程\begin{equation}  \label{eq:2}du=pdx+qdy.\end{equation}而且,方程\eqref{eq:1}变成\begin{equation}  \label{eq:3}  \frac{\partial p}{\partial x}=-\frac{\partial q}{\partial y}=k\_1(x,y).\end{equation}设$$\frac{\partial p}{\partial y}=k\_2(x,y),$$则我们有全微分方程\begin{equation}  \label{eq:4}  dp=k\_1dx+k\_2dy,\end{equation}以及\begin{equation}  \label{eq:5}  dq=k\_2dx-k\_1dy.\end{equation}同样,全微分方程\eqref{eq:4}和\eqref{eq:5}之所以共享同一个$k\_{2}$,乃是因为混合偏导数的Clairaut定理.将\eqref{eq:4}和\eqref{eq:5}合起来,可得
\begin{equation}
  \label{eq:6}
  \begin{pmatrix}
    dq\\\
    dp
  \end{pmatrix}=
  \begin{pmatrix}
    k\_2&-k\_1\\\
    k\_1&k\_2
  \end{pmatrix}
  \begin{pmatrix}
    dx\\\
    dy
  \end{pmatrix}.
\end{equation}
将矩阵
$$
  \begin{pmatrix}
    k\_2&-k\_1\\\
    k\_1&k\_2
  \end{pmatrix}
$$
对角化,可得
\begin{equation}\label{eq:7}
  \begin{pmatrix}
    k\_2&-k\_1\\\
    k\_1&k\_2
  \end{pmatrix}=
  \begin{pmatrix}
    \frac{i}{2}&\frac{1}{2}\\\
    -\frac{i}{2}&\frac{1}{2}
  \end{pmatrix}^{-1}
  \begin{pmatrix}
    k\_2-ik\_1&0\\\
    0&k\_2+ik\_1
  \end{pmatrix}
  \begin{pmatrix}
    \frac{i}{2}&\frac{1}{2}\\\
    -\frac{i}{2}&\frac{1}{2}
  \end{pmatrix},
\end{equation}
其中$i$是虚数单位.将\eqref{eq:7}代入\eqref{eq:6},可得
\begin{equation}
  \label{eq:8}
  \begin{pmatrix}
    \frac{i}{2}&\frac{1}{2}\\\
    \frac{-i}{2}&\frac{1}{2}
  \end{pmatrix}
  \begin{pmatrix}
    dq\\\
    dp
  \end{pmatrix}=
  \begin{pmatrix}
    k\_2-ik\_1&0\\\
    0&k\_2+ik\_1
  \end{pmatrix}
  \begin{pmatrix}
    \frac{i}{2}&\frac{1}{2}\\\
    \frac{-i}{2}&\frac{1}{2}
  \end{pmatrix}
  \begin{pmatrix}
    dx\\\
    dy
  \end{pmatrix}.
\end{equation}
不妨去掉\eqref{eq:8}中恼人的$\frac{1}{2}$,则\eqref{eq:8}变成
\begin{equation}
  \label{eq:9}
  \begin{pmatrix}
    i&1\\\
   -i&1
  \end{pmatrix}
  \begin{pmatrix}
    dq\\\
    dp
  \end{pmatrix}=
  \begin{pmatrix}
    k\_2-ik\_1&0\\\
    0&k\_2+ik\_1
  \end{pmatrix}
  \begin{pmatrix}
     i&1\\\
    -i&1
  \end{pmatrix}
  \begin{pmatrix}
    dx\\\
    dy
  \end{pmatrix}.
\end{equation}
令$ix+y=\xi\_1,-ix+y=\xi\_2,p+iq=P,p-iq=Q$.则$\xi\_1$和$\xi\_2$是共轭复函数,且$P$和$Q$是共轭复函数.则\eqref{eq:9}变成
\begin{equation}
  \label{eq:10}
  \begin{cases}
    dP=l\_1(\xi\_1,\xi\_2)d\xi\_1,\\\
    dQ=l\_2(\xi\_1,\xi\_2)d\xi\_2,
  \end{cases}
\end{equation}
其中$l\_1$和$l\_2$是共轭复函数,且
$$
l\_1(\xi\_1,\xi\_2)=k\_2(x,y)-ik\_1(x,y)=k\_2(\frac{\xi\_1-\xi\_2}{2i},\frac{\xi\_1+\xi\_2}{2})-ik\_1(\frac{\xi\_1-\xi\_2}{2i},\frac{\xi\_1+\xi\_2}{2}),
$$
$$
l\_2(\xi\_1,\xi\_2)=k\_2(x,y)+ik\_1(x,y)=k\_2(\frac{\xi\_1-\xi\_2}{2i},\frac{\xi\_1+\xi\_2}{2})+ik\_1(\frac{\xi\_1-\xi\_2}{2i},\frac{\xi\_1+\xi\_2}{2}).
$$
对\eqref{eq:10}积分可得,
$$
P=\int l\_1d\xi\_1,Q=\int l\_2d\xi\_2,
$$
这里涉及到的积分是复积分.于是,
\begin{equation}\label{eq:11} p=\frac{P+Q}{2}=\frac{\int
    l\_1d\xi\_1+\int
    l\_2d\xi\_2}{2}=\frac{f(\xi\_{1})+g(\xi\_{2})}{2},q=\frac{P-Q}{2i}=\frac{\int
    l\_1d\xi\_1-\int
    l\_2d\xi\_2}{2i}=\frac{f(\xi\_{1})-g(\xi\_{2})}{2i},\end{equation}
其中$f=\int l\_1d\xi\_{1},g=\int l\_2d\xi\_{2}$,且$f$和$g$是共轭复函数.将\eqref{eq:11}代入\eqref{eq:2},可得
\begin{equation}\label{eq:12}
du=\frac{1}{2i}\left[f(\xi\_1)d\xi\_1-g(\xi\_2)d\xi\_2\right].
\end{equation}
而且$du$是实函数.对\eqref{eq:12}积分可得
$$
u=F(\xi\_1)+G(\xi\_2)=F(y+ix)+G(y-ix),
$$
其中$F(\xi)=-\frac{i}{2}\int f(\xi\_{1})d\xi\_{1}$,$G(\xi)=\frac{i}{2}\int g(\xi\_2)d\xi\_2$.这样我们就得到了Laplace方程的解,而且由于共轭复函数的存在,保证了$u$始终是实函数.将这个解与波方程的D'Alembert解相比较可能会是有益的.
