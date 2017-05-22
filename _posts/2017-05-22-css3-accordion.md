---
layout: post
title: css3手风琴
---
手风琴效果一般实现需要通过js，不过css3也可以实现，效果如下
![]({{site.baseurl}}/asset/img/css3-accordion/1.jpg)

### html结构1：通过label，input[type="radio"]实现
```
<div class="m-accordion">
		<label for="r1"><img src="img1.jpg" alt=""></label>
		<input id="r1" type="radio" name="accordion">
		<label for="r2"><img src="img2.jpg" alt=""></label>
		<input id="r2" type="radio" name="accordion">
		<label for="r3"><img src="img3.jpg" alt=""></label>
		<input id="r3" type="radio" name="accordion">
		<label for="r4"><img src="img4.jpg" alt=""></label>
		<input id="r4" type="radio" name="accordion">
		<label for="r5"><img src="img5.jpg" alt=""></label>
		<input id="r5" type="radio" name="accordion">
	</div>
```
#### 实现原理：
label可以用来做图片容器，当点击图片时，也可以触发label对应的input[type="radio"]的是否选中，然后通过css3:`input:checked ~ label`来给对应的label添加对应的位移：transfrom

### html结构2：ul，li
```
<ul class="m-accordion m-accordion-1">
		<li><img src="img5.jpg" alt=""></li>
		<li><img src="img4.jpg" alt=""></li>
		<li><img src="img3.jpg" alt=""></li>
		<li><img src="img2.jpg" alt=""></li>
		<li><img src="img1.jpg" alt=""></li>
	</ul>
```
#### 实现原理：
主要应用css3伪类选择符：E:not(s)和transition，当鼠标hover到容器时，给所有没有hover的li设置宽度，当前hover到的li也设置对应宽度


### 完整代码
<a href="{{site.baseurl}}/demo/css3-accordion/index.html" target="_blank">demo</a>