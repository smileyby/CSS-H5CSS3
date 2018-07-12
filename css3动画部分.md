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

[点击查看-示例代码](https://codepen.io/smileyby/pen/gjpoJg)

