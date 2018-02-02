title: Bernoulli不等式
date: 2015-07-08 13:37:54
categories:
- 数学
- 不等式

tags:
- Bernoulli不等式

---
Bernoulli不等式如下:

**Bernoulli不等式:**$(1+a)^n\geq 1+na$,对于一切 $a\geq -1$以及$n\in \mathbf{N}$.

-----
该不等式的证明很简单,可以用数学归纳法.
**使用数学归纳法证明:**当$n=0$时,$1=1$,此时命题成立(规定$0^0=1$).假设当 $n=k(k\geq 0,k\in \mathbf{N})$时,不等式仍然成立,即
\begin{equation}
\label{eq:1.39}
(1+a)^k\geq 1+ka
\end{equation}
则
\begin{equation}
\label{eq:1.41}
(1+a)^{k+1}=(1+a)^k(1+a)\geq (1+ka)(1+a)=1+ka+a+ka^2\geq 1+(k+1)a
\end{equation}
即此时不等式对于$n=k+1$时也成立.因此由归纳法,对于一切自然数$n$,Bernoulli不等式都成立.

---
也可以用微分中值定理来证.
**使用微分中值定理证明:**当$n=0$时原不等式成立,因此我们只讨论$n\in \mathbf{N}^+$的情形.当$a=0$时原不等式显然成立.当$a>0$时,原不等式等价于
\begin{equation}\label{eq:1}
\frac{(1+a)^n-1^n}{a}\geq n
\end{equation}
由微分中值定理,\eqref{eq:1}等价于
$$
(\xi^n)'=n\xi^{n-1}\geq n,
$$
其中$\xi\in (1,1+a)$.也即证明$\xi^{n-1}\geq 1$.这对于任意$n\in\mathbf{N}^{+}$是显然成立的.当$a<0$时,原不等式等价于
\begin{equation}
  \label{eq:2}
  \frac{(1+a)^n-1^n}{a}\leq n.
\end{equation}
由微分中值定理,\eqref{eq:2}等价于
$$
(\xi^n)'=n\xi^{n-1}\leq n,
$$
其中$\xi\in (1+a,1)$.也即证明$\xi^{n-1}\leq 1$.这对于任意$n\in\mathbf{N}^{+}$是显然成立的.

-----
Bernoulli不等式有其现实意义.它无非就是说,利滚利赚得比较多.该现实意义可以看作其最自然的证明.
**Bernoulli不等式的利率解释:**假设你存$p$元钱于某银行.银行给你两种利率方案让你任选.第一种是利滚利方案,年利率为$a$.每年计算利息的时候,把以前给的利息算进本金.第二种不是利滚利方案,年利率也为$a$,但无论存了几年钱,在每年算利息的时候,本金始终是刚存进去的时候那笔钱.显然,任何一个正常人都会选择利滚利方案,因为这种方案让本金滚雪球式累积,这样每年算利息的时候,利息都比后一种方案多.实际上,利滚利方案经过$n$年后,本息和为$p(1+a)^n$,非利滚利方案经过$n$年后,本息和为$p+npa$.
$$
p(1+a)^n\geq p+npa\iff (1+a)^n\geq 1+na.
$$

----
**推论:**$$(1-a)^n<\frac{1}{1+na},$$其中$0<a<1$,$n=2,3,\cdots$

----
**证明:**
$$
(1-a)^n(1+a)^n=(1-a^2)^n<1 \iff (1-a)^n<\frac{1}{(1+a)^n}.
$$
由Bernoulli不等式,$(1+a)^n\geq 1+na$,因此
$$
(1-a)^n<\frac{1}{1+a)^n}\leq \frac{1}{1+na}.
$$

----
**习题:**分别用数学归纳法,微分中值定理,以及实际意义给出不等式
$$
1-na<(1-a)^n
$$
的证明,其中$0<a<1$,$n=2,3,\cdots$
