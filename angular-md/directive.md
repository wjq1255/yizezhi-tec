# 指令

> **摘要**：Directive（指令）是AngularJ非常强大而有有用的功能之一。它就相当于为我们写了公共的**自定义DOM元素或CLASS属性或ATTR属性**，并且它不只是单单如此，你还可以在它的基础上来**操作scope、绑定事件、更改样式**等。通过这个Directive，我们可以封装很多公共指令，比如分页指令、自动补全指令等等。然后在HTML页面里只需要简单的写一行代码就可以实现很多强大的功能。

一般情况下，需要用Directive有下面的情景：
- 使你的Html更具语义化，不需要深入研究代码和逻辑即可知道页面的大致逻辑。
- 抽象一个自定义组件，在其他地方进行重用。

#### 一、Directive的定义及其使用方法
AngularJs的指令定义大致如下
```
angular.module("app",[]).directive("directiveName",function(){ 
	return{ 
	//通过设置项来定义 
	}; 
})
```
Directive可以放置于元素名、属性、class、注释中。