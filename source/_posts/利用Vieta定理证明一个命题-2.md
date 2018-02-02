title: 利用Vieta定理证明一个命题(2)
date: 2015-06-07 11:29:40
categories:
- 数学
- 多项式

tags:
- Vieta定理
- 叶立军《初等数学研究》

---
下面我们来做叶立军《初等数学研究》例2.3.4.不同于书上的解法(利用因式分解),我们使用Vieta定理来解决.

**题目**:设三个数$a,b,c$满足
\begin{equation}\label{eq:1}
\frac{1}{a}+\frac{1}{b}+\frac{1}{c}=\frac{1}{a+b+c},
\end{equation}
证明
$$
\frac{1}{a^{2n+1}}+\frac{1}{b^{2n+1}}+\frac{1}{c^{2n+1}}=\frac{1}{(a+b+c)^{2n+1}}.
$$

-----
**证明**:由等式\eqref{eq:1}可得
\begin{equation}\label{eq:2}
(ab+bc+ca)(a+b+c)=abc.
\end{equation}
构造三次函数
$$
f(x)=(x-a)(x-b)(x-c)=x^3-(a+b+c)x^2+(ab+bc+ca)x-abc=x^3+t\_2x^2+t\_1x+t\_0.
$$
由等式\eqref{eq:2}可得$t\_0=t\_1t\_2$.因此
\begin{align\*}
  f(x)&=x^3+t\_2x^2+t\_1x+t\_1t\_2
    \\\&=(x^2+t\_1)(x+t\_2)
    \\\&=(x-\sqrt{-t\_1})(x+\sqrt{-t\_1})(x+t\_2).
\end{align\*}
因此不妨设$a=-b$.因此
$$
\frac{1}{a^{2n+1}}+\frac{1}{b^{2n+1}}+\frac{1}{c^{2n+1}}=\frac{1}{c^{2n+1}}=\frac{1}{(a+b+c)^{2n+1}}.
$$
