---
layout: post
title: 表单美化
---

由于浏览器自带的表单默认样式有些是无法通过css样式表来修改，而且各个浏览器的默认样式也并不一致，看起来就像这个样子

![]({{site.baseurl}}/asset/img/form-beautify/img1.png)

若要实现自定义表单样式，就要通过css3或图片+js来模拟实现，css3适用于高级浏览器，图片+js模拟兼容性更广，美化后的表单样式就像下面这样

![]({{site.baseurl}}/asset/img/form-beautify/img2.png)

### 实现原理
radio,checkbox：通过label标签的for属性指向标签id，label标签可以自定义样式，radio和checkbox可以隐藏起来

```
<div class="u-radio">
  <input id="r1" type="radio" name="sex" checked>
  <label for="r1">男</label>
</div>
<div class="u-radio">
  <input id="r2" type="radio" name="sex">
  <label for="r2">女</label>
</div>


<div class="u-checkbox">
  <input id="h1" type="checkbox" name="hobby">
  <label for="h1">篮球</label>
</div>
<div class="u-checkbox">
  <input id="h2" type="checkbox" name="hobby">
  <label for="h2">足球</label>
</div>
```

select：通过ul,隐藏input[type='hidden']来模拟

```
<div class="u-select j-select">
  <p>设计师</p>
  <input type="hidden" value="">
  <ul>
  <li data-val="0">请选择</li>
  <li data-val="1">设计师</li>
  <li class="z-sel" data-val="2">厨师</li>
  <li data-val="3">理想家</li>
  <li data-val="4">僧侣</li>
  </ul>
</div>
```

### 完整代码
<a href="{{site.baseurl}}/demo/form-beautify/index.html" target="_blank">demo</a>

