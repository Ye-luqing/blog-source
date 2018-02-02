title: "Hexo之Reference Error: match is not defined解决方案"
date: 2015-03-10 22:17:50
categories:
- 计算机
- Hexo
tags:
- Hexo
---
我这个博客是使用Hexo架设在Github上的.今晚当我使用

```
hexo g
```
的时候,Hexo突然发癫,显示如下信息:
```
[error] HexoError: Process failed: _posts/混合偏导数的Clairaut定理.md
ReferenceError: match is not defined
    at Object.<anonymous> (/usr/local/lib/node_modules/hexo/lib/plugins/filter/external_link.js:25:46)
    at exports.each (/usr/local/lib/node_modules/hexo/node_modules/cheerio/lib/api/traversing.js:268:24)
    at module.exports (/usr/local/lib/node_modules/hexo/lib/plugins/filter/external_link.js:11:10)
    at /usr/local/lib/node_modules/hexo/lib/post/render.js:112:11
    at iterate (/usr/local/lib/node_modules/hexo/node_modules/async/lib/async.js:149:13)
    at Object.async.eachSeries (/usr/local/lib/node_modules/hexo/node_modules/async/lib/async.js:165:9)
    at /usr/local/lib/node_modules/hexo/lib/post/render.js:111:15
    at /usr/local/lib/node_modules/hexo/lib/extend/renderer.js:78:20
    at b (domain.js:183:18)
    at Domain.run (domain.js:123:23)

```
Google许久不能找到解决方案.最后通过排除法不断实验终于确定是博文 [混合偏导数的Clairaut定理](/2015/02/23/混合偏导数的Clairaut定理/)里的链接问题.当链接到我自己的网站 blogmath.org 里的内容的时候,`http://blogmath.org/` 不能出现.比如要链接到 [平面转动系统中质点的运动](/2015/03/03/平面转动系统中质点的运动) ,不能写
```
[平面转动系统中质点的运动](http://blogmath.org/2015/03/03/平面转动系统中质点的运动)
```
而要写
```
[平面转动系统中质点的运动](/2015/03/03/平面转动系统中质点的运动)
```

这真奇怪,我以前编译博文的时候都没出现这样的问题的,为何今晚偏偏出现了.深层的机制我不想探究也没精力探究,问题解决了就好.不过稍微想一下可以知道,显然把链接写为 `/2015/03/03/平面转动系统中质点的运动` 更好,因为这有利于以后博客域名的改变.




