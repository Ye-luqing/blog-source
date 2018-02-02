title: 与三角函数Taylor展开有关的一个不等式
date: 2015-08-24 22:26:38
categories:
- 数学
- 单元微积分
tags:
- Taylor展开
- 三角函数

---
我提出了一个猜想,现证明之.

**猜想:**设$f(x)=x-\frac{x^3}{3!}+\frac{x^5}{5!}-\frac{x^7}{7!}+\cdots+(-1)^{n}\frac{x^{2n+1}}{(2n+1)!}$,其中$n$为任意给定的自然数.当$0\leq a< b\leq 2n+3$时,有
\begin{equation}
  \label{eq:1}
  |\sin(a)-f(a)|<|\sin(b)-f(b)|.
\end{equation}

----
我们先把该猜想分解,来做它的一个子命题.

-----
**猜想1.1**:设$f(x)=x-\frac{x^3}{3!}+\frac{x^5}{5!}-\frac{x^7}{7!}+\cdots+(-1)^{n}\frac{x^{2n+1}}{(2n+1)!}$,其中自然数$n$为任意给定的奇数.当$0\leq a< b\leq 2n+3$时,有
\begin{equation}
  \label{eq:2}
  |\sin(a)-f(a)|<|\sin(b)-f(b)|.
\end{equation}

-----
为了证明猜想1.1,我们先叙述如下引理.该引理可以用翘翘板数学归纳法证明.

**引理:**设
$$
f(x)=x-\frac{x^3}{3!}+\frac{x^5}{5!}-\frac{x^7}{7!}+\cdots+(-1)^{n}\frac{x^{2n+1}}{(2n+1)!},
$$
$$
g(x)=1-\frac{x^2}{2!}+\frac{x^4}{4!}-\frac{x^6}{6!}+\cdots+(-1)^n \frac{x^{2n}}{(2n)!}.
$$
其中$n$为任意给定的自然数.则当$n$为偶数时,$f(x)\geq\sin x$,$g(x)\geq\cos x$;当$n$为奇数时,$f(x)\leq\sin x$,$g(x)\leq\cos x$.且等号当且仅当$x=0$时成立.

----
**猜想1.1证明:**由引理,可以将欲证的不等式\eqref{eq:2}化为
\begin{equation}
  \label{eq:3}
  \sin a-f(a)<\sin b-f(b).
\end{equation}
根据正弦函数的Taylor展开,为了证明不等式\eqref{eq:3},我们只用证明
\begin{equation}
  \label{eq:4}
p(x)=\frac{x^{2n+3}}{(2n+3)!}-\frac{x^{2n+5}}{(2n+5)!}+\frac{x^{2n+7}}{(2n+7)!}-\frac{x^{2n+9}}{(2n+9)!}+\cdots
\end{equation}
在$[0,2n+3]$上单调递增即可.由于$p(0)=0$,因此为了证明\eqref{eq:4}在$[0,2n+3]$上单调递增,在我们只用证明
\begin{equation}\label{eq:4.1}
p'(x)=\frac{x^{2n+2}}{(2n+2)!}-\frac{x^{2n+4}}{(2n+4)!}+\frac{x^{2n+6}}{(2n+6)!}-\frac{x^{2n+8}}{(2n+8)!}+\cdots
\end{equation}
在$[0,2n+3]$上大于$0$即可,而这是容易验证的,因为当$x\in [0,2n+3]$时,
$$
\frac{x^{2n+2}}{(2n+2)!}-\frac{x^{2n+4}}{(2n+4)!}>0,\frac{x^{2n+6}}{(2n+6)!}-\frac{x^{2n+8}}{(2n+8)!}>0,\cdots,\frac{x^{2n+k}}{(2n+k)!}-\frac{x^{2n+(k+2)}}{(2n+k+2)!}>0,\cdots
$$


这样我们就证明了猜想1.1.

---------
下面我们来做猜想的另外一个子命题.
**猜想1.2:**设$f(x)=x-\frac{x^3}{3!}+\frac{x^5}{5!}-\frac{x^7}{7!}+\cdots+(-1)^{n}\frac{x^{2n+1}}{(2n+1)!}$,其中自然数$n$为任意给定的偶数.当$0\leq a< b\leq 2n+3$时,有
\begin{equation}
  \label{eq:5}
  |\sin(a)-f(a)|<|\sin(b)-f(b)|.
\end{equation}

-----
**猜想1.2证明:**由引理,当$n$为偶数时,式\eqref{eq:5}等价于
\begin{equation}\label{eq:6}
\sin a-f(a)>\sin b-f(b).
\end{equation}
根据正弦函数的Taylor展开,式\eqref{eq:6}等价于
$$
p(x)=\frac{x^{2n+3}}{(2n+3)!}-\frac{x^{2n+5}}{(2n+5)!}+\frac{x^{2n+7}}{(2n+7)!}-\frac{x^{2n+9}}{(2n+9)!}+\cdots
$$
在$[0,2n+3]$上单调递增.这是我们已经在猜想1.1中证明过了的.

将猜想1.1与猜想1.2合并,我们就证明了猜想.

----
网名为元始天尊的哆嗒数学群(QQ 128709478)网友(QQ 94136048)说我的猜想应该能推广成更完美的形式.

**猜想推广:**设$f(x)=x-\frac{x^3}{3!}+\frac{x^5}{5!}-\frac{x^7}{7!}+\cdots+(-1)^{n}\frac{x^{2n+1}}{(2n+1)!}$,其中$n$为任意给定的自然数.当$0\leq a< b$时,有
\begin{equation}
  \label{eq:7}
  |\sin(a)-f(a)|<|\sin(b)-f(b)|.
\end{equation}  

---
**猜想推广之证明纲要:**照样把$n$分奇偶性来分类讨论.当$n$为偶数时,欲证的式\eqref{eq:7}可以化为
$$
\sin a-f(a)>\sin b-f(b).
$$
当$n$为奇数时,欲证的式\eqref{eq:7}可以化为
$$
\sin a-f(a)<\sin b-f(b).
$$
无论是哪种情况,最终我们都只需要证明
$$
p(x)=\frac{x^{2n+3}}{(2n+3)!}-\frac{x^{2n+5}}{(2n+5)!}+\frac{x^{2n+7}}{(2n+7)!}-\frac{x^{2n+9}}{(2n+9)!}+\cdots
$$
在$[0,+\infty)$上单调递增即可.由于$p(0)=0$,于是只用证明
$$
p'(x)=\frac{x^{2n+2}}{(2n+2)!}-\frac{x^{2n+4}}{(2n+4)!}+\frac{x^{2n+6}}{(2n+6)!}-\frac{x^{2n+8}}{(2n+8)!}+\cdots
$$
在$(0,+\infty)$上恒大于$0$即可.这根据引理是能证明的,这是因为当$n$是奇数时,
$$
p'(x)=\cos x-g(x)>0,
$$
当$n$是偶数时,
$$
p'(x)=g(x)-\cos x>0.
$$
![](/img/与三角函数Taylor展开有关的一个不等式-1.png)
