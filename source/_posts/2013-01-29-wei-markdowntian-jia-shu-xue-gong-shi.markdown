---
layout: post
title: "为Markdown添加数学公式"
date: 2013-01-29 14:49
comments: true
categories: [Markdown, 技术]
---

如何在`Markdown`语言中加入数学公式。这个问题是我这两天一直在考虑的。通过`Google`搜索，以及自己分析研究。我确定了以下四个解决方案。他们都可以完美支持中文和数学公式。其中第四个方案，我个人认为是最方便的。

下面说说我的初衷吧。我是一个狂热的`Markdown`拥趸。同时也是`nvALT`的重度使用者。我希望我所有的文章都可以存储在`nvALT`里面。前一阵子刚刚解决了`nvALT`加入图片的问题。现在突发奇想是不是也应该实现数学公式的问题？虽然目前没有需求，但是可以为过一段开始的研究生生活做一些技术储备嘛！呵呵。

**NOTE!** 看起来博客现实数学公式的功能还没实现…T T

## 方案1 没问题=)

第一个方案是通过`pandoc`这款程序来实现的。通过对于md的超集来解决。

只需要在`markdown`文件中加入tex公式即可。
`$\sum_i=a_i$` 就可以编译出来。在终端中使用如下代码。

	pandoc thisfile.md -o anyName.pdf
		
就出来结果了。

但是因为`latex`的一些原因，不支持中文 T T

~~需要先编译成tex文件，然后进行一些修改，才能编译中文。（中文还没有办法）~~

	pandoc -s thisfile.md -o anyName.tex
	修改一些参数
	xelatex anyName.tex -o anyName.pdf

~~就可以了。~~

因为本人`latex`造诣有限，目前还没有找到解决方案。。。T T

**Pandoc最好的选择是转换成HTML格式。可以完美支持中文，同时可以很好的显示数学代码。不过从使用的角度来说还是Marked的效果最好。**

## 方案2 支持中文

	<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=default"></script>

看到没在上面添加这个脚本链接就可以了。这回支持中文了。：）

	(E=mc^2)，$$x_{1,2} = \frac{-b \pm \sqrt{b^2-4ac}}{2b}.$$

不过需要网络哦！

注意的一点事，这个公式的`$`个数和`latex`标准不太一样哦！是两个啦！不支持行内公式。

## 方案3 支持中文
就是直接在这里写，但是可以通过`Marked`进行查看。因为Marked支持`MathJax`的渲染。~~不过好像需要联网才行。~~

`nvALT`是可以使用外部编辑器的。所以通过`Marked`这款专门用来看`Markdown`语言的工具来进行实时浏览很方便。

## 方案4 最佳方案
`Mou`竟然支持数学表达式！！！XD 只需要在两个`$$敲击代码$$`之间敲击代码即可。支持`Latex`的代码方式哦！！太好用了啦！！

	$$\sum_{i\to 2}^i$$

是不是很酷呀！！
