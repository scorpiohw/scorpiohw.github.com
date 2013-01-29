---
layout: post
title: "如何在nvALT中加入图片"
date: 2013-01-29 15:17
comments: true
categories: [Tech, Markdown]
---
## 方法一
{% img /pictures/插入图片测试.png 测试图片1%}  

`![插入图片测试](./pictures/插入图片测试.png)`

如上所示，我在`nvALT`数据库中建立了一个专门用于存放`_Picture`的文件，之后把所有的图片放在这里，通过`Markdown`语言的特性进行调用。

因为`nvALT`支持第三方编辑器的修改。所以可以很容易的启动`Mou`这个软件。这样就可以完美解决`nvALT`只能存文本的情况了。真的是太好用了。。。以后就可以保存图片了！XD

## 方法二

方法一中的方式使通过相对地址。这样的好处是只要文件结构相同不需要修改代码。方法二中采用的是直接地址，好处是可以添加文件，添加视频等等任何东西都可以只要绝对地址不改变。不过对于文件结构稳定性要求较高。不适合长期使用。还是相对地址比较合适。当然如果是有效期比较短的文件没有什么问题，使用完直接`export`就好了。如果有效期比较长的文件就需要考虑引用方式了。

{% img /pictures/mouth.png 测试图片2%} 

`![](file:///Users/Mike/Dropbox/Apps/nvALT%20Data/pictures/mouth.png)`