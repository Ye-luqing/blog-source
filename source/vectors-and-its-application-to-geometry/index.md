本页面收录上海教育出版社出版的上海市中小学拓展型课程教材《平面向量与几何》的习题解答以及感悟.

# 练习2-2(3),第2题：一道简单的三点共线题

>已知：如图，四边形$ABCD$是平行四边形，点$E,F,G,H$分别在边$AB,BC,CD,DA$上，$EF\parallel HG$,$EG$与$HF$相交于点$Q$.求证：$B,Q,D$三点共线.

![图1](/vectors-and-its-application-to-geometry/1.png)

**证明**:因为$HG\parallel FE$,所以$\frac{HQ}{FQ}=\frac{HG}{FE}$.又易得$\frac{HG}{FE}=\frac{HD}{FB}$,所以$\frac{HQ}{FQ}=\frac{HD}{FB}$.这表明三角形$HDQ$以$Q$为旋转中心，顺时针旋转$180^{\circ}$,再放大$\frac{QF}{QH}$倍，得到三角形$FBQ$.因此$B,Q,D$三点共线.

# 练习2-2(7),第1题：三角形内心的向量表达式
> 已知：如图，$\triangle ABC$的三边长为$BC=a,AC=b,AB=c$,点$I$是它的内心,$O$是$\triangle ABC$外任意一点.利用三角形的角平分线定理，证明：
$$
\overrightarrow{OI}=\frac{1}{a+b+c}(a\overrightarrow{OA}+b\overrightarrow{OB}+c\overrightarrow{OC}).
$$
![图2](/vectors-and-its-application-to-geometry/2.png)
**证明**:由三角形的角平分线定理，$\frac{BD}{DC}=\frac{AB}{AC}=\frac{c}{b}$,因此$BD=\frac{ac}{b+c}$,$DC=\frac{ab}{b+c}$.因此,由三角形的角平分线定理,$\frac{DI}{IA}=\frac{BD}{BA}=\frac{a}{b+c}$.因此
$$
  \overrightarrow{AI}=\frac{b+c}{a+b+c}\overrightarrow{AD}=\frac{b+c}{a+b+c}\left(\frac{b}{b+c}\overrightarrow{AB}+\frac{c}{b+c}\overrightarrow{AC}\right)=\frac{b}{a+b+c}\overrightarrow{AB}+\frac{c}{a+b+c}\overrightarrow{AC},
$$
即
$$
\overrightarrow{OI}-\overrightarrow{OA}=\frac{b}{a+b+c}\left(\overrightarrow{OB}-\overrightarrow{OA}\right)+\frac{c}{a+b+c}\left(\overrightarrow{OC}-\overrightarrow{OA}\right),
$$
整理可得
$$
\overrightarrow{OI}=\frac{a}{a+b+c}\overrightarrow{OA}+\frac{b}{a+b+c}\overrightarrow{OB}+\frac{c}{a+b+c}\overrightarrow{OC}.
$$