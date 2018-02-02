---
title: Lagrange恒等式
date: 2016-10-30 11:16:11
categories:
- 数学
- 线性代数
tags:
- 行列式
- 二面角
- Lagrange恒等式
- 向量积

---
Lagrange恒等式是说：
\begin{equation}
  \label{eq:1}
  \left(\overrightarrow{OA}\times\overrightarrow{OB}\right)\cdot \left(\overrightarrow{OC}\times\overrightarrow{OD}\right)=
  \begin{vmatrix}
    \overrightarrow{OA}\cdot\overrightarrow{OC}&\overrightarrow{OB}\cdot\overrightarrow{OC}\\\\
\overrightarrow{OA}\cdot\overrightarrow{OD}&\overrightarrow{OB}\cdot\overrightarrow{OD}
  \end{vmatrix}.
\end{equation}
下证之.令$\overrightarrow{OA'}=\overrightarrow{OA}-t\overrightarrow{OB}$,使得$\overrightarrow{OA'}\perp\overrightarrow{OB}$.易得这样的$t$是唯一存在的.且,由向量积的性质,易得
\begin{equation}
  \label{eq:2}
  (\overrightarrow{OA}\times\overrightarrow{OB})\cdot(\overrightarrow{OC}\times\overrightarrow{OD})=(\overrightarrow{OA'}\times\overrightarrow{OB})\cdot(\overrightarrow{OC}\times\overrightarrow{OD}).
\end{equation}
而且，由行列式的性质，我们有
\begin{equation}
  \label{eq:3}
\begin{vmatrix}
    \overrightarrow{OA}\cdot\overrightarrow{OC}&\overrightarrow{OB}\cdot\overrightarrow{OD}\\\\
\overrightarrow{OA}\cdot\overrightarrow{OD}&\overrightarrow{OB}\cdot\overrightarrow{OC}
  \end{vmatrix}=\begin{vmatrix}
    \overrightarrow{OA'}\cdot\overrightarrow{OC}&\overrightarrow{OB}\cdot\overrightarrow{OC}\\\\
\overrightarrow{OA'}\cdot\overrightarrow{OD}&\overrightarrow{OB}\cdot\overrightarrow{OD}
  \end{vmatrix}.
\end{equation}
关系式\eqref{eq:2}和\eqref{eq:3}表明，Lagrange恒等式\eqref{eq:1}等价于
\begin{equation}
  \label{eq:4}
    \left(\overrightarrow{OA'}\times\overrightarrow{OB}\right)\cdot \left(\overrightarrow{OC}\times\overrightarrow{OD}\right)=
  \begin{vmatrix}
    \overrightarrow{OA'}\cdot\overrightarrow{OC}&\overrightarrow{OB}\cdot\overrightarrow{OC}\\\\
\overrightarrow{OA'}\cdot\overrightarrow{OD}&\overrightarrow{OB}\cdot\overrightarrow{OD}
  \end{vmatrix}.
\end{equation}
令$\overrightarrow{OA''}=\frac{\overrightarrow{OA}}{|\overrightarrow{OA}|}$,$\overrightarrow{OB'}=\frac{\overrightarrow{OB}}{|\overrightarrow{OB}|}$,则由向量积和行列式的性质，式\eqref{eq:4}等价于
\begin{equation}
  \label{eq:5}
     \left(\overrightarrow{OA''}\times\overrightarrow{OB'}\right)\cdot \left(\overrightarrow{OC}\times\overrightarrow{OD}\right)=
  \begin{vmatrix}
    \overrightarrow{OA''}\cdot\overrightarrow{OC}&\overrightarrow{OB'}\cdot\overrightarrow{OC}\\\\
\overrightarrow{OA''}\cdot\overrightarrow{OD}&\overrightarrow{OB'}\cdot\overrightarrow{OD}
  \end{vmatrix}, 
\end{equation}
其中$(\overrightarrow{OA''},\overrightarrow{OB'})$形成单位正交基.结合行列式的几何意义（平行四边形的有向面积），等式\eqref{eq:5}的右边是向量$\overrightarrow{OC},\overrightarrow{OD}$张成的平行四边形在向量$\overrightarrow{OA''},\overrightarrow{OB'}$张成的平面上的投影所得的平行四边形的有向面积,这恰好就是该式左边的几何意义.因此Lagrange恒等式成立.