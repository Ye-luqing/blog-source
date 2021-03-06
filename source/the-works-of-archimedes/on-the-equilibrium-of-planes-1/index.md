﻿# 阿基米德《论平面图形的平衡1》命题6的证明
最近在读阿基米德的文章[《论平面图形的平衡1》](/the-works-of-archimedes/on-the-equilibrium-of-planes-1/论平面图形的平衡1.pdf).这篇文章的命题6如下：

>  可公度的两个量，当其距支点的距离与两量成反比时，处于平衡状态.

我向来不愿意一字一句地读别人写的证明，哪怕证明是阿基米德写的.因而我要对命题6给出自己的证明.

不妨设支点左边重物的量为$m$,支点右边重物的量为$n$,其中$m,n$都是正整数.则我们考察等距(设间距为$1$个单位长度)分步在一条直线上的$m+n$个重物，其中每个重物的量都是$1$.
![图1](/the-works-of-archimedes/on-the-equilibrium-of-planes-1/1.png)
则从左开始，以第$1$个点为起点，以第$m$个点为终点，可以形成一条线段$L\_1$.从右开始，以右边第$1$个点为起点，以右边第$n$个点为终点，可以形成另外一条线段$L\_2$.以左边第$1$个点为起点，以右边第$1$个点为终点，可以形成线段$L\_3$.线段$L\_1$的长度为$m-1$,线段$L\_2$的长度为$n-1$,线段$L\_{3}$的长度为$n+m-1$.

由文章命题$5$中的两个推论，左边$m$个点的质心$G\_m$位于线段$L\_1$的中点，右边$n$个点的质心$G\_n$位于线段$L\_2$的中点.所有点的重心$G\_{m+n}$位于线段$L\_3$的中点.

也即，若将支点放在点$G\_{m+n}$处，所有点都将保持平衡.由于左边$m$个点的质心位于$G\_m$,右边$n$个点的质心位于$G\_n$,因此把这$m+n$个点全部撤掉，转而在点$G\_m$处放一个量为$m$的重物，在点$G\_n$处放一个量为$n$的重物，把支点设在$G\_{m+n}$处，则这两个量分别为$m$和$n$的重物将仍保持平衡.

易得$|G\_mG\_{m+n}|:|G\_nG\_{m+n}|=\frac{n}{2}:\frac{m}{2}=n: m$.再结合文章中的公设5，就证明了命题6.

# 为什么三角形的重心必位于中线上
这篇文章的命题13如下：

>任何三角形的重心均在其任一顶点与其对边的中点的连线上.

阿基米德对此命题给出了两种证明方法，现在我给出我自己的证明方法.
![图2](/the-works-of-archimedes/on-the-equilibrium-of-planes-1/2.png)
如图，对于三角形$ABC$来说，分别取线段$AB,BC,CA$的中点$D,E,F$.由文章命题9，平行四边形$ADEF$的重心位于线段$DF$的中点$M$.为了证明三角形$ABC$的重心位于中线$AE$上，我们只用证明三角形$DBE$和三角形$FEC$联合组成的图形的重心位于直线$AE$上即可.

事实上，三角形$DBE$和三角形$FEC$是全等的，如果三角形$DBE$的重心是$I$且重心位于中线$DG$上，则三角形$FEC$的重心也会落在中线$FH$上，且设重心是$J$.点$I,J$会落在两个三角形的相似位置.那么三角形$DBE$和三角形$FEC$联合组成的图形的重心将位于线段$IJ$的中点$P$.易得点$P$也位于三角形$ABC$的中线$AE$上.这样，大三角形$ABC$的重心也会在$AE$上.

假设，如果三角形$DBE$的重心是$K$,且点$K$不在三角形$DBE$的中线$DG$上.则三角形$FEC$的重心$L$也不会在中线$FH$上，但是$K,L$仍然会位于两个三角形的相似位置.此时，三角形$DBE$和三角形$FEC$联合组成的图形的重心$N$会位于线段$KL$的中点，而大三角形$ABC$的重心会位于线段$MN$的中点$O$.由于三角形$ABC$与三角形$DBE$相似，因此三角形$ABC$的重心$O$和三角形$DBE$的重心$K$必定位于两个三角形的相似位置.于是，直线$DK$平行于直线$AO$.再由于直线$DK$平行于直线$MO$,因此直线$AO$与直线$MN$重合，即点$N$和点$P$一样，都位于三角形$ABC$的中线$AE$上，但是这显然与“点$K$不在三角形$DBE$的中线$DG$上”矛盾.因此假设不成立，即三角形$DBE$的重心$K$必位于$DBE$的中线$DG$上.证毕.