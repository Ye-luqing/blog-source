# 复平面上的点关于圆周的反演点

设$z$是复平面上的一个点.圆$K$是以点$q$为圆心,以$R$为半径的一个圆.其中$z,q\in \mathbf{C}$,且$z\neq q$.$R\in \mathbf{R}$.作点$z$关于圆$K$的反演点.现在,我们来求点$z$的反演点$z'$.

首先,由反演点的定义,可得
\begin{equation}
  \label{eq:1.1}
  |z'-q||z-q|=R^2\iff |(z'-q)(z-q)|=R^2\iff \overline{z'-q}(z'-q)\overline{z-q}(z-q)=R^4.
\end{equation}
而且,
\begin{equation}
  \label{eq:2.1}
  z'-q=\lambda(z-q),
\end{equation}
其中$\lambda>0$.由式\eqref{eq:1.1}和式\eqref{eq:2.1}可得,
\begin{equation}
  \label{eq:3.1}
  \lambda^2|z-q|^4=R^4\iff \lambda=\frac{R^2}{(z-q)\overline{z-q}}.
\end{equation}
将\eqref{eq:3.1}代入\eqref{eq:2.1},可得
\begin{equation}
  \label{eq:4.1}
  z'-q=\frac{R^2}{\overline{z}-\overline{q}}.
\end{equation}
这样就求出了点$z'$.