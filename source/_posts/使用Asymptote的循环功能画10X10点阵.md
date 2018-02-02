title: 使用Asymptote的循环功能画$10\times 10$点阵
date: 2015-03-30 15:44:27
categories:
- 计算机
- Asymptote
tags:
- Asymptote
- 画图
---
[Asymptote](http://en.wikipedia.org/wiki/Asymptote_%28vector_graphics_language%29)是一个强大的可编程的画图软件.在这里,我们使用Asymptote的循环功能画一个$10\times 10$的点阵.代码如下.把如下代码放在一个 asy 文件中,然后编译.可以得到一个eps文件.效果如图1所示(不过图1是png格式的).

```
size(5cm,5cm);
for (int x=-5;x<5;++x)//不能写为 x++
  {
   for (int y=-5;y<5;++y)
      {
	   dot((x,y));//不能写为 dot(x,y)
      }
  }

```
![图1](/img/使用Asymptote的循环功能画10X10点阵-1.png) 



