---
title: CSS块行行内块级元素行高
tags: css
categories: CSS
---

## 块级元素block

> ```
> 常见的块元素有<h1>~<h6>、<p>、<div>、<ul>、<ol>、<li>等，其中<div>标签是最典型的块元素。
> 特点：
> （1）比较霸道，自己独占一行
> （2）高度，宽度、外边距以及内边距都可以控制。
> （3）宽度默认是容器（父级宽度）的100%
> （4）是一个容器及盒子，里面可以放行内或者块级元素。
> ```

> ```
> 块级元素即使设置了宽度也是独占一行，块级元素可以设置margin、padding属性；
> 
> 块级元素（block element）
> 
> address 地址
> center 举中对齐块
> div- 常用块级容易
> dl 定义列表
> form 交互表单 （只能用来容纳其它块元素）
> h标签
> hr 水平分隔线
> ol 无需列表
> ul有序列表
> p 段落
> pre 格式化文本
> ```





## 行内元素inline

> ```html
> 常见的行内元素有<a>、<strong>、<b>、<em>、<i>、<del>、<s>、<ins>、<u>、<span>等，
> 其中<span>标签最典型的行内元素。有的地方也成内联元素
> ```
>
> 特点：
> （1）相邻行内元素在一行上，一行可以显示多个。
> （2）高、宽直接设置是无效的。
> （3）默认宽度就是它本身内容的宽度。
> （4）行内元素只能容纳文本或则其他行内

```
行内元素：

`a` - 锚点,b - 粗体(不推荐),`br`- 换行,`code` - 计算机代码(在引用源码的时候需要)
`em` - 强调,i - 斜体
`img` - 图片（特殊的内联元素，同时是内联替换元素，替换元素可以设置宽高）
当图片和DIV在一起时，图片周围会出现margin现象，即元素不重合贴在一起，为了解决这个问题，设置img的css为
```

> ```css
>{margin：0；display：block；border：0px}
> ```
> 



> ```
>`input` - 输入框,label - 表格标签,select - 项目选择,strong - 粗体强调,`textarea` - 多行文本输入框
> u - 下划线,var - 定义变量
> 
> 替换元素有如下：（和img一样的设置方法）
> 
><img>、<input>、<textarea>、<select>
> 
> <object>都是替换元素，这些元素都没有实际的内容
> 
>
> 行内元素的margin、padding属性很奇怪，水平方向的padding-left、padding-rigtht、margin-left、padding-right都会产生边距效果，但是竖直方向的padding-top、padding-bottom、margin-top、margin-bottom却不产生边距效果。
> ```



## 行内块元素inline-block

> ```
> 在行内元素中有几个特殊的标签——<img />、<input />、<td>，可以对它们设置宽高和对齐属性，有些资料可能会称它们为行内块元素。
> ```
>
> 特点：
> （1）和相邻行内元素（行内块）在一行上,但是之间会有空白缝隙。一行可以显示多个
> （2）默认宽度就是它本身内容的宽度。
> （3）高度，行高、外边距以及内边距都可以控



## 标签显示模式转换display

```
块转内：display:inline;
行内转块:display:block;
块、行内元素转换为行内块：display:inline-block;
display:none; 不显示
```





