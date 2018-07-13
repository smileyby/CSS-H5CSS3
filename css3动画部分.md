CSS3 动画部份
============

* transition 过渡动画
* transform 变型属性
* animation 帧动画

> transition-property 过渡属性 all[attr]
> 
> transition-duration 过渡时间
> 
> transition-delay 延迟时间
>
> transition-timing-function 运动类型
>> ease:(逐渐变慢)默认值
>
>> linear:匀速 
>
>> ease-in 加速
>
>> ease-out 减速
>
>> ease-in-out 先加速后减速
>
>> cubic-bezier 贝塞尔曲线（x1,y1,x2,y2）[贝塞尔曲线](http://cubic-bezier.com)

## 如何分析一个动画效果
1. 找到过度属性
2. 找到过度属性的起始值和结束值
3. 在合适的位置增加transition属性

## 2D变换一般配合transition使用

> transform

* rotate() 旋转函数
>> deg 度数 transform-origin 旋转基点

* skew() 倾斜函数
>> skewX() skewY()

* scale() 缩放函数 默认值是1
>> scaleX() scaleY()

* translate() 位移函数
>> translateX() translateY()

**动画之间的顺序会影响元素动画的基点**

**translate方法，默认的基准点不会发生改变永远都是元素的中心点**

[点击查看-示例代码](https://codepen.io/smileyby/pen/gjpoJg)

## animation帧动画

> 关键帧-@keyframes
>> 类似flash （定义动画的每个阶段的样式，即帧动画）
>
> 关键帧的时间单位
>> 数字：0%、25%、100%等（设置某个时间段内的任意时间点的样式）
> 
> 格式

	@keyframes 动画名称 {
		动画状态
	} 

> 必要属性
>> animation-name 动画名称（关键帧名称）
>
>> animation-duration 动画执行时间

> 可选属性
>> animation-timing-function
>
>> 可能的取值：linear匀速、ease缓冲、ease-in由慢到快、ease-out由快到慢、ease-in-out由慢到块再到慢、cubic-bezier 贝赛尔曲线 
>
>> animation-delay 动画延迟
>
>> animation-iteration-count 重复次数
>
>> animation-direction 动画运行的方向
>> 可能的取值：normal|reverse|alternate|alternate-reverse
>
>> animation-play-state 动画状态
>> 可能取值：running|paused
>
>> animation-fill-mode 动画结束后的状态
>> 可能取值：none|forward|backwards|both

[点击查看-动画示例](https://codepen.io/smileyby/pen/xJwxMY)

[点击查看-综合练习](https://codepen.io/smileyby/pen/jpbEJY)

## transform3D变形

* transform-style: flat | preserve-3d(3D空间展示)
* perspective 景深效果 （设置给父元素）
* transform: perspective(800px) 直接作用在子元素上
* transform 新增函数
* [translate3d](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/translate3d)(tx, ty, tz) => translateX() translateY() translateZ()
* translateZ 近大远小
* [rotate3d](https://developer.mozilla.org/zh-CN/docs/Web/CSS/transform-function/rotate3d)(rx, ry, rz) => rotateX() rotateY() rotateZ()
* rotateZ() 需要其他效果配合才能起作用，单独使用不起作用。
* [scale3d](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/scale3d)(sx, sy, sz) => scaleX() scaleY() scaleZ()

[点击查看-效果展示](https://codepen.io/smileyby/pen/BPoLjy)

[点击查看-3D变换练习1](https://codepen.io/smileyby/pen/YjyNbR)

[点击查看-3D变换练习2](https://codepen.io/smileyby/pen/LBpOdO)



