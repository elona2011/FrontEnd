样本代码：

```html
<!DOCTYPE html>
<html>
<head>
	<title></title>
</head>
<body>
	<div class="main">
		<div class="loader"></div>
	</div>
	
	<link rel="stylesheet" href="./test.css" type="text/css" />
</body>
</html>
```

HTML 颜色名 http://www.w3school.com.cn/tags/html_ref_colornames.asp

HTML 字符实体 http://www.w3school.com.cn/tags/html_ref_entities.html
 	空格	&nbsp;	&#160;
<	小于号	&lt;	&#60;
>	大于号	&gt;	&#62;
&	和号	&amp;	&#38;
"	引号	&quot;	&#34;
'	撇号 	&apos; (IE不支持)	&#39;
￠	分	&cent;	&#162;
£	镑	&pound;	&#163;
¥	日圆	&yen;	&#165;
€	欧元	&euro;	&#8364;
§	小节	&sect;	&#167;
©	版权	&copy;	&#169;
®	注册商标	&reg;	&#174;
™	商标	&trade;	&#8482;
×	乘号	&times;	&#215;
÷	除号	&divide;	&#247;
 	
例：黑色三角
<div>
    &blacktriangledown; Details
</div>

<div tabindex="0"> 用于设置是否可以落焦点，以及触发键盘事件





网址后加#q4，代表打开页面后移动到q4位置。

顺序一定不能反：
a:link{
    color:gray;
}
a:visited{
}
a:hover{
}
a:active{
}

空格
1. 使用输出html标签&nbsp;来解决
 document.write("&nbsp;&nbsp;"+"1"+"&nbsp;&nbsp;&nbsp;&nbsp;"+"23");
2. 使用CSS样式来解决
document.write("<span style='white-space:pre;'>"+"  1        2    3    "+"</span>");
 在输出时添加“white-space:pre;”样式属性。这个样式表示"空白会被浏览器保留"

乱码
<head>
 <meta charset＝"utf-8">
</head>


