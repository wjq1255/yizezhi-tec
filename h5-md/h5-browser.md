# HTML5 浏览器支持

> 你可以让一些较早的浏览器（不支持HTML5）支持 HTML5。

---

#### 将 HTML5 元素定义为块元素

HTML5 定了 8 个新的 HTML 语义（semantic） 元素。所有这些元素都是 块级 元素。
为了能让旧版本的浏览器正确显示这些元素，你可以设置 CSS 的 display 属性值为 block:

		header, section, footer, aside, nav, main, article, figure {
	    	display: block; 
		}

#### 为 HTML 添加新元素

你可以为 HTML 添加新的元素。
该实例向 HTML 添加的新的元素，并为该元素定义样式，元素名为 <myHero> ：
JavaScript 语句 document.createElement("myHero") 是为 IE 浏览器添加新的元素。

#### Internet Explorer 浏览器问题

完美的 Shiv 解决方案
实例
```
	<!DOCTYPE html>
	<html>
	<head>
	<meta charset="utf-8">
	<title>渲染 HTML5</title>
	  <!--[if lt IE 9]>
	  <script src="http://cdn.static.runoob.com/libs/html5shiv/3.7/html5shiv.min.js"></script>
	  <![endif]-->
	</head>
	 
	<body>
	 
	<h1>易则知教程</h1>
	 
	<article>
	易则知教程 —— 简单易知，成就非凡！！！
	</article>
	 
	</body>
	</html>
```