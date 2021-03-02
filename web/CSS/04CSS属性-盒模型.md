---
title: CSS盒子模型
tags: css
categories: CSS
---



# CSS属性-盒子模型

> 盒子模型的**组成部分** 外边距（margin）、边框（border）、内边距（padding）、内容（content）四个属性 
>
> 自身的身高 width height  
>
> 内边距 padding 
>
> 盒子边框 border 
>
> 与其他盒子的距离 margin 外边距



### margin居中

![0003](https://i.loli.net/2021/01/28/magCV87iqUvFEdb.jpg "元素的总高度")

> 遇到内容div想要居中与外部div中，可以使用`margin: 0 auto; `这样会根据内部div宽度自动填充左右两侧的margin值以达到居中效果。 

## border边框属性

> 常见的写法 border:1px solid #foo;(连写，没有规定的顺序)

> 单独属性:
> 	border-widh:1px;(定义边框粗细,常用单位px)



> `border: border-width | border-style | border-color; `

```html
<html>
    <head>
        <style type="text/css">
            p {
                padding: 10px; 
                border: 5px solid green;
            }
        </style>
    </head>
    <body>
        <p>
            I am surrounded by green, right?
        </p>
    </body>
</html>
```

### border-style属性

> `border-style: none | solid | dotted | dashed | double | groove | ridge | inset | outset | hidden; `
>
> ```css
> border-style:(定义边框样式)
> dotted 点状虚线
>             dashed（虚线）
>             solid（实线）
>             double（双实线）
> ```

```html
<html>
    <head>
        <style type="text/css">
            p.none {
                border-style: none;
            }
            p.solid {
                border-style: solid;
            }
            p.dotted {
                border-style: dotted;
            }
            p.dashed {
                border-style: dashed;
            }
            p.double {
                border-style: double;
            }
            p.groove {
                border-style: groove;
            }
            p.ridge {
                border-style: ridge;
            }
            p.inset {
                border-style: inset;
            }
            p.outset {
                border-style: outset;
            }
            p.hidden {
                border-style: hidden;
            }
        </style>
    </head>
    <body>
        <p class="none">
            none
        </p>
        <p class="solid">
            solid
        </p>
        <p class="dotted">
            dotted
        </p>
        <p class="dashed">
            dashed
        </p>
        <p class="double">
            double
        </p>
        <p class="groove">
            groove
        </p>
        <p class="ridge">
            ridge
        </p>
        <p class="inset">
            inset
        </p>
        <p class="outset">
            outset
        </p>
        <p class="hidden">
            hidden
        </p>
    </body>
</html>
```

> 可以使用以下属性为不同的边指定不同的边框：
>
> - border-top-style：上边框
> - border-right-style：右边框
> - border-bottom-style：下边框
> - border-left-style：左边框

```html
<p style="border-top-style: dashed; ">
    w3cschool
</p>
```

<p style="border-top-style: dashed; ">
    w3cschool
</p>

### border-width属性

> border-width设置边框的宽度。

```html
<html>
    <head>
        <style type="text/css">
            p.first {
                padding: 10px;
                border-style: solid;
                border-width: 2px;
            }
            p.second {
                padding: 10px;
                border-style: solid;
                border-width: 5px;
            }
        </style>
    </head>
    <body>
        <p class="first">
            w3xschool
        </p>
        <p class="second">
            w3cschool
        </p>
    </body>
</html>
```

<p style="border: 2px solid; ">w3cschool</p>

<p style="border: 5px solid; ">w3cschool</p>

### border-color属性

> 可以使用颜色名称关键词，RGB或十六进制值定义元素的边框颜色。

```html
<html>
    <head>
    	<style type="text/css">
            p.first, p.second, p.third {
                padding: 10px; 
                border-style: solid; 
                border-width: 2px; 
            }
            p.first {
                border-color: blue;
            }
            p.second {
                border-color: #FF6600;
            }
            p.third {
                border-color: rgb(0, 153, 0); 
            }
        </style>
    </head>
    <body>
        <p class="first">
            blue
        </p>
        <p class="second">
            #FF6600
        </p>
        <p class="third">
            rgb(0, 153, 0)
        </p>
    </body>
</html>
```

<p style="border: 2px solid blue; ">blue</p>

<p style="border: 2px solid #FF6600; ">#FF6600</p>

<p style="border: 2px solid rgb(0, 153, 0); ">rgb(0, 153, 0)</p>

### border综合写法

> 综合写法：border:宽度 样式 颜色;(没有顺序)



### 分别指定边框

> 没边框：border-top/bottom/left/right:none;
> 上边框
> border-top-style/width/color:;
> 下边框
> border-bottom-style/width/color:;
> 左边框
> border-left-style/width/color:;
> 右边框
> border-right-style/width/color:;
> 综合写法：border-top/bottom/left/right:宽度 样式 颜色;



### 表格的细线边框

> • 通过css属性：
> table{ border-collapse:collapse; }  
> 	• collapse 单词是合并的意思
> border-collapse:collapse; 表示相邻边框合并在一起。



## 内边距padding

> padding值：像素/厘米等长度单位、百分比
> padding:10px; 上下左右
> padding:10px 10px; 上下 左右
> padding:10px 10px 10px; 上 左右 下
> padding:10px 10px 10px 10px; 上 右 下 左（设置4个点-->顺时针方向）

> 单独属性
>
> padding-top:(上)
> padding-right:(右)
> padding-bottom:(下)
> padding-left:(左)

> • 宽度
> Element Height = content height + padding + border （Height为内容高度）
> • 高度
> Element Width = content width + padding + border （Width为内容宽度）
> 盒子的实际的大小 = 内容的宽度和高度 + 内边距 + 边框
> 当设置内边距的时候会把盒子撑大，为了保持盒子原来的大小，应该高度和宽度进行减小，根据width和height减小

> padding不影响盒子大小情况
> 如果没有给一个盒子指定宽度， 此时，如果给这个盒子指定padding， 则不会撑开盒子。



## 外边距margin

> margin值：(与padding相同)像素/厘米等长度单位、百分比

> 单独属性：与padding相同
> margin-top:(上)
> margin-right:(右)
> margin-bottom:(下)
> margin-left:(左)

> **外边距合并**：两个盒子同时设置了外边距，会进行一个外边距合并

### 块级盒子水平居中

> 可以让一个块级盒子实现水平居中必须：
> 	• 盒子必须指定了宽度（width）
> 	• 然后就给左右的外边距都设置为auto，
> 实际工作中常用这种方式进行网页布局，示例代码如下：
> .header{ width:960px; margin:0 auto;}
> 常见的写法，以下下三种都可以。
> 1.margin-left: auto; margin-right: auto;
> 2.margin: auto;
> 3.margin: 0 auto;

### 文字居中和盒子居中区别

> 1. 盒子内的文字水平居中是 text-align: center, 而且还可以让 行内元素和行内块居中对齐
> 2. 块级盒子水平居中 左右margin 改为 auto
> text-align: center; /*  文字 行内元素 行内块元素水平居中 */
> margin: 10px auto;  /* 块级盒子水平居中  左右margin 改为 auto 就阔以了 上下margin都可以 */
> margin
> margin:10px  上下左右都会腾出10px出来
> margin:0px auto; 居中

## 插入图片和背景图片的区别

> 插入图片 我们用的最多 比如产品展示类 移动位置只能靠盒模型 padding margin
> 背景图片我们一般用于小图标背景 或者 超大背景图片 背景图片 只能通过 background-position
>  img {  
>         width: 200px;/* 插入图片更改大小 width 和 height */
>         height: 210px;
>         margin-top: 30px;  /* 插入图片更改位置 可以用margin 或padding  盒模型 */
>         margin-left: 50px; /* 插入当图片也是一个盒子 */
>     }
> div {
>         width: 400px;
>         height: 400px;
>         border: 1px solid purple;
>         background: #fff url(images/sun.jpg) no-repeat;
>         background-position: 30px 50px; /* 背景图片更改位置 我用 background-position */
>     }



## 清除元素默认的内外边距(重要)

> 为了更灵活方便地控制网页中的元素，制作网页时，我们需要将元素的默认内外边距清除
> 代码：
> * {
>    padding:0;         /* 清除内边距 */
>    margin:0;          /* 清除外边距 */
> }
> 注意：
> 行内元素为了照顾兼容性， 尽量只设置左右内外边距， 不要设置上下内外边距。



## 外边距合并

> 使用margin定义块元素的垂直外边距时，可能会出现外边距的合并。
> (1). 相邻块元素垂直外边距的合并
> 当上下相邻的两个块元素相遇时，如果上面的元素有下外边距margin-bottom
> 下面的元素有上外边距margin-top，则他们之间的垂直间距不是margin-bottom与margin-top之和
> 取两个值中的较大者这种现象被称为相邻块元素垂直外边距的合并（也称外边距塌陷）。
> 解决方案：尽量给只给一个盒子添加margin值。
>
> (2). 嵌套块元素垂直外边距的合并（塌陷）
> 对于两个嵌套关系的块元素，如果父元素没有上内边距及边框
> 父元素的上外边距会与子元素的上外边距发生合并
> 合并后的外边距为两者中的较大者
> 解决方案：
> 1. 可以为父元素定义上边框。
> 2. 可以为父元素定义上内边距
> 3.可以为父元素添加overflow:hidden。



## 盒子模型布局稳定性

> • 学习完盒子模型，内边距和外边距，什么情况下用内边距，什么情况下用外边距？
> 大部分情况下是可以混用的。 就是说，你用内边距也可以，用外边距也可以。 你觉得哪个方便，就用哪个。
> 我们根据稳定性来分，建议如下：
> 按照 优先使用 宽度 （width） 其次 使用内边距（padding） 再次 外边距（margin）。
>   width >  padding  >   margin   
> • 原因：
> 	• margin 会有外边距合并 还有 ie6下面margin 加倍的bug（讨厌）所以最后使用。
> 	• padding 会影响盒子大小， 需要进行加减计算（麻烦） 其次使用。
> width 没有问题（嗨皮）我们经常使用宽度剩余法 高度剩余法来做。



## 去掉列表的默认样式

> 无序和有序列表前面默认的列表样式，在不同浏览器显示效果不一样，而且也比较难看，所以，我们一般上来就直接去掉这些列表样式就行了。 
>
> 代码如下li { list-style: none; }



## 扩展

### 1.圆角边框(CSS3)

> • 语法：
> border-radius:length;  
> • 其中每一个值可以为 数值或百分比的形式。
> • 技巧： 让一个正方形 变成圆圈
> border-radius: 50%;
> 以上效果图矩形的圆角， 就不要用 百分比了，因为百分比会是表示高度和宽度的一半。
> 而我们这里矩形就只用 
> 用 高度的一半就好了。精确单位。
> eg:border-radius:10px;

### 2.盒子阴影

> • 语法:
> box-shadow:水平阴影 垂直阴影 模糊距离（虚实）  阴影尺寸（影子大小）  阴影颜色  内/外阴影；
> • 前两个属性是必须写的。其余的可以省略。
> • 外阴影 (outset) 是默认的 但是不能写 想要内阴影可以写 inset
> div {
>             width: 200px;
>             height: 200px;
>             border: 10px solid red;
>             /* box-shadow: 5px 5px 3px 4px rgba(0, 0, 0, .4);  */
>             /* box-shadow:水平位置 垂直位置 模糊距离 阴影尺寸（影子大小） 阴影颜色  内/外阴影； */
>             box-shadow: 0 15px 30px  rgba(0, 0, 0, .4);
> }



## CSS书写规范

开始就形成良好的书写规范，是你专业的开始。

### 空格规范

>  【强制】 选择器 与 {} 之间必须包含空格。

```
示例：
.selector {
}
【强制】 属性名 与之后的 : 之间不允许包含空格， : 与 属性值 之间必须包含空格。
示例：
font-size: 12p
```



### 选择器规范

> 【强制】 并集选择器，每个选择器声明必须独占一行。

```
示例：
/* good */
.post,
.page,
.comment {
    line-height: 1.5;
}
/* bad */
.post, .page, .comment {
    line-height: 1.5;
}
```

> 【建议】 一般情况情况下，选择器的嵌套层级应不大于 3 级，位置靠后的限定条件应尽可能精确。

```
示例：
/* good */
#username input {}
.comment .avatar {}
/* bad */
.page .header .login  input {}
.comment div * {}
```



### 属性规范

> 【强制】 属性定义必须另起一行。

```
示例：
/* good */
.selector {
    margin: 0;
    padding: 0;
}
/* bad */
.selector { margin: 0; padding: 0; }
```



> 【强制】 属性定义后必须以分号结尾。

```
示例：
/* good */
.selector {
    margin: 0;
}
/* bad */
.selector {
    margin: 0
}
```

