title: 用Stolz-Cesàro定理证明L'Hospital法则
date: 2015-11-29 10:05:48
categories:
- 数学
- 单元微积分

tags:
- Stolz-Cesàro定理
- L'Hospital法则

---
[Stolz定理](/2015/11/24/Stolz-Cesaro定理)与L'Hospital法则在形式上十分接近,只不过前者针对离散情形,后者针对连续情形.在这篇博文里,我要证明,由前者借助于可微函数的一些性质,可以推出后者.

 

下面是$\frac{\infty}{\infty}$型的洛必达法则:


>已知$\displaystyle\lim\_{x\to\infty}g(x)=\infty$,而且$\lim\_{n\to\infty}\frac {f'(x)}{g'(x)}=L$或者$\lim\_{n\to\infty}\frac {f'(x)}{g'(x)}$是无限.而且存在正实数$K$,当$a>K$时,都有$g'(a)\neq 0$而且保证$f(a)$与$g(a)$的可导,则$$\lim\_{x\to\infty}\frac{f(x)}{g(x)}=\lim\_{x\to\infty}\frac{f'(x)}{g'(x)}$$


**证明**：当$\lim\_{n\to\infty}\frac {f'(x)}{g'(x)}$有限时,在区间$(K,+\infty)$上取间隔为1的点:$x\_1< x\_2< x\_3< \cdots$,这些点对应的函数值分别为$f(x\_1),f(x\_2),\cdots$和$g(x\_1),g(x\_2),\cdots$,因为$\lim\_{n\to\infty}\frac{f'(x)}{g'(x)}=L$,即对于任意给定的正实数$\varepsilon$,都存在相应的正实数$M$,对于一切$x>M$都有\begin{equation}\label{eq:1}|\frac{f'(x)}{g'(x)}-L|<\varepsilon\end{equation}必定存在正整数$P$,使得$x\_P,x\_{P+1},x\_{P+2},\cdots$都大于$M$.


现在要证的是：对于任意一个大于或等于$P$的正整数$N$,都有\begin{equation}\label{eq:2}|\frac{f(x\_{N+1})-f(x\_N)}{g(x\_{N+1})-g(x\_N)}-L|<\varepsilon\end{equation}这是因为根据柯西中值定理,必定有$t\in(x\_N,x\_{N+1})$,使得$$\frac{f'(t)}{g'(t)}=\frac{f(x\_{N+1})-f(x\_N)}{g(x\_{N+1})-g(x\_N)}$$再结合\eqref{eq:1}得证\eqref{eq:2}.可见,$$\lim\_{n\to\infty}\frac{f(x\_{n+1})-f(x\_n)}{g(x\_{n+1})-g(x\_n)}=L$$.由于当$a>K$时,$g'(a)\neq 0$,且$g'(a)$可导,根据导函数的介值性(达布定理),$g'(a)$恒大于0或者恒小于0.那么我们很容易得出数列$g(x\_N),g(x\_{N+1}),\cdots$是单调的,而且$\lim\_{x\to\infty}g(x)=\infty$,那么我们现在就可以使用Stolz定理.由Stolz定理,$\lim\_{n\to\infty}\frac{f(x\_n)}{g(x\_n)}=L$.

 

其实证到这一步就可以推出$\lim\_{x\to\infty}\frac{f(x)}{g(x)}=L$了.因为我并没有规定$x\_1,x\_2,...$必须为整数,我只是规定它们的间隔必须为1而已,若存在给定的正实数$\Delta$,对于任意的正实数$K$都存在实数$m>K$,使得$|\frac{f(m)}{g(m)}-L|>\Delta$,那么我可以在距离$m$很近的地方设置一个$x\_i$,因为易证$\frac{f(x)}{g(x)}$在$x$很大的时候肯定是一个连续函数,那么$\frac{f(m)}{g(m)}$与$\frac{f(x\_i)}{g(x\_i)}$也会很近,可以达到想多近就有多近的程度.这就与$|\frac{f(m)}{g(m)}-L|>\Delta$矛盾.


**注**:$\frac{\infty}{\infty}$型的L'Hospital法则有鲜明的运动学意义.一个质点往无穷远方向运动,如果它的速度越来越趋于某个向量,则以原点为起始点,以质点位置为终点的向量与速度向量间的夹角也会趋于$0$.
