# 定理一另证
第428页的定理一说：任何一种与直线反映及全等性不相同的轴向仿射性，具有恰好一个不变的直角对.在全等性与直线反映现象中，所有直角对都是不变的.

对于此结果，书上给出了基于平面几何的论述.在此，我给出代数证明.设向量$\mathbf{v}=(x\_1,y\_1),\mathbf{w}=(x\_2,y\_2)$代表平面上的两个方向.在轴向仿射
\begin{equation}\label{eq:1}
\begin{cases}
  \overline{x}=x+ry\\\
\overline{y}=ky
\end{cases}
\end{equation}
的作用下，设向量$\mathbf{v},\mathbf{w}$分别变为向量$\mathbf{v}'=(\overline{x\_{1}},\overline{y\_{1}}),\mathbf{w}'=(\overline{x\_{2}},\overline{y\_{2}})$.

若向量$\mathbf{v}\_1,\mathbf{w}\_{1}$互相垂直，则
\begin{equation}
  \label{eq:2}
  x\_1x\_2+y\_1y\_2=0
\end{equation}
向量$\mathbf{v}',\mathbf{w}'$互相垂直，则
\begin{equation}
  \label{eq:3}
  \overline{x\_1}\overline{x\_2}+\overline{y\_1}\overline{y\_2}=0,
\end{equation}
将关系\eqref{eq:1}代入式\eqref{eq:3},再进一步整理可得
\begin{equation}
  \label{eq:4}
  x\_1x\_2+r(x\_1y\_2+y\_1x\_2)+(r^2+k^2)y\_1y\_2=0.
\end{equation}
将关系\eqref{eq:2}代入关系\eqref{eq:4},再整理可得
\begin{equation}
  \label{eq:5}
  r(x\_1y\_2+y\_1x\_2)+(r^2+k^2-1)y\_1y\_2=0.
\end{equation}
当$y\_1y\_2\neq 0$，且$r\neq 0$时，式\eqref{eq:2}和式\eqref{eq:5}联立，等价于
$$
\begin{cases}
\frac{x\_1}{y\_1}\cdot \frac{x\_2}{y\_2}=-1.\\\
  r(\frac{x\_1}{y\_1}+\frac{x\_2}{y\_2})+(r^2+k^2-1)=0\\\
\end{cases}
$$
上面的方程组有解，由向量$\mathbf{v},\mathbf{w}$地位的对称性，上面的解其实只是代表了一对正交方向.

当$y\_1y\_2\neq 0$,且$r=0$时，$k=\pm 1$.此时，轴向仿射变成了全等造像，或者是关于$x$轴的对称造像.此时，满足$y\_1y\_2\neq 0$的所有正交方向都满足在该轴向仿射下仍然是正交方向.

当$y\_1y\_2=0$时，由向量$\mathbf{v},\mathbf{w}$地位的对称性，不妨设$y\_1=0,y\_2\neq 0$（若$y\_{1},y\_{2}$都为$0$则向量$\mathbf{v},\mathbf{w}$将同向或反向，不能起到代表不同方向的作用）.此时，
$$
rx\_1=0,x\_1x\_2=0.
$$
由于此时$x\_1\neq 0$,因此$r=0,x\_2=0$.此时，对应的轴向仿射是与$x$轴正交的仿射.向量对$(1,0)$和$(0,1)$在该正交仿射下，变成的两个向量方向依旧垂直.

综上所述，定理一成立.
