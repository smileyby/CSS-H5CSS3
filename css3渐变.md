## 线性渐变

* linear-gradient

> 只能用在背景上
> 颜色沿着一条直线轴变化

	/* 渐变轴为45度，从蓝色渐变到红色 */
	linear-gradient(45deg, blue, red);

	/* 从右下到左上、从蓝色渐变到红色 */
	linear-gradient(to left top, blue, red);

	/* 从下到上，从蓝色开始渐变、到高度40%位置是绿色渐变开始、最后以红色结束 */
	linear-gradient(0deg, blue, green 40%, red);

**为了兼容，需要写对应的浏览器的私有前缀。私有前缀放在标准属性之前，当发生渐变角度不一致时，以标准属性为准。**

[点击查看-效果展示](https://codepen.io/smileyby/pen/ZjYQMw)

[点击查看-更详尽的使用指南](https://developer.mozilla.org/zh-CN/docs/Web/CSS/linear-gradient)

## 径向渐变

* radial-gradient([[<shape>||<size> [at <position>]?,|at<position>,]?<color-stop>[color-stop]+);
* 从“一个点”向多方向颜色渐变
* shape形状：ellipse、circle或设置水平半径垂直半径
* size：渐变的大小，即渐变到哪里停止，有如下关键词：closest-side(最近边)；farthest-side(最远边)；closest-corner(最近角)；farthest-corner(最远角，默认值)
* position：关键词|数值|百分比
* 重复的径向渐变

[点击查看-效果展示](https://codepen.io/smileyby/pen/djPNzQ)

[径向渐变-详细资料](https://developer.mozilla.org/zh-CN/docs/Web/CSS/radial-gradient)