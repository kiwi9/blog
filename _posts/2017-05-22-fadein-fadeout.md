---
layout: post
title: 淡入淡出
---
要让一个元素淡入，淡出，要控制它的透明度：`opacity`以及兼容ie系列的`filter:alpha(opacity=1)`

### 实现原理（以淡入为例子）

1. 获取当前元素的当前透明度
2. 判断是否处于不透明（opacity=1）
3. 如果不透明（即已经是透明度为1），则不做处理，返回
4. 清除定时器
5. 设置初始值和变化值，透明度从0~100，变化值5（可以是任意合适的）
6. 开启定时器
7. 判断初始值是否到达100，如果到达则淡入完成，关闭定时器
8. 没有达到100，则初始值累加变化值
9. 给元素设置相应的style

中文翻译代码感觉有些奇怪，不过可以理清思路，完整代码如下：

### 完整代码
<a href="{{site.baseurl}}/demo/fadeIn-fadeOut/index.html" target="_blank">demo</a>