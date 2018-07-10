CSS3选择器
=========

* <font color="red">结构选择器</font>

	:nth-child(n) 第几个元素 从1开始设置
	:nth-child(2n) 偶数元素 从0开始设置
	:nt-child(2n+1) 奇数元素
	:nth-of-type(n)
	:first-child -> nth-child(1)
	:first-of-type -> nth-of-type(1)
	:last-child
	:last-of-type
	:only-child 仅有一个子元素
	:only-of-type 同种类型的子元素还有一个
	:empty

* <font color="red">否定选择器</font>

	:not()

* <font color="red">属性选择器</font>

	E[attr=val]
	E[attr|=val] 只能等于val 或只能以val-开头
	E[attr*=val] 包含val字符串
	E[attr~=val] 属性值有多个，其中有一个是val
	E[attr^=val] 以val开头
	E[attr$=val] 以val结尾
	