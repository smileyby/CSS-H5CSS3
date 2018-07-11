Forms
=====

## 新增input元素的种类

* search：搜索输入框
* tel：电话号码输入框
* url：输入url地址
* email：邮件输入框
* number：数字输入框
* range：特定范围内的数值选择器（通过拖动滚动条改变一定范围内的数字）
* color：颜色选取器指在Opera和Blackberry浏览器
* datetime：显示完整日期和事件 UTC标准时间
* datetime-local：显示完整日期时间
* time：显示时间
* month：显示月
* week：显示周
* submit：提交

[点击查看-实例演示](https://codepen.io/smileyby/pen/mjdEGJ)

## 新增表单特性

* placeholder：输入框占位符，常用作输入提示，在光标聚焦时，占位符自动消失
* autocomplete：是否保存用户输入值（默认为on，关闭为off）
* autofocus：自动聚焦
* required：此项必填，不能为空
* pattern：正则验证pattern="\d{1,5}"
* form属性只要加载form属性，表单元素可以放在页面的任意位置
* formnovalidate和novalidate：他俩都表示不需要验证表单，直接提交novlidate用于form标签；formnovalidate用于submit类型的提交按钮

[点击验证上述属性](https://codepen.io/smileyby/pen/zLYKGb)

## 表单验证

* validity对象，通过下面的valid可以查看验证是否通过

	var oText = document.querySelecter('#text');
	oText.addEventListener('invalid',fn,false);
	function fn(){
		console.log(this.validity);
	}

* valid：验证不通过时返回false
* valueMissing：输入值为空时返回true
* typeMismatch：空间值与预期类型不匹配
* patternMismatch：输入值不满足pattern正则
* customError 不符合自定义验证（setCustomValidity()自定义验证提示）[自定义验证提示-效果演示](https://codepen.io/smileyby/pen/NBWbKe)

[点击查看-验证对象](https://codepen.io/smileyby/pen/bjGwYv)