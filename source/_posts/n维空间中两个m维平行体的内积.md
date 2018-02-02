title: $n$ 维空间中两个 $m$ 维有向平行体的内积
date: 2015/2/14 20:46:25
categories:
- 数学
- 线性代数
tags:
- 有向平行体
- 内积
- 行列式
- Gram行列式
- gram-schmidt正交化
---

我们知道,对于 $\mathbf{R}^n$ 中的两个向量 $\mathbf{p}=(p\_1,p\_2,\cdots,p\_n)$ 和向量 $\mathbf{q}=(q\_1,q\_2,\cdots,q\_n)$,它们之间的内积是
$$
|\mathbf{p}||\mathbf{q}|\cos\alpha,
$$
其中 $|\mathbf{p}|,|\mathbf{q}|$ 是两个向量的长度,$\alpha$ 是两个向量之间的夹角.也许读者觉得难以想像 $n$ 维空间中两个向量的夹角,毕竟很多人的经验都只是停留在 $n=1,2,3$ 的情形.其实可以这样想像:只考虑 $n$ 维空间中两个向量 $\mathbf{p},\mathbf{q}$ 张成的二维子空间,这个二维子空间就是我们喜闻乐见的二维平面.然后只在该二维平面上看两个向量的夹角,此时你所看到的两个向量的夹角就是 $\alpha$.


然后在 $\mathbf{p},\mathbf{q}$ 张成的二维平面上使用余弦定理,可得
$$
\cos\alpha
=\frac{|\mathbf{p}|^2+|\mathbf{q}|^2-|\mathbf{p}-\mathbf{q}|^2}{2
|\mathbf{p}||\mathbf{q}|},
$$
于是,两个向量的内积就是
\begin{align\*}
|\mathbf{p}||\mathbf{q}|\cos\alpha&=|\mathbf{p}||\mathbf{q}| \frac{|\mathbf{p}|^2+|\mathbf{q}|^2-|\mathbf{p}-\mathbf{q}|^2}{2|\mathbf{p}||\mathbf{q}|}\\\&=\frac{|\mathbf{p}|^2+|\mathbf{q}|^2-|\mathbf{p}-\mathbf{q}|^2}{2}\\\&=p\_1q\_1+p\_2q\_2+\cdots+p\_nq\_n.
\end{align\*}
这就是我们熟知的两个向量的内积公式.


如果向量 $\mathbf{p}$ 在向量 $\mathbf{q}$ 所张成的子空间上的正投影 $\mathbf{p}'$ 和向量 $\mathbf{q}$ 的方向相同,则两个向量的夹角是锐角;方向相反,则夹角是钝角.若 $\mathbf{p}'=\mathbf{0}$,则两个向量垂直.


以上都是我们所熟知的事实.在这里,我们要将这些熟知的事实进行高维推广.首先,我们将 $\mathbf{R}^n$ 中的向量推广为 $\mathbf{R}^n$ 中的有向平行体.

> **定义1(有向平行体)** 设 $ \mathbf{a}\_1,\mathbf{a}\_2,\cdots,\mathbf{a}\_m $ 是 $ \mathbf{R}^n $ 中的 $ m $ 个向量.集合$$ \\{p\_1\mathbf{a}\_1+p\_2\mathbf{a}\_2+\cdots+p\_m\mathbf{a}\_m:p\_1,p\_2,\cdots,p\_m\geq 0,p\_1+p\_2+\cdots+p\_m\leq 1\\} $$ 叫做 $ \mathbf{R}^{n} $ 中由向量 $ \mathbf{a}\_1,\mathbf{a}\_2,\cdots,\mathbf{a}\_m $ 张成的一个有向平行体.

设 $ A $ 是 $ \mathbf{R}^{n} $ 中由 $ m $ 个线性无关的向量 $ \mathbf{a}\_1,\mathbf{a}\_2,\cdots,\mathbf{a}\_m $ 张成的一个 $ m $ 维有向平行体. $ B $ 是 $ \mathbf{R}^n $ 中由 $ m $ 个线性无关的向量$ \mathbf{b}\_1,\mathbf{b}\_2,\cdots,\mathbf{b}\_m $ 张成的一个 $ m $ 维有向平行体.其中 $ m<n $ .

然后,我们来考虑有向平行体 $ A $ 在有向平行体 $ B $ 所在的子空间上进行投影后得到的有向平行体的 $m$ 维有向体积,与有向平行体 $ B $ 的 $m$ 维有向体积相乘而得到的结果.这与 $ \mathbf{R}^n $ 中两个向量的内积类似,可以看作是一种推广.因此我们称其为 $ \mathbf{R}^n $ 中两个 $ m $ 维有向平行体之间的内积.

设向量 $ \mathbf{a}\_j $ 在 $ \mathbf{b}\_1,\mathbf{b}\_2,\cdots,\mathbf{b}\_m $ 张成的子空间上的正投影为 $ \mathbf{a}\_j' $ ,易得 $ \mathbf{a}\_j' $ 是存在且唯一的,而且 $ \forall 1\leq i,j\leq m $ ,
\begin{equation}\label{eq:1}
(\mathbf{a}\_j-\mathbf{a}\_j')\cdot \mathbf{b}\_i=0.\iff \mathbf{a}\_j\cdot\mathbf{b}\_i=\mathbf{a}\_j'\cdot\mathbf{b}\_i.
\end{equation}

+ 当 $ \mathbf{b}\_1,\mathbf{b}\_2,\cdots,\mathbf{b}\_m $ 是两两正交的向量时.设 $ \mathbf{a}\_j'=x\_{1j}\mathbf{b}\_1+x\_{2j}\mathbf{b}\_2+\cdots+x\_{mj}\mathbf{b}\_m $ ,代入关系式\eqref{eq:1},可得 $ x\_{ij}|b\_i|^2=\mathbf{a}\_j\cdot
\mathbf{b}\_i $ .令 $ \mathbf{e}\_i=\frac{\mathbf{b}\_i}{|\mathbf{b}\_i|} $ ,可得 $ x\_{ij}=\mathbf{a}\_j\cdot\mathbf{e}\_i $ .于是
 $$ 
\begin{cases}
  \mathbf{a}\_1'=(\mathbf{a}\_1\cdot
  \mathbf{e}\_1)\mathbf{e}\_1+(\mathbf{a}\_1\cdot
  \mathbf{e}\_2)\mathbf{e}\_2+\cdots+(\mathbf{a}\_1\cdot
  \mathbf{e}\_m)\mathbf{e}\_m,\\\
  \mathbf{a}\_2'=(\mathbf{a}\_2\cdot
  \mathbf{e}\_1)\mathbf{e}\_1+(\mathbf{a}\_2\cdot
  \mathbf{e}\_2)\mathbf{e}\_2+\cdots+(\mathbf{a}\_2\cdot
  \mathbf{e}\_m)\mathbf{e}\_m,\\\
\vdots\\\
  \mathbf{a}\_m'=(\mathbf{a}\_m\cdot
  \mathbf{e}\_1)\mathbf{e}\_1+(\mathbf{a}\_m\cdot
  \mathbf{e}\_2)\mathbf{e}\_2+\cdots+(\mathbf{a}\_m\cdot
  \mathbf{e}\_m)\mathbf{e}\_m.
\end{cases}
 $$ 
可见,在标架 $ (\mathbf{e}\_1,\mathbf{e}\_2,\cdots,\mathbf{e}\_m) $ 下,由 $ \mathbf{a}\_1',\mathbf{a}\_2',\cdots,\mathbf{a}\_m' $ 张成的有向平行体的 $m$ 维有向体积为
 $$ 
\begin{vmatrix}
  \mathbf{a}\_1\cdot \mathbf{e}\_1&\mathbf{a}\_1\cdot
  \mathbf{e}\_2&\cdots&\mathbf{a}\_1\cdot \mathbf{e}\_m\\\
  \mathbf{a}\_2\cdot \mathbf{e}\_1&\mathbf{a}\_2\cdot
  \mathbf{e}\_2&\cdots&\mathbf{a}\_2\cdot \mathbf{e}\_m\\\
\vdots&\vdots&\ddots&\vdots\\\
  \mathbf{a}\_m\cdot \mathbf{e}\_1&\mathbf{a}\_m\cdot
  \mathbf{e}\_2&\cdots&\mathbf{a}\_m\cdot \mathbf{e}\_m
\end{vmatrix}.
 $$ 
于是,
 $$ 
  \begin{vmatrix}
  \mathbf{a}\_1\cdot \mathbf{b}\_1&\mathbf{a}\_1\cdot
  \mathbf{b}\_2&\cdots&\mathbf{a}\_1\cdot \mathbf{b}\_m\\\
  \mathbf{a}\_2\cdot \mathbf{b}\_1&\mathbf{a}\_2\cdot
  \mathbf{b}\_2&\cdots&\mathbf{a}\_2\cdot \mathbf{b}\_m\\\
\vdots&\vdots&\ddots&\vdots\\\
  \mathbf{a}\_m\cdot \mathbf{b}\_1&\mathbf{a}\_m\cdot
  \mathbf{b}\_2&\cdots&\mathbf{a}\_m\cdot \mathbf{b}\_m\\\
\end{vmatrix}=|\mathbf{b}\_1||\mathbf{b}\_2|\cdots |\mathbf{b}\_m|\begin{vmatrix}
  \mathbf{a}\_1\cdot \mathbf{e}\_1&\mathbf{a}\_1\cdot
  \mathbf{e}\_2&\cdots&\mathbf{a}\_1\cdot \mathbf{e}\_m\\\
  \mathbf{a}\_2\cdot \mathbf{e}\_1&\mathbf{a}\_2\cdot
  \mathbf{e}\_2&\cdots&\mathbf{a}\_2\cdot \mathbf{e}\_m\\\
\vdots&\vdots&\ddots&\vdots\\\
  \mathbf{a}\_m\cdot \mathbf{e}\_1&\mathbf{a}\_m\cdot
  \mathbf{e}\_2&\cdots&\mathbf{a}\_m\cdot \mathbf{e}\_m\\\
\end{vmatrix}
 $$ 
等于标架 $ (\mathbf{e}\_1,\mathbf{e}\_2,\cdots,\mathbf{e}\_m) $ 下 $ \mathbf{a}\_1',\mathbf{a}\_2',\cdots,\mathbf{a}\_m' $ 张成的有向平行体的 $m$ 维有向体积(可正可负),再乘以同一个标架下 $ \mathbf{b}\_1,\mathbf{b}\_2,\cdots,\mathbf{b}\_m $ 张成的有向平行体的 $m$ 维有向体积 $ |\mathbf{b}\_1||\mathbf{b}\_2|\cdots |\mathbf{b}\_m| $ (为正).

+ 当 $ \mathbf{b}\_1,\mathbf{b}\_2,\cdots,\mathbf{b}\_m $ 并非都是两两正交向量时,可以利用[Gram-Schimit 正交化](http://zh.wikipedia.org/wiki/%E6%A0%BC%E6%8B%89%E5%A7%86-%E6%96%BD%E5%AF%86%E7%89%B9%E6%AD%A3%E4%BA%A4%E5%8C%96)将向量组 $ \\{\mathbf{b}\_1,\mathbf{b}\_2,\cdots,\mathbf{b}\_m\\} $ 正交化成为向量组 $ \\{\mathbf{b}\_1',\mathbf{b}\_2',\cdots,\mathbf{b}\_m'\\} $ .设 $ (\mathbf{e}\_1',\mathbf{e}\_2',\cdots,\mathbf{e}\_m')=(\frac{\mathbf{b}\_1'}{|\mathbf{b}\_1'|},\frac{\mathbf{b}\_2'}{|\mathbf{b}\_2'|},\cdots,\frac{\mathbf{b}\_m'}{|\mathbf{b}\_m'|}) $ .根据行列式的性质(某一列(行)乘以常数加到另外一列(行)上,行列式不变),在标架 $ (\mathbf{e}\_1',\mathbf{e}\_2',\cdots,\mathbf{e}\_m') $ 下,向量 $ \mathbf{b}\_1,\mathbf{b}\_2,\cdots,\mathbf{b}\_m $ 张成的有向平行体的$m$ 维有向体积和向量 $ \mathbf{b}\_1',\mathbf{b}\_2',\cdots,\mathbf{b}\_m' $ 张成的有向平行体的$m$ 维有向体积相等(都为正),且
 $$ 
  \begin{vmatrix}
  \mathbf{a}\_1\cdot \mathbf{b}\_1&\mathbf{a}\_1\cdot
  \mathbf{b}\_2&\cdots&\mathbf{a}\_1\cdot \mathbf{b}\_m\\\
  \mathbf{a}\_2\cdot \mathbf{b}\_1&\mathbf{a}\_2\cdot
  \mathbf{b}\_2&\cdots&\mathbf{a}\_2\cdot \mathbf{b}\_m\\\
\vdots&\vdots&\ddots&\vdots\\\
  \mathbf{a}\_m\cdot \mathbf{b}\_1&\mathbf{a}\_m\cdot
  \mathbf{b}\_2&\cdots&\mathbf{a}\_m\cdot \mathbf{b}\_m\\\
\end{vmatrix}=  \begin{vmatrix}
  \mathbf{a}\_1\cdot \mathbf{b}\_1'&\mathbf{a}\_1\cdot
  \mathbf{b}\_2'&\cdots&\mathbf{a}\_1\cdot \mathbf{b}\_m'\\\
  \mathbf{a}\_2\cdot \mathbf{b}\_1'&\mathbf{a}\_2\cdot
  \mathbf{b}\_2'&\cdots&\mathbf{a}\_2\cdot \mathbf{b}\_m'\\\
\vdots&\vdots&\ddots&\vdots\\\
  \mathbf{a}\_m\cdot \mathbf{b}\_1'&\mathbf{a}\_m\cdot
  \mathbf{b}\_2'&\cdots&\mathbf{a}\_m\cdot \mathbf{b}\_m'\\\
\end{vmatrix}.
 $$ 
因此此时
 \begin{equation}\label{eq:2}
  \begin{vmatrix}
  \mathbf{a}\_1\cdot \mathbf{b}\_1&\mathbf{a}\_1\cdot
  \mathbf{b}\_2&\cdots&\mathbf{a}\_1\cdot \mathbf{b}\_m\\\
  \mathbf{a}\_2\cdot \mathbf{b}\_1&\mathbf{a}\_2\cdot
  \mathbf{b}\_2&\cdots&\mathbf{a}\_2\cdot \mathbf{b}\_m\\\
\vdots&\vdots&\ddots&\vdots\\\
  \mathbf{a}\_m\cdot \mathbf{b}\_1&\mathbf{a}\_m\cdot
  \mathbf{b}\_2&\cdots&\mathbf{a}\_m\cdot \mathbf{b}\_m\\\
\end{vmatrix}
 \end{equation}
等于标架 $ (\mathbf{e}\_1',\mathbf{e}\_2',\cdots,\mathbf{e}\_m') $ 下 $ \mathbf{a}\_1',\mathbf{a}\_2',\cdots,\mathbf{a}\_m' $ 张成的有向平行体的$m$ 维有向体积(可正可负),再乘以同一个标架下 $ \mathbf{b}\_1,\mathbf{b}\_2,\cdots,\mathbf{b}\_m $ 张成的有向平行体的 $m$ 维有向体积 $ |\mathbf{b}\_1'||\mathbf{b}\_2'|\cdots |\mathbf{b}\_m'| $(为正).

我们规定,当行列式 \eqref{eq:2} 的值为正时,有向平行体 $A$ 和有向平行体 $B$ 的夹角为锐角;当行列式 \eqref{eq:2} 的值为负时,$A$ 和 $B$ 的夹角为钝角;当行列式 \eqref{eq:2} 的值为 $0$ 时,$A$ 和 $B$ 正交.

这样我们就完成了推广.

> 练习1(来自张禾瑞等编写《高等代数》第5版习题8.1.7):设 $\alpha\_1$,$\cdots$,$\alpha\_2$,$\alpha\_n$ 是欧式空间的 $n$ 个向量.行列式
$$
G(\alpha\_1,\cdots,\alpha\_n)=\begin{vmatrix}
  \mathbf{a}\_1\cdot \mathbf{a}\_1&\mathbf{a}\_1\cdot
  \mathbf{a}\_2&\cdots&\mathbf{a}\_1\cdot \mathbf{a}\_n\\\
  \mathbf{a}\_2\cdot \mathbf{a}\_1&\mathbf{a}\_2\cdot
  \mathbf{a}\_2&\cdots&\mathbf{a}\_2\cdot \mathbf{a}\_n\\\
\vdots&\vdots&\ddots&\vdots\\\
  \mathbf{a}\_n\cdot \mathbf{a}\_1&\mathbf{a}\_n\cdot
  \mathbf{a}\_2&\cdots&\mathbf{a}\_n\cdot \mathbf{a}\_n\\\
\end{vmatrix}
$$
> 叫做 $\alpha\_1,\cdots,\alpha\_n$ 的 Gram 行列式.证明 $G(\alpha\_1,\cdots,\alpha\_n)=0$ 当且仅当 $\alpha\_1,\cdots,\alpha\_n$ 线性相关.
