---
title: CSS边框属性
tags: css
categories: CSS
---

## CSSborder属性

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

> border-width设置边框的宽度，定位px

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

