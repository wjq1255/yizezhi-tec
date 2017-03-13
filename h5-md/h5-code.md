# H5常用代码及规范

#### 1、屏幕适配JS代码
```
	<pre class="brush:html;gutter:true;">
	<script>
	　　if(/Android (\d+\.\d+)/.test(navigator.userAgent)){
	var version = parseFloat(RegExp.$1);
	if(version>2.3){
	var phoneScale = parseInt(window.screen.width)/750;
	document.write(&#39;<meta name="viewport" content="width=750, minimum-scale = &#39;+ phoneScale +&#39;, maximum-scale = &#39;+ phoneScale +&#39;, target-densitydpi=device-dpi">&#39;);
	}else{
	document.write(&#39;<meta name="viewport" content="width=750, target-densitydpi=device-dpi">&#39;);
	}
	}else{
	document.write(&#39;<meta name="viewport" content="width=750, user-scalable=no, target-densitydpi=device-dpi,minimal-ui">&#39;);
	　　}
	　　var html = document.querySelector(&#39;html&#39;);
	var rem = html.offsetWidth / 7.5 ;
	html.style.fontSize = rem + &#39;px&#39; ;
	<script>
	</pre>
```
#### 2、简单选择器
```
function $(selector){
　　return document.querySelector(selector);
}
```
#### 3、添加class
```
function addClass(obj,claName){
　　var reg = new RegExp("(^|\\s+)"+claName+"($|\\s+)");
　　if(!obj.className.match(reg)){
obj.className+=" "+claName;
　　}
　　return obj;
}
```
#### 4、删除class
```
function removeClass(obj,claName){
　　var reg = new RegExp("(^|\\s+)"+claName+"($|\\s+)");
　　if(obj.className.match(reg)){
obj.className=obj.className.replace(reg,"");
　　}
　　return obj;	
}
```
#### 5、loadJS（jonp）
```
function loadJs(url){
　　var script = document.createElement("script");
　　document.getElementsByTagName("head")[0].appendChild(script);
　　script.src=url;
}
```
#### 6、ajax
```
function ajax(method,url,callback,data){
　　var xhr = window.XMLHttpRequest ? new XMLHttpRequest() : new ActiveXObject("Microsoft.XMLHTTP");
　　xhr.onreadystatechange=function(){
　　　　if(xhr.readyState==4&&xhr.status==200){
　　	　　callback&&callback(xhr.responseText)
　　　　}
　　}
　　xhr.open(method,url);
　　if(data){
　　　　xhr.send(data);
　　}
}
```
#### 7、微信检测
```
if((window.navigator.userAgent.toLowerCase().match(/MicroMessenger/i) == &#39;micromessenger&#39;)){
　　//微信
}
```
#### 8、QQ检测
```
if(window.navigator.userAgent.match(/QQ\//i)){
　　//qq 
}
```