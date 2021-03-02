---
title: CSS基础
tags: css
categories: CSS
---
# CSS基础

## CSS介绍

> CSS指**层叠样式表**（Cascading Style Sheets）
>
> 样式定义如何显示[HTML元素](../HTML/01基础.md)
>
> 样式通常存储在样式表中
>
> 把样式添加到HTML4.0中，是为了解决内容与表现分离的问题
>
> 外部样式表可以极大提高工作效率
>
> 外部样式表通常存储在CSS文件中
>
> 多个样式定义可层叠为一个

### 行内样式表

> 内联CSS也称为行内CSS/行级CSS，它直接在标签内部引用

```html
语法:
<标签名 style="属性1:属性值1; 属性2:属性值2; 属性3:属性值3;"> 内容 </标签名>

eg:<div style="color: red; font-size: 18px;">hello,worls</div>
```

<p style="color:red; background-color:blue; ">
    Hi!I am a text!
</p>

### 内部样式表

> 内部样式表定义在\<head>的\<style>元素中

```html
是将CSS代码集中写在HTML文档的head头部标签中，并且用style标签定义每行结束都有分号";"
语法:
<head>
<style type="text/CSS">
    选择器（选择的标签） { 
      属性1: 属性值1;
      属性2: 属性值2; 
      属性3: 属性值3;
    }
</style>
</head>

eg:
<head>
<style>
     div {
         color: red;
         font-size: 12px;
     }
</style>

</head>
```

### 外部样式

> CSS样式表存储在同一个后缀名为.css的拓展文件中。然后通过HTML标签\<link>在HTML页面的\<head>部分将CSS文件引入。

```html
link标签需要放到head头部标签里,所有样式都放在一个css文件
语法:<link rel="stylesheet" type="text/css" href="css文件路径">

eg: <link rel="stylesheet" type="text/css" href="mystyle.css">
```

```CSS
/* CSS part */
p {
    color:white;
    background-color:gray;
}
```



### import 引用样式(用的比较少)

> ```html
> 引用样式:
> @import url(cssimport.css);
> 
> url()括号里面写引用样式的文件路径
> ```



### CSS语法

> CSS是由浏览器解释的样式规则，然后应用于文档中相应的元素。
>
> 样式规则由三个部分：**选择器**，**属性**和**值**。`Selector { Property: Value; }`

```css
h1{color:red;font-size:14px;}
h1是选择器 color是属性 red是值

用花括号包围声明
```



### CSS注释

> ```css
> css的注释语法:
> /*css注释*/
> ```

