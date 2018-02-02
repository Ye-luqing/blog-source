title: "$1/(1+x^2)$的Taylor展开"
date: 2015-04-04 23:23:21
categories:
- 数学
- 单元微积分
tags:
- Taylor展开
- 《复分析——可视化方法》
---
在此,我们试图对函数
$$
H(x)=\frac{1}{1+x^2}
$$
在$x=k$处进行Taylor展开.这是[《复分析——可视化方法》](http://www.amazon.cn/%E5%A4%8D%E5%88%86%E6%9E%90-%E5%8F%AF%E8%A7%86%E5%8C%96%E6%96%B9%E6%B3%95-Tristan-Needham/dp/B002DW9ZTU)上的习题2.9.9.如果使用了复数,Taylor展开是简单的.具体如下.
>**使用复数解决:**因为$$\frac{1}{1+x^2}=\frac{1}{(1+ix)(1-ix)}=\frac{1}{2}(\frac{1}{1-ix}+\frac{1}{1+ix}),$$而$$\frac{1}{1-ix}=\frac{1}{1-ik}+\frac{i}{(1-ik)^2}(x-k)+\frac{i^2}{(1-ik)^3}(x-k)^2+\frac{i^3}{(1-ik)^4}(x-k)^{3}+\cdots+\frac{i^n}{(1-ik)^{n+1}}(x-k)^n+\cdots$$且$$\frac{1}{1+ix}=\frac{1}{1+ik}+\frac{-i}{(1+ik)^2}(x-k)+\frac{(-i)^{2}}{(1+ik)^3}(x-k)^2-\frac{(-i)^{3}}{(1+ik)^4}(x-k)^3+\frac{(-i)^{n}}{(1+ik)^{n+1}}(x-k)^n+\cdots$$因此可得$$\frac{1}{1+x^2}=\frac{1}{1+k^2}-\frac{2k}{(1+k^2)^2}(x-k)+\cdots+\frac{i^n(1+ik)^{n+1}+(-i)^n(1-ik)^{n+1}}{(1+k^2)^{n+1}}(x-k)^n+\cdots$$我们发现,$i^n(1+ik)^{n+1}$和$(-i)^n(1-ik)^{n+1}$是共轭复数,因此$\frac{i^n(1+ik)^{n+1}+(-i)^n(1-ik)^{n+1}}{(1+k^2)^{n+1}}$肯定是实数.这样我们就得到了$H(x)$在$x=k$处的Taylor展开式.

可以想见,如果仅仅在实数范围内对$H(x)$在$x=k$处Taylor展开,计算过程将异常麻烦.
