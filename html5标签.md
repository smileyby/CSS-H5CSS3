HTML5标签
========

## 前言

> HTML5语法变化
>
>1. DOCTYPE及字符编码

	html5文档声明
	<!DOCTYPE html>
	html4文档申明类型
	<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">

	html5字符编码
	<meta charset="UTF-8">
	html4字符编码
	<meta http-equip="Content-Type" content="text/html;charset=utf-8">

>2. 大小写都可以

	<Input type="Radio">
	
>3. 具有布尔属性

	html4中
	<input type="checkbox" checked="checked">
	html5中
	<input type="checkbox" checked>
	只写属性不写值时默认是true，如果想要将属性设置为false，可以不适用该属性

>4. 部分标签可以省略

	1.不允许写的结束符的标签：area/basebr/col/command/embed/hr/img/input/link/meta/param/source/track/wbr
	
	2.可以省略结束符的标签：li/dt/dd/p/rt/optgroup/option/colgroup/thread/tbody/tr/td/th

	3.可以完全省略的标签：html/head/body/colgroup/tbody

**以上内容了解为主**

## 语义化标签

* section
> w3c规范规定section是用来划分网页，表示网页中的一个内容区块，比如章节，页眉，页脚或页面的其他部分，可以和h1，h2...等其他标签结合气啦使用，表示文档结构（表示范围很广，任何区块都可以用section标签来表示）

* hgroup----对整个页面/页面中的一个内容区块的标题进行组合
* header----一个内容区块或页面的头部部分
* footer----整个页面或页面区块的尾部
* nav----页面中导航链接的部分
* article----定义可以独立于内容其余部分的完整独立内容快，article元素就是专门为**摘要**设计的，比如一篇文章
* aside----表示article标签内容之外的，与article标签内容相关的辅助信息，aside元素应该被用于无关内容（可用在主要内容相关的引用，侧边栏，广告，nav元素组等）**简单来说：aside的内容如果被删除，剩下的内容仍然很合理**
* figure----表示一段独立的流内容，一般表示文档主体流内容中的一个独立单元（figure元素常用语图片）
* figcaption----代表一个图例的说明、代表了figure元素的一个标题或者说是其相关解释，在使用figcaption时，它最好是figure块的第一个或者最后一个元素

## 兼容性问题

* HTML5语义化标签在IE6-8下，对于不支持的标签不会有任何的样式，也默认的当成行内元素出现，所以在样式表里要对这些标签定义一下它默认的display
* 通过引入如下js解决IE9一下新增标签的兼容问题	
	<!-- IE条件注释法 -->
	<!--[if lt IE 9]>
		<script type="text/javascript" src="html5shiv.min.js"></script>
	<![endid]-->

具体代码如下：

	/**
	* @preserve HTML5 Shiv 3.7.3 | @afarkas @jdalton @jon_neal @rem | MIT/GPL2 Licensed
	*/
	!function(a,b){function c(a,b){var c=a.createElement("p"),d=a.getElementsByTagName("head")[0]||a.documentElement;return c.innerHTML="x<style>"+b+"</style>",d.insertBefore(c.lastChild,d.firstChild)}function d(){var a=t.elements;return"string"==typeof a?a.split(" "):a}function e(a,b){var c=t.elements;"string"!=typeof c&&(c=c.join(" ")),"string"!=typeof a&&(a=a.join(" ")),t.elements=c+" "+a,j(b)}function f(a){var b=s[a[q]];return b||(b={},r++,a[q]=r,s[r]=b),b}function g(a,c,d){if(c||(c=b),l)return c.createElement(a);d||(d=f(c));var e;return e=d.cache[a]?d.cache[a].cloneNode():p.test(a)?(d.cache[a]=d.createElem(a)).cloneNode():d.createElem(a),!e.canHaveChildren||o.test(a)||e.tagUrn?e:d.frag.appendChild(e)}function h(a,c){if(a||(a=b),l)return a.createDocumentFragment();c=c||f(a);for(var e=c.frag.cloneNode(),g=0,h=d(),i=h.length;i>g;g++)e.createElement(h[g]);return e}function i(a,b){b.cache||(b.cache={},b.createElem=a.createElement,b.createFrag=a.createDocumentFragment,b.frag=b.createFrag()),a.createElement=function(c){return t.shivMethods?g(c,a,b):b.createElem(c)},a.createDocumentFragment=Function("h,f","return function(){var n=f.cloneNode(),c=n.createElement;h.shivMethods&&("+d().join().replace(/[\w\-:]+/g,function(a){return b.createElem(a),b.frag.createElement(a),'c("'+a+'")'})+");return n}")(t,b.frag)}function j(a){a||(a=b);var d=f(a);return!t.shivCSS||k||d.hasCSS||(d.hasCSS=!!c(a,"article,aside,dialog,figcaption,figure,footer,header,hgroup,main,nav,section{display:block}mark{background:#FF0;color:#000}template{display:none}")),l||i(a,d),a}var k,l,m="3.7.3",n=a.html5||{},o=/^<|^(?:button|map|select|textarea|object|iframe|option|optgroup)$/i,p=/^(?:a|b|code|div|fieldset|h1|h2|h3|h4|h5|h6|i|label|li|ol|p|q|span|strong|style|table|tbody|td|th|tr|ul)$/i,q="_html5shiv",r=0,s={};!function(){try{var a=b.createElement("a");a.innerHTML="<xyz></xyz>",k="hidden"in a,l=1==a.childNodes.length||function(){b.createElement("a");var a=b.createDocumentFragment();return"undefined"==typeof a.cloneNode||"undefined"==typeof a.createDocumentFragment||"undefined"==typeof a.createElement}()}catch(c){k=!0,l=!0}}();var t={elements:n.elements||"abbr article aside audio bdi canvas data datalist details dialog figcaption figure footer header hgroup main mark meter nav output picture progress section summary template time video",version:m,shivCSS:n.shivCSS!==!1,supportsUnknownElements:l,shivMethods:n.shivMethods!==!1,type:"default",shivDocument:j,createElement:g,createDocumentFragment:h,addElements:e};a.html5=t,j(b),"object"==typeof module&&module.exports&&(module.exports=t)}("undefined"!=typeof window?window:this,document);

[github解决方案地址](https://github.com/aFarkas/html5shiv)
