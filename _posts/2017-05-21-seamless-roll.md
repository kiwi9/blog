---
layout: post
title: 无缝滚动
---
### 原理

这是无缝滚动的基本结构
![](/asset/img/seamless-roll/1.png)
```
<div id="j-roll" class="m-roll">
	<div class="wrap">
		<div class="inner">
			<ul>
				<li><a href="#"><img src="img1.jpg" alt=""></a></li>
				<li><a href="#"><img src="img2.jpg" alt=""></a></li>
			</ul>
		</div>
		<a class="prev" href="javascript:;">&lt;</a>
		<a class="next" href="javascript:;">&gt;</a>
	</div>
</div>
```
默认只有2个li，通过js复制一组在后面，也就是4个li，通过样式overflow隐藏掉
![](/asset/img/seamless-roll/2.png)

当图片移动时会是这样
![](/asset/img/seamless-roll/3.png)

再次移动
![](/asset/img/seamless-roll/4.png)

当移动到图片长度的一半时，若再点击移动，就把图片容器ul拉取到初始位置0，这样就可以图片无缝滚动了
![](/asset/img/seamless-roll/2.png)

### 完整代码
<a href="/demo/seamless-roll/index.html" target="_blank">demo</a>