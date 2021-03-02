# HTML基础

## html骨架

```html
<html>   
    <head>     
        <title></title>
    </head>
    <body>
    </body>
</html>
```



## 文档类型

> html5的文档声明<!DOCTYPE html>

## 页面语言

> <html lang="en"> 指定html 语言种类

## html头部

> \<head>元素包含了所有的头部标签元素。
>
> 在\<head>元素中可以插入脚本（scripts），样式文件（CSS），及各种meta信息。
>
> ​	\<head>定义了文档的信息。
>
> ​	\<titile>定义了文档的标题。
>
> ​	\<base>定义了页面链接标签的默认链接地址。
>
> ​	\<link>定义了一个文档和外部资源之间的关系。
>
> ​	\<meta>定义了HTML文档中的元数据。可以为搜索引擎定义关键词；为网页定义描述内容；定义网页作  者；或其他Web服务。
>
> ​	\<script>定义了客户端的脚本文档。
>
> ​	\<noscript>定义在脚本未被执行是的代替内容（文本）。
>
> ​	\<style>定义了HTML文档的样式文件。

```html
<html>
	<head>
		<title>浏览器工具栏中的标题</title>
         <!-- <link>标签用于链接到CSS样式表 -->
         <link rel="stylesheet" type="text/css" href="mystyle.css">
         <!-- <link>标签设置网页图标 -->
         <link rel="shortcut icon" href="picture_url">
        有列于网站seo
         <!-- <meta>标签为搜索引擎定义关键词 -->
		<meta name="keywords" content="HTML";>
         <!-- <meta>标签为网页定义描述内容 -->
		<meta name="description" content="HTML学习";>
         <!-- <meta>标签定义网页作者 -->
		<meta name="author" content="wang tsinghua";>
         <!-- <meta>标签设置每30秒刷新当前页面 -->
		<meta http-equiv="refresh" content="30";>
         <!-- <meta>标签定义字符集,没有这个网页就会出现乱码 -->
		<meta charset=utf-8;>
         <style type="text/css">
             body {background-color:yellow}
             p {color:blue}
         </style>
    </head>
</html>
```



## html标题标签

```html
<h1>这是一级标题</h1>

<h2>这是二级标题</h2>

<h3>这是三级标题</h3>

<h4>这是四级标题</h4>

<h5>这是五级标题</h5>

<h6>这是六级标题</h6>
```

## html水平线标签

> 在不产生一个新段落的情况下进行换行。

```html
<hr />
```

## html换行标签

```html
<br />
```

## html注释

```html
<!-- 注释内容 -->
```

## html段落标签

```html
<p>段落</p>
```

> 浏览器会自动在段落前后添加空行！

## html格式化标签

> \<b>粗体\</b>
>
> \<strong>粗体\</strong>
>
> \<i>斜体\</i>
>
> \<em>斜体\</em>
>
> \<s>删除线\</s>
>
> \<u>下划线\</u>
>
> \<sub>定义下标字\</sub>
>
> \<sup>定义上标字\</sup>
>
> \<small>定义小号字\</small>

```html
<b>粗体</b> 记主
<strong>粗体</strong> 记主

<i>斜体</i> 记主
<em>斜体</em> 记主

<s>删除线</s>

<u>下划线</u>

<sub>定义下标字</sub>

<sup>定义上标字</sup>

<small>定义小号字</small>
```



## html图片标签

> 语法:\<img src="图像_url"> 
>
> alt属性用来为图像定义一串预备的可替代的文本。
>
> title属性设置鼠标放在图片上时显示的文字
>
> border属性设置图片的边框,一般为0
>
> align属性设置图片的居中,有左eft居中和有right居中
>
> width、height属性用于指定设置图像的宽度与高度。单位为px（像素【默认】）或%（百分比）。

```html
<img src="../res/img/p001.png" alt="射击游戏" title="测试" width="800" height="400" border="1">
```



## html链接标签

> 使用href属性来描述链接的目标地址。

```html
<a herf="https://127.0.0.1">链接</a>
```

> 使用target属性规定在何处打开链接文档。
>
> ​	_blank:在新窗口中打开被链接文档。
>
> ​	_self:默认。在相同的框架中打开被链接文档。
>
> ​	_parent:在父框架集中打开被链接文档。
>
> ​	_top:在整个窗口中打开被链接文档。
>
> ​	framename:在指定的框架中打开被链接文档。

```html
<a href="http://127.0.0.1" target="_blank">k0</a>
<a href="http://127.0.0.1" target="_self">k0</a>
<a href="http://127.0.0.1" target="_parent">k0</a>
<a href="http://127.0.0.1" target="_top">k0</a>
<a href="http://127.0.0.1" target="framename">k0</a>
```

> 使用title属性设置鼠标放在链接上时显示的文字。

```html
 <a href="http://127.0.0.1" target="_blank" title="测试">k0</a>
```

> 扩展-描点

```html
<a href="#id名"></a>
<p id="id名">11</p>
```

> 图片链接

```html
<a href="#" target="_blank">
<img src="#">
</a>
```

> 邮箱链接

```html
<!-- 简单的邮箱链接 -->
<a href="mailto:someone@microsoft.com?subject=Hello%20again">发送邮件</a>
注意：应该使用 %20 来替换单词之间的空格，这样浏览器就可以正确地显示文本了。
```

```html
<!-- 另一个mailto链接 -->
<a href="mailto:someone@microsoft.com?cc=someoneelse@microsoft.com&bcc=andsomeoneelse2@microsoft.com&subject=Summer%20Party&body=You%20are%20invited%20to%20a%20big%20summer%20party!">发送邮件！</a>
注意：应该使用 %20 来替换单词之间的空格，这样浏览器就可以正确地显示文本了。
```



## html CSS

> ​	CSS(层叠样式表或级联样式表 Cascading Style Sheets)是用于渲染HTML元素标签的样式。
>
> ​	CSS可以通过以下方式添加到HTML中：
>
> - 内联样式：在HTML元素中使用\<style>属性。
> - 内部样式表：在HTML文档头部\<head>区域使用\<style>元素来包含CSS。
> - 外部引用：使用外部CSS文件。

```html
<!-- 内联样式(行内样式) -->
<h1 style="font-family:arial; text-align:center; ">
    学习HTML
</h1>
<p style="font-family:arial; color:red; font-size:20px; ">
    CSS内联样式
</p>
```

```html
<!-- 内部样式表 -->
<head>
<style type="text.css">
    h1 {color:red;}
    p {color:blue;}
</style>
</head>
```

```html
<!-- 外部样式表 -->
<head>
    <link rel="stylesheet" type="text/css" href="../res/css/基础.css">
</head>
```



## 路径

>  路径分:绝对路径,相对路径
>
> 相对路径又分:同一级,下一级,上一级路径

### 绝对路径

> 绝对路径以Web站点根目录为参考基础的目录路径。之所以称为绝对，意指当所有网页引用同一个文件时，所使用的路径都是一样的。

```html
“D:\web\img\logo.gif”，或完整的网络地址，例如“http://www.itcast.cn/images/logo.gif”。
```

### 相对路径

| 路径分类   | 符号  | 说明                                                         |
| ---------- | ----- | ------------------------------------------------------------ |
| 同一级路径 |       | 只需输入图像文件的名称即可，如<img  src="#" />。<img src='#'> |
| 下一级路径 | “/”   | 图像文件位于HTML文件同级文件夹下（例如文件夹名称为：images）  如<img src="#" />。 <img src="#"/> |
| 上一级路径 | “../” | 在文件名之前加入“../”  ，如果是上两级，则需要使用 “../ ../”，以此类推， 如<img src="#" />。 <img  src='#'/> |

## html区块

> HTML块级元素（在浏览器中显示时，通常会以新行来开始和结束，另起一行，如：\<div>,\<h1>,\<p>,\<ul>,\<table>等元素。）
>
> HTML内联元素（在浏览器中显示时，通常不会以新行来开始和结束，如：\<span>,\<a>,\<img>,\<b>,\<td>等元素。）

> \<div>元素是块级元素，可用于组合其他HTML元素的容器。如果与CSS一同使用，\<div>元素可用于对大的内容块设置样式属性。

```html
<div style="color:#FF0000">
    <h1>
        div中的元素标题
    </h1>
    <p>
        div中的文本
    </p>
</div>
```

> \<span>元素是内联元素，可用作文本的容器。如果与CSS一同使用，\<span>元素可用于对部分的文本设置样式属性。

```html
<p>我的哥哥有<span style="color:#0000FF; font-weight:bold">蓝色</span>的球鞋，我的姐姐有<span style="color:#FF0000; font-weight:bold">红色</span>的球鞋。</p>
```

> div和span的区别
>
> div一行放不了多个,span一行可以放多个





## html脚本

> 向HTML添加脚本，使HTML页面具有更强的动态性和交互性。
>
> \<script>:定义了客户端脚本。
>
> \<noscript>:定义了不支持脚本浏览器输出的文本。

```html
<script>
document.write("Hello world!");
</script>
<nosript>
抱歉，您的浏览器不支持JavaScript！
</nosript>
```



## html内联框架

> \<iframe>标签规定一个内联框架。一个内联框架被用来在当前HTML文档中嵌入另一个文档。
>
> 语法: \<iframe src="url">\</iframe>
>
> src 必要属性，填url
>
> width、height属性用于指定设置图像的宽度与高度。单位为px（像素【默认】）或%（百分比）。
>
> frameborder属性用于定义是否显示边框。（1【默认】：开启边框；0：移除边框。）

```html
<iframe src="https://www.w3cschool.cn" width="300" height="300" frameborder="0">
</iframe>
```

> 使用iframe 作为链接的目标(traget)
>
> 链接的target属性必须引用iframe 的name属性
>
> 示例：

```html
<iframe src="demo_iframe.htm" name="iframe_a"></iframe>
<p><a href="http://www.w3school.com.cn" target="iframe_a">W3School.com.cn</a></p
```



## html框架

> 语法：
> \<frameset rows="50%,*">
>
> \<frame src="http://www.baidu.com" scrolling="no"/>
> \<frame src="http://www.soso.com" />
> \</frameset>
> frameset 不能在body内使用
> frame 一般都是在frameset中使用



> 属性：
> cols 定义框架集中列的数目和尺寸
> rows 定义框架集中行的数目和尺寸eg:rows="50%,*" *就会复制前面的50%
> scrolling   滚动条 eg：scrolling="no"
>      auto 在需要的情况下出现滚动条（默认值）。
>      yes  始终显示滚动条（即使不需要）。
>      no 从不显示滚动条（即使需要）

```html
<frameset rows="50%,*">

<frame src="http://www.baidu.com" scrolling="no"/>
<frame src="http://www.soso.com" />
</frameset>
```



## html列表

> 无序列表ul
>
> \<ul>:unordered lists
>
> \<li>:list item
>
> 属性：square正方形,circle空心圆，disc实心圆''
>
> eg:\<ul type="disc">实心圆\</ul>

```html
<ul>
	<li>apple</li>
    <li>banana</li>
    <li>pineapple</li>
</ul>
<ul type="disc">
	<li>apple</li>
    <li>banana</li>
    <li>pineapple</li>
</ul>
```

> 有序列表ol(默认数字列表)
>
> \<ol>:ordered lists
>
> \<li>:list item
>
> 属性：小写字母列表 a,大写字母列表 A,罗马字母列表  I,小写罗马字母列表 i

```html
<ol>
	<li>apple</li>
    <li>banana</li>
    <li>pineapple</li>
</ol>
```

> 自定义列表
>
> \<dl>:definition lists(自定义列表)
>
> \<dt>:definition term(自定义列表组)
>
> \<dd>:definition description(自定义列表描述)

```html
<dl>
    <dt>apple</dt>
    	<dd>big and red</dd>
    <dt>banana</dt>
    	<dd>smell and sweet</dd>
</dl>
```



## html颜色

> \#000000 ~ \#FFFFFF
>
> rgb: rgb(0,0,0)
>
> 颜色名

## HTML字符实体

> | 显示结果 | 描述         | 实体名称  | 实体编号 |
> | -------- | ------------ | --------- | -------- |
> |          | 空格         | \&nbsp;   | \&#160;  |
> | <        | 小于号(常用) | \&lt;     | \&#60;   |
> | >        | 大于号(常用) | \&gt;     | \&#62;   |
> | &        | 和号         | \&amp;    | \&#38;   |
> | "        | 引号         | \&quot;   | \&#34;   |
> | '        | 撇号         | \&apos;   | \&#39;   |
> | &cent;   | 分           | \&cent;   | \&#162;  |
> | &pound;  | 镑           | \&pound;  | \&#163;  |
> | ￥       | 人民币/日元  | \&yen;    | \&#165;  |
> | &euro;   | 欧元         | \&euro;   | \&#8364; |
> | &sect;   | 小节         | \&sect;   | \&#167;  |
> | &copy;   | 版权         | \&copy;   | \&#169;  |
> | &reg;    | 注册商标     | \&reg;    | \&#174;  |
> | &trade;  | 商标         | \&trade;  | \&#8482; |
> | &divide; | 除号         | \&divide; | \&#247;  |



## base标签

>设置整体链接的打开状态，
>
>base写到`<head></head>`之间
>
>所有的链接都会默认添加target="_blank"



## pre标签

> **pre**标签（预格式化文本标签)
>
> **按照我们预先写好的文字格式来显示页面，保留空格和换行**

