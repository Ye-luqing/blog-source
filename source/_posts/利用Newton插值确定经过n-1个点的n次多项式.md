title: 利用Newton插值确定经过n+1个点的n次多项式
date: 2015-10-30 14:59:04
categories:
- 数学
- 单元微积分
tags:
- Newton插值
- Taylor公式

---
设一个 $n(n\geq 0)$ 次多项式通过平面直角坐标系上 $n+1$ 个已知点
$$(x\_{0},f(x\_0)),\cdots,(x\_{n},f(x\_n)).$$
而且满足 $x\_0< x\_1< \cdots< x\_n$.下面我们通过待定系数法,利用Newton插值来求通过这 $n+1$ 个点的多项式的表达式,在最后,我们来说明这样的多项式是唯一的.先考虑$n=1,2,3$的特殊情形.
# $n=1$ 时
此时,通过两个点 $(x\_0,f(x\_0)),(x\_1,f(x\_1))$的是一次函数
$$g=f(x\_0)+\frac{f(x\_0)-f(x\_1)}{x\_0-x\_1}(x-x\_0).$$
记 $\frac{f(x\_0)-f(x\_1)}{x\_0-x\_1}:=f[x\_0,x\_1]$.则一次函数化为$$u(x)=f(x\_0)+f[x\_0,x\_1] (x-x\_0).$$
# $n=2$ 时
此时,通过三个点 $(x\_0,f(x\_0)),(x\_1,f(x\_1)),(x\_2,f(x\_2))$ 的二次多项式函数设为
$$u(x)=f(x\_0)+f[x\_0,x\_1] (x-x\_0)+p(x-x\_0)(x-x\_1),$$
其中 $p$ 是一个常数.易得$u(x\_0)=f(x\_0),u(x\_1)=f(x\_1)$,然后令$u(x\_2)=f(x\_2)$,即
$$f[x\_0,x\_2]=f[x\_0,x\_1]+p(x\_2-x\_1),$$
因此便确定了
$$p=\frac{f[x\_0,x\_2]-f[x\_0,x\_1]}{x\_2-x\_1}.$$
将其记为 $f[x\_0,x\_1,x\_2]$.这样,二次多项式就成了
$$u(x)=f(x\_0)+f[x\_0,x\_1] (x-x\_0)+f[x\_0,x\_1,x\_2] (x-x\_0)(x-x\_1).$$
# $n=3$时
此时,通过四个点 $(x\_0,f(x\_0)),(x\_1,f(x\_1)),(x\_2,f(x\_2)),(x\_3,f(x\_3))$的三次多项式函数设为
$$u(x)=f(x\_0)+f[x\_0,x\_1] (x-x\_0)+f[x\_0,x\_1,x\_2] (x-x\_0)(x-x\_1)+p(x-x\_0)(x-x\_1)(x-x\_2).$$
其中 $p$ 是一个常数.易得$u(x\_0)=f(x\_0),u(x\_1)=f(x\_1),u(x\_2)=f(x\_2)$.现在使得 $u(x\_3)=f(x\_3)$,即
$$f(x\_3)=f[x\_0,x\_1] (x\_3-x\_0)+f(x\_0)+f[x\_0,x\_1,x\_2] (x\_3-x\_0)(x\_3-x\_1)+p(x\_3-x\_0)(x\_3-x\_1)(x\_3-x\_2).$$
可见,
$$p=\frac{f[x\_0,x\_1,x\_3]-f[x\_0,x\_1,x\_2]}{x\_3-x\_2}.$$
将其记为 $f[x\_0,x\_1,x\_{2},x\_3]$.这样,三次多项式就成了
$$u(x)=f(x\_0)+f[x\_0,x\_1] (x-x\_0)+f[x\_0,x\_1,x\_2] (x-x\_0)(x-x\_1)+f[x\_0,x\_1,x\_2,x\_3] (x-x\_0)(x-x\_1)(x-x\_2).$$
# 一般情形
有了上面三个特例作为启发,一般地,通过递推,我们能归纳出,通过 $n+1$ 个点$(x\_0,f(x\_0)),(x\_1,f(x\_1)),\cdots,(x\_n,f(x\_n))$ 的多项式为
$$u(x)=f(x\_0)+f[x\_0,x\_1] (x-x\_0)+\cdots+f[x\_0,x\_1,\cdots,x\_n] (x-x\_0)(x-x\_1)\cdots(x-x\_{n-1}),$$
其中 $\forall k\geq 0$,
$$\frac{f[x\_0,x\_1,\cdots,x\_{k},
  x\_{k+2}]-f[x\_0,x\_1,\cdots,x\_k,x\_{k+1}]}{x\_{k+2}-x\_{k+1}}:=f[x\_0,x\_1,\cdots,x\_{k+2}].$$
# 唯一性说明
易得 $n$ 个多项式
$$1,x-x\_0,(x-x\_0)(x-x\_1),\cdots,(x-x\_0)(x-x\_1)\cdots (x-x\_{n-1})$$
是线性无关的,因此能作为 $n$ 维线性空间 $\mathcal{P}\_{n-1}$ 的一组基,其中 $\mathcal{P}\_{n-1}$ 是所有次数不超过 $n-1$ 的多项式的集合.而线性空间中的每个向量被基中的向量进行线性表示时,基中的各个向量前的系数是唯一的.这样就证明了通过点 $(x\_0,f(x\_0)),\cdots,(x\_{n-1},f(x\_{n-1}))$ 的多项式的唯一性.

# Newton插值的一个特殊情形
令$n+1$个点为$(0,f(0)),(1,f(1)),\cdots,(n,f(n))$.则经过这$n+1$个点的$n$次多项式为
$$
  f(0)+f[0,1] (x-0)+\cdots+f[0,1,\cdots,n] (x-0)(x-1)\cdots(x-(n-1)).
$$
# 从Newton插值到带Lagrange余项的Taylor公式
已知$x\_0< x\_1< \cdots< x\_n$.设函数$g(x)$在$(x\_0,x\_n)$上有$n+1$阶导数且在$[x\_0,x\_n]$上$n$阶导数连续.且函数$g(x)$通过点$(x\_0,g(x\_0)),(x\_1,g(x\_1)),\cdots,(x\_n,g(x\_n))$.则经过这$n+1$个点的$n$次多项式为
\begin{equation}\label{eq:1}
p(x)=g(x\_0)+g[x\_0,x\_1] (x-x\_0)+\cdots+g[x\_0,x\_1,\cdots,x\_n] (x-x\_0)(x-x\_1)\cdots(x-x\_{n-1}).
\end{equation}
我们给这个$n$次多项式再添加一个余项$R\_n(x)$,使得
$$
g(x)=p(x)+R\_n(x).
$$
其中余项 $R\_n(x)$就是
$$
g[x\_0,x\_1,\cdots,x\_n,x] (x-x\_0)(x-x\_1)\cdots (x-x\_{n-1})(x-x\_n).
$$
然后我们来看函数$R\_n(x)=g(x)-p(x)$.易得
$$
R\_{n}(x\_0)=R\_{n}(x\_1)=\cdots=R\_{n}(x\_n)=0,
$$
且 $R\_{n}(x)$拥有$n$阶导数,$n$阶导数连续.由于$R\_{n}(x\_0)=R\_{n}(x\_1)$,因此根据Rolle定理,存在$\varepsilon\_{1,1}\in (x\_0,x\_1)$,使得$R\_{n}'(\varepsilon\_{1,1})=0$,同理,$\forall 1\leq i\leq n$,存在$\varepsilon\_{1,i}\in (x\_{i-1},x\_i)$,使得 $R\_{n}'(\varepsilon\_{1,i})=0$.这样,我们就有$$R\_{n}'(\varepsilon\_{1,1})=R\_{n}'(\varepsilon\_{1,2})=\cdots=R\_{n}'(\varepsilon\_{1,n})=0.$$再次使用Rolle定理,可得
$$
R\_{n}'(\varepsilon\_{2,1})=\cdots=R\_{n}'(\varepsilon\_{2,n-1})=0,
$$
其中 $\varepsilon\_{2,1}\in (\varepsilon \_{1,1},\varepsilon\_{1,2}),\cdots,\varepsilon\_{2,n-1}\in (\varepsilon\_{1,n-1},\varepsilon\_{1,n})$.不断地使用Rolle定理,最终使用Rolle定理$n$次,可得$R\_{n}^{(n)}(\varepsilon\_{n,1})=0$,也即
$$
g^{(n)}(\varepsilon\_{n,1})=n!g[x\_0,x\_1,\cdots,x\_n].
$$
同理,存在$\delta\_{n+1}(x)$,使得$g^{(n+1)}(\delta\_{n+1}(x))=(n+1)!g[x\_0,x\_1,\cdots,x\_n,x]$(多亏了函数$g(x)$是$n+1$阶可导函数),其中$\delta\_{n+1}(x)\in (\min\{x\_0,x\_1,\cdots,x\_n,x\},\max\{x\_0,x\_1,\cdots,x\_n,x\})$.而且存在$\delta\_1\in (x\_0,x\_1)$,使得
$$
g'(\delta\_1)=g[x\_0,x\_1].
$$
$$
\vdots
$$
存在$\delta\_n\in (x\_1,x\_n)$,使得
$$
g^{(n)}(\delta\_n)=n!g[x\_0,x\_1,\cdots,x\_n],
$$
这样,多项式\eqref{eq:1}就会变为
\begin{equation}\label{eq:2}
  g(x\_0)+g'(\delta\_1)(x-x\_0)+\cdots+\frac{1}{n!}g^{(n)}(\delta\_n)(x-x\_0)(x-x\_1)\cdots
  (x-x\_{n-1})
\end{equation}
再加上余项
$\frac{1}{(n+1)!}g^{(n+1)}(\delta\_{n+1}(x))(x-x\_0)(x-x\_1)\cdots (x-x\_{n-1})(x-x\_n)$,就得到
$$
g(x)=  g(x\_0)+g'(\delta\_1)(x-x\_0)+\cdots+\frac{1}{n!}g^{(n)}(\delta\_n)(x-x\_0)(x-x\_1)\cdots
  (x-x\_{n-1})+\frac{1}{(n+1)!}g^{(n+1)}(\delta\_{n+1}(x))(x-x\_0)(x-x\_1)\cdots
  (x-x\_{n-1})(x-x\_n).
$$
特别地,如果$x\_0\to a,x\_1\to a,\cdots,x\_n\to a$,则 $g(x)$ 趋于
\begin{equation}
\label{eq:3}
g(x)=g(x\_0)+g'(a)(x-a)+\cdots+\frac{1}{n!}g^{(n)}(a)(x-a)^{n}+\frac{1}{(n+1)!}g^{(n+1)}(\delta)(x-a)^{n+1}.
\end{equation}
其中$\delta\in (a,x)$或$(x,a)$.注意这里用到了条件“$g(x)$在$[x\_0,x\_n]$上$n$阶导函数连续”.
