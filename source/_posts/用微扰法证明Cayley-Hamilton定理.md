title: 用微扰法证明Cayley-Hamilton定理
date: 2015-05-20 03:01:22
categories:
- 数学
- 线性代数
tags:
- Cayley-Hamilton定理

---
在此我们使用数学分析的方法证明Cayley-Hamilton定理.

设$V$是$\mathbf{C}$上的一个$m(m\geq 1)$维线性空间.$T$是$V$上的线性算子.设$\alpha$是$V$里的一组有序基,线性算子$T$在$\alpha$下的矩阵为$[T]\_{\alpha}^{\alpha}$.下面我们来看关于$[T]\_{\alpha}^{\alpha}$的多项式
$$
P([T]\_{\alpha}^{\alpha})=a\_n([T]\_{\alpha}^{\alpha})^n+\cdots+a\_1[T]\_{\alpha}^{\alpha}+a\_0I,
$$
其中$a\_n,\cdots,a\_0\in \mathbf{C}$.如果$[T]\_{\alpha}^{\alpha}$是可对角化矩阵,则存在$V$的一组基$\beta$,使得$[T]\_{\beta}^{\beta}$是对角阵,且
$$
[T]\_{\alpha}^{\alpha}=[I]\_{\beta}^{\alpha}[T]\_{\beta}^{\beta}[I]\_{\alpha}^{\beta},
$$
于是,
$$
P([T]\_{\alpha}^{\alpha})=P([I]\_{\beta}^{\alpha}[T]\_{\beta}^{\beta}[I]\_{\alpha}^{\beta})=[I]\_{\beta}^{\alpha}P([T]\_{\beta}^{\beta})[I]\_{\alpha}^{\beta}.
$$
由于$[T]\_{\beta}^{\beta}$是对角阵,因此$P([T]\_{\beta}^{\beta})$的计算会变得特别容易,详细地说,此时,关于矩阵$[T]\_{\beta}^{\beta}$的多项式$P([T]\_{\beta}^{\beta})$已经变成了关于$[T]\_{\beta}^{\beta}$的所有的特征值的一组同样的多项式.由于对角阵$[T]\_{\beta}^{\beta}$的对角线上的每个数都是$T$的特征值,因此特别地,如果$P$是关于线性映射$T$的特征多项式,那么$P([T]\_{\beta}^{\beta})=\mathbf{0}$,于是,
$$
P([T]\_{\alpha}^{\alpha})=P([I]\_{\beta}^{\alpha}[T]\_{\beta}^{\beta}[I]\_{\alpha}^{\beta})=[I]\_{\beta}^{\alpha}P([T]\_{\beta}^{\beta})[I]\_{\alpha}^{\beta}=\mathbf{0}.
$$
这就是关于对角阵的Cayley-Hamilton定理.


当$[T]\_{\alpha}^{\alpha}$不是可对角化矩阵,那么$[T]\_{\alpha}^{\alpha}$不再可对角化,但是[可上三角化](/2015/05/20/复数域上的方阵必相似于上三角阵).也就是说,存在$V$的一组基$\gamma$,使得$[T]\_{\gamma}^{\gamma}$是一个上三角矩阵,该上三角矩阵对角线上的元素都是$T$的特征值.然后,设上三角矩阵$[T]\_{\gamma}^{\gamma}$的对角线的第$1,2,\cdots,m$行的特征值分别为$\lambda\_1,\lambda\_2,\cdots,\lambda\_m$.对上三角矩阵$[T]\_{\gamma}^{\gamma}$的对角线进行微扰,使得其对角线上的元素的第$1,2,\cdots,m$行分别变为$\lambda\_1+\varepsilon\_1,\lambda\_2+\varepsilon\_2,\cdots,\lambda\_m+\varepsilon\_m$.这样上三角矩阵$[T]\_{\gamma}^{\gamma}$就变成了另一个上三角矩阵$[T']\_{\gamma}^{\gamma}$.通过恰当地选取$\varepsilon\_1,\varepsilon\_2,\cdots,\varepsilon\_m$,能使的$[T']\_{\gamma}^{\gamma}$的对角线上的元素互不相同.这样线性算子$T'$就成了一个可对角化线性变换.因此,对于$T'$的特征多项式$P'$来说,$P([T']\_{\tau}^{\tau})=\mathbf{0}$,其中$[T']\_{\tau}^{\tau}$是$T'$关于$V$的任意一组基$\tau$的矩阵.令$\varepsilon\_1,\varepsilon\_2,\cdots,\varepsilon\_m$趋于$0$的同时,保持$T'$的可对角化性不变,此时,$T'$的特征多项式$P'$会趋于$T$的特征多项式$P$,$T'$会趋于$T$.于是,即便当$T$不是可对角化的矩阵,Cayley-Hamilton定理对于$T$依然是成立的.
