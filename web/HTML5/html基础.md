
简单的HTML页面架构
```
<!DOCTYPE html>
<html>
<head>
	<title></title>
	<meta charset="utf-8">
</head>
<body>

</body>
</html>
```

```
meta标签
<meta> 元素可提供有关页面的元信息（meta-information），比如针对搜索引擎和更新频度的描述和关键词。

有利于网站seo
<meta name="keywords" content="网络安全，WEB渗透，数据安全，渗透测试，安全培训" />网站关键字
<meta name="desrciption" conter="暗月博客，打造最专业的网络安全博客，同时记录分享身边事" /> 网站的一些描述
<meta name="author" conter="moon"> 网站作者，给搜索引擎看的
```

```
<link> 标签定义文档与外部资源的关系。

<script> 引入js文件
```

```
标题标签
<h1>h1</h1>
<h2>h2</h2>
<h3>h3</h3>
<h4>h4</h4>
<h5>h5</h5>
<h6>h6</h6>
```

段落标签
```
<p>这是一个段落标签</p>
```

注释
```
<!-- 这是一个注释，在网页上看不见 -->
```

换行标签
```
<br />
```

水平线标签
```
<hr />
```

`div和span标签`
```
div和span标签都是盒子，用来装网页元素
相同：都是用来布局
不同：div一行只能放一个，span一行可以放多个
```
文本格式化标签(文本属性)
```
<strong></strong>加粗
<b></b>加粗
<i></i>斜体
<u></u> 下划线
<sup></sup>上标
<sub></sub>下标
<del></del>删除线
```
规定字体属性
```
<font></font> 规定字体属性
      size 字体大小
      color 字体颜色
```

`a标签(链接标签)`
```
作用:就是用于控制界面与页面之间的跳转

语法:<a href="https://www.baidu.com">百度</a>

属性:
     href(必要属性)
     target用于指定链接页面的打开方式
        默认是_self在当前页面打开
        _blank在新窗口打开

扩展-描点
<a href="#id名"></a>
<p id="id名">11</p>
```


`base标签`
```
作用:设置整体链接的打开状态
需要写到head里面
所有链接都会默认添加target="_blank"

语法:
<head>
<base href="">
</head>
```

`图片标签(img标签)`
```
作用:向网页中嵌入一幅图像。

语法:<img src="/1/egg.jpg" alt="鸡蛋">
属性:
    alt 规定图片的替代文本
    src 必要属性 规定显示图片的url
    width 规定图片的高度
    height 规定同的宽度
    title 规定鼠标触摸提示文本
    border 规定图片边框,一般默认为0
```

路径
```
路径分相对路径和绝对路径
相对路径又分同一级,下一级,上一级路径

绝对路径


相对路径
同一级路径
eg:<img src="baidu.git">
下一级路径(/)
eg: <img src="img/baidu.git">
上一级路径(../)
eg: <img src="../baidu.git">
```


预格式化标签(pre标签)
```
作用:保留原有的文字格式
<pre>
    11111
      222 2
</pre>
```

特殊符号
```
&nbsp; 空格
&gt; 大于号
&lt; 小于号
```


`表格table`
```
基本语法:
<table>

<tr> 每行
<td>单元格内的文字</td> 每格
</tr>

</table>

属性
 border 设置边框(默认为0px)
 cellspacing 设置单元格与单元格边框之间的空白间距(默认2像素)
 cellpadding 设置单元格内容与单元格边框之间的空白间距(默认1px)
 width 设置表格宽度
 height 设置表格高度
 align 设置表格再网页中水平对齐方式

 表头单元格标签th
 语法: 
 <tr> 直接替换td即可
<th>2</th>
<th>1</th>
 </tr>

表格标题标签caption
语法:
<table>
<caption>我是表格标题</caption>
</table>

合并单元格
跨行合并：rowspan=”合并单元格的个数”
跨列合并：colspan=”合并单元格的个数”
```
列表标签
```
无序列表ul
语法:
<ul>
  <li>列表项1</li>
  <li>列表项2</li>
</ul>
项目符号 square circle  disc
eg:<ul type="disc"></ul>

有序列表ol(默认数字列表)
语法:
<ol>
  <li>列表项1</li>
  <li>列表项2</li>
</ol>
属性
小写字母列表 a
大写字母列表 A
罗马字母列表  I
小写罗马字母列表 i


自定义列表
<dl>
  <dt>名词1</dt>
  <dd>名词1解释1</dd>
  <dd></dd>
</dl>


```

`input标签`
```
name：同样是表示的该文本输入框名称。
size：输入框的长度大小。
maxlength：输入框中允许输入字符的最大数。
value：输入框中的默认值
readonly：表示该框中只能显示，不能添加修改。

input类型
type=password 密码输入框
type=file 文件上传
type=hidden 隐藏域
type=buttom 按钮
radio 多选框 
checked="checked" 默认选择 
type=submit 提交按钮
eg： <input type="submit" value="搜索"> 做成一个搜索框
type=reset 重置按钮
type=checkbox 复选框
账号<input type="text" > 不写name值，服务器获取不到参数
密码<input type="password" > 不写name值，服务器获取不到参数

```
`form表单域`
```
语法：
<form action="url地址" method="提交方式" name="表单名称"> 不写name值，服务器获取不到参数
</form>

属性：
action 填url地址
method 提交方式get/post
get方式就是在浏览器上显示出来，数据小
post是不会在浏览器上显示出来的，数据大

name 表单名称
enctype 规定在发送表单数据之前如何对其进行编码

规定在发送表单数据之前如何对其进行编码。

enctype 属性可能的值 
		application/x-www-form-urlencoded 普通表单默认
		multipart/form-data 上传文件时
		text/plain 不用进行编码

```

`textarea 文本域`
```
语法：
<textarea name="message" cols="10" rows="10">文本内容</<textarea>

属性
cols 每行的字符数
rows 显示的行数
```

`select下拉列表`
```
语法：
<select>
	<option>1</option>
	<option>2</option>
	<option>3</option>
	<option selected="selected">4</option>
</select>

在option 中定义selected =” selected “时，当前项即为默认选中项。
```

`内联框架iframe`
```
语法：
<iframe src="url"></iframe>
属性：
src 必要属性，填url
height 设置高度
width 设置宽度
frameborder 删除框架，设置属性值为0即可删除

使用 iframe 作为链接的目标(traget)
链接的 target 属性必须引用 iframe 的 name 属性：
示例：
<iframe src="demo_iframe.htm" name="iframe_a"></iframe>
<p><a href="http://www.w3school.com.cn" target="iframe_a">W3School.com.cn</a></p>

```

`框架frameset`
```
语法：
<frameset rows="50%,*">
<frame src="http://www.baidu.com" scrolling="no"/>
<frame src="http://www.soso.com" />
</frameset>
frameset 不能在body内使用
frame 一般都是在frameset中使用

属性：
cols 定义框架集中列的数目和尺寸
rows 定义框架集中行的数目和尺寸eg:rows="50%,*" *就会复制前面的50%
scrolling   滚动条 eg：scrolling="no"
     auto	在需要的情况下出现滚动条（默认值）。
     yes	始终显示滚动条（即使不需要）。
     no	从不显示滚动条（即使需要）

```