---
title: CSS选择器
tags: css
categories: CSS
---
# CSS选择器

> note: 
>
> - 据点“.”表示class（可理解为后缀）
> - 井号“#”表示id
> - 空格“ ”表示后代
> - 大于号“>”表示子代

## 标签选择器

> **标签选择器**是指用**HTML标签名**作为选择器，按**标签名称**分类，为页面中某一类标签制定统一的CSS样式。(元素选择器)

```html
语法:
标签名{属性1:属性值1; 属性2:属性值2; 属性3:属性值3; } 

实例:
<style type="text/css">
		p {
			color: green;
		}

		div {
			color: yellow;
		}
	</style>

作用：
标签选择器 可以把某一类标签全部选择出来 比如所有的div标签 和 所有的 span标签
```

## class选择器(使用次数多)

> **class选择器（类型选择器）**通过绑定HTML元素上已设置的class标签进行设置对应的CSS样式。
>
> class前加.号

```html
类选择器使用“.”（英文点号）进行标识，后面紧跟类名.

语法:
	• 类名选择器
.类名  {   
    属性1:属性值1; 
    属性2:属性值2; 
    属性3:属性值3;     
}
eg:.p {
			color:red;
			font-size:20px;
		}

		.div {
			color: green;
			font-size:20px;
		}

	• 标签
<p class='类名'></p>
eg:<p class="p">hello,world</p>

类选择器-多类名(类名旁边空格类名)
eg: <p class='类名 类名 类名'>多类名</p>
```

## id选择器

> **id选择器**通过绑定HTML元素上已设置的唯一id标签进行设置对应的CSS样式。
>
> id前加#号。

```html
语法:
id选择器
#id名 {属性1:属性值1; 属性2:属性值2; 属性3:属性值3; }
标签
<p id="id名"></p>

eg:
#e{
			color: green;
			font-size:18px;
		}
		#o {
			color: red;
			background: green;
		}
<p id="o">11111111</p>
<div id="e">222222222</div>
```

> id属性在文档内必须是唯一的。
>
> 不能使用数字开头的id属性！

## 类选择器和id选择器的区别

```
• W3C标准规定，在同一个页面内，不允许有相同名字的id对象出现，但是允许相同名字的class。
	• 类选择器（class） 好比人的名字， 是可以多次重复使用的， 比如 张伟 王伟 李伟 李娜
	• id选择器 好比人的身份证号码， 全中国是唯一的， 不得重复。 只能使用一次。
id选择器和类选择器最大的不同在于 使用次数上。
```



## 通配符选择器

> 选择所有的元素,给他使用样式

```html
语法:
* { 属性1:属性值1; 属性2:属性值2; 属性3:属性值3; }

eg:
* {
			color: red;
			font-size:100px;
		}

使用通配符选择器定义CSS样式，清除所有HTML标记的默认边距
* {
  margin: 0;                    /* 定义外边距*/
  padding: 0;                   /* 定义内边距*/
}
```



## 复合选择器

## 后代选择器(重点)

> **后代选择器**选择某个父级下的所有子级，并针对该子级设置CSS样式。
>
> 作用:用来选择元素或元素组的子孙后代
>
> 父元素与子元素间加空格。

```html
语法：
父级 子级 孙子 {属性:属性值;属性:属性值;}
eg: .wangsicong ul li {color:red;font-size:16px;}
<div class="wangsicong">
	<ul>
		<li>王可可</li>
		<li>王可可</li>
		<li>王可可</li>
	</ul>
</div>
```

> 后代标签允许跨代影响。如：`.grandpa .baby {color:#808000;}`会对`<div class="grandpa"><div class="anyone"><p class="baby">I am brown.</p></div></div>`有作用。
>
> 不同的后代的标签可能会对同一处地方产生作用，此时谁的定义在后面便由谁！

## 子元素选择器

> **子元素选择器**与后代选择器类似，但不允许跨代影响。
>
> 作用:子元素选择器只能选择作为某元素子元素(亲儿子)的元素。
>
> 父元素与子元素间加 > 号。

```html
• 语法：
父级 子级{属性:属性值;属性:属性值;}
div>strong{color:red;font-size:14px;}
eg:
<div>
	<strong>儿子</strong>
	<strong>儿子</strong>
	<strong>儿子</strong>
</div>
```



## 交集选择器

> 作用:交集选择器 既是p标签 又是.red类选择器的关系

```html
语法:
标签选择器 类选择器{属性1:属性值1; 属性2:属性值2;}
p.red{color:red;}
<p class="red">红色</p>
<p class="red">红色</p>
<p class="red">红色</p>
```



## 并集选择器(重点)

```html
语法:
标签选择器,标签选择器,类选择器{属性1:属性值1;属性2:属性值2;}
eg:
p,div,.red{color:red;font-size:100xp;}
<p>我和你</p>
<p>我和你</p>
<p>我和你</p>
<span>我和你</span>
<span>我和你</span>
<span>我和你</span>
<div class="red">我和你</div>
```



## 链接伪类选择器(重点)

> 作用：用于向某些选择器添加特殊的效果。比如给链接添加特殊效果， 比如可以选择 第1个，第n个元素

```css
伪类选择器 eg: link:

按照 lvha 的顺序写

a:link /* 未访问的链接 */
a:visited /* 已访问的链接 */
a:hover /* 鼠标移动到链接上 */
a:active /* 选定的链接 */


• 因为a链接浏览器具有默认样式，所以我们实际工作中都需要给链接单独指定样式。
• 实际工作开发中，我们很少写全四个状态，一般我们写法如下：
a {   /* a是标签选择器  所有的链接 */
            font-weight: 700;
            font-size: 16px;
            color: gray;
}
a:hover {   /* :hover 是链接伪类选择器 鼠标经过 */
            color: red; /*  鼠标经过的时候，由原来的 灰色 变成了红色 */
}
```



## 相邻选择器

> **相邻选择器**选中对应元素的下一个兄弟元素。

```html
<html>
    <head>
        <style type="text/css">
            #w3cschool+p {
                color:red;
            }
            #error+p {
                color:blue;
            }
        </style>
    </head>
    <body>
        <div id="w3cschool">
            coding...
        </div>
        <p>
            coding after id w3cschool...
        </p>
        <p>
            coding after a long time since learning w3cschool...
        </p>
        <!-- coming is a intentional error -->
        <div id="error">
            coding when there is a bug...
        </div>
        <div>
            <!-- this p is not next to id error -->
            <p>
                coding when i found the bug...
            </p>
        </div>
    </body>
</html>
```

## 属性选择器

> **属性选择器**检索HTML页面中符合所设置的属性条件的元素。
>
> 属性选择器通过[]设置被选元素的属性条件。其中包含**属性名称**，后跟**可选条件**以匹配属性的值。如`img[alt] {width:80px; height:90px; }`将选择HTML页面中所有包含了alt属性的img元素并为其设置CSS样式。
>
> 属性选择器分两类：
>
> - 存在和值属性选择器（匹配精确的属性值）
>
>   - [attr]：包含attr属性的所有元素
>
>     `div[id] {color:red; }`
>
>   - [attr=val]：选择属性attr被赋值为val的所有元素
>
>     `a[href="http://testftp002.tech:404"] {color:red; }`
>
>   - [attr~=val]：仅选择属性attr中，属性值包含val的所有元素
>
>     `div[class~="w3cschool"] {color:red; }`
>
> - 子串值属性选择器（伪正则选择器）
>
>   - [attr|=val]：选择attr属性的值是val或值以val-开头的元素
>   - [attr^=val]：选择attr属性的值以val开头（包括val）的元素
>   - [attr$=val]：选择attr属性的值以val结尾（包括val）元素
>   - [attr*=val]：选择attr属性的值中包含字符串val的元素

```html
<html>
    <head>
        <style type="text/css">
            *[class] {
                color:red;
            }
            /* class中以w3cschool-开头或等于w3cschool的所有元素 */
            *[class|="w3cschool"] {
                color:green;
            }
            /* class中以w3cschool开头（包括w3cschool）的所有p元素 */
            p[class$="w3cschool"] {
                color:blue;
            }
        </style>
    </head>
    <body>
        <div class="w3cschool-programmer">
            程序猿
        </div>
        <div class="w3cschool_product">
            产品鲸鲤
        </div>
        <p class="designer-w3cschool">
            设计狮
        </p>
        <p>
            单身狗
        </p>
    </body>
</html>
```

## 选择器分组

> **选择器分组**通过逗号“,”将需要复用同一套样式的多个元素进行分隔。

```html
<html>
    <head>
        <style type="text/css">
            a, p, div {
                color:red;
            }
        </style>
    </head>
    <body>
        <div id="w3cschool">
            i am a div.
        </div><br/>
        <p>
            i am a p.
        </p><br/>
        <a>i am a a.</a><br/>
        <span>i am a span.</span>
    </body>
</html>
```