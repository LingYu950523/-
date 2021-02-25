# 第十五天

CSS动画原理

文档对象模型DOM

用SetInInterval设定计时器。

可以用开发者工具 Rendering 来查看屏幕上重新渲染的地方。

transform：translateX（0=>300px）这种语法可以减少浏览器的渲染次数。

---------

## 浏览器的渲染

浏览器的渲染过程分六步：

1. 根据HTML构建HTML树（DOM）
2. 根据CSS构建CSS树（CSSOM）
3. 将两棵树合并为渲染树（Render Tree）
4. Layout 布局（盒模型、文档流、计算大小和位置）
5. Paint 绘制（边框颜色、文字颜色、背景颜色、阴影等画出来）
6. Compose 合成（将层叠关系展示出来）

但是更新样式的时候一般使用JS，一般直接加类。

样式更新又会有以下三种方式：

* JS/CSS > 样式 > 布局 > 绘制 > 合成
* JS/CSS > 样式 > 绘制 > 合成
* JS/CSS > 样式 > 合成

transform：translateX（0=>300px）这种语法可以减少浏览器的渲染次数，也就是完成第三种样式更新，直接浮动元素进行变动。

CSS动画优化看google写的文章。

：hover是鼠标悬浮事件

transform 可以看MDN的语法。作用：

* 位移。 可以XY轴动，也可以按Z轴动，如果是Z轴那需要事先确定一个视点。

```CSS
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
```
以上可以让绝对位置元素定位在居中位置。

* 缩放。 scale。transition： all 1s 可以加上动画效果。
    和transform类似，但border也会一起变换，会变形。

* 旋转。 rotate。

* 倾斜。 Skew。
  可以合并一起写


--------------
Transition 过渡，补充中间帧

语法：transition：属性名 时长 过渡方式 延迟

e.g. transition：left 200ms linear

可以用逗号分隔两个不同的属性。

有些属性是无法过渡的，例如display：none=》block就不能过渡。

透明度的过渡一般使用visibility：hidden=》visible

如果需要用transition做两段动画需要中间加上监控点

----------
animation 动画，做三个关键帧

@keyframe的语法：mdn

一种是from。。to。。写法，一种是百分数写法

然后就把keyframe放进animation就可以了

animation：时长｜过渡方式｜延迟｜次数｜方向｜填充模式｜是否暂停｜动画名



