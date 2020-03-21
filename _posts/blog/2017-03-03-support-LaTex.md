---
layout: post
title: 增加LaTeX支持 
category: blog
description: I'm angry!
---

用了大半天的时间让本站支持LaTeX数学公式。<br/>
一开始就决定了采用Jekyll官方推荐的方法：MathJax。按说很容易，在html中加一行引用它的代码，然后在文章中使用相应记号标示出LaTeX语法块，它就会将其处理成好看的公式了；但由于我是用Markdown写好文章，然后让Jekyll调用编辑器将其转化为html，这一过程往往会破坏掉为MathJax所留的标识符。

当时我并没去弄清楚整个执行过程，而是忙着找能与MathJax兼容的Markdown编辑器。<br/>
于是找到了Kramdown，它官方声称支持MathJax。兴冲冲拿来一试，结果不能满意。主要问题是：
* Kramdown的文档中声称\'\\$\\$\'是独行居中公式的标示符，但实际上是行内的；
* MathJax的默认符号含有\'\\\'，会被Kramdown预先处理。需要同时考虑两个软件的符号，很烦。
* 我想要尽量使用跟LaTeX中一样的记号。

翻来覆去弄了半天，最终觉得，改变MathJax的tex2jax识别符号，自然地让Kramdown不会对数学部分作任何处理是最省心的方案。

***
ANGRY！被官方文档坑走了几个小时。<br/>
以后一定要记得，还是自己最可靠，搞清问题的内在逻辑比问谁都有用。
