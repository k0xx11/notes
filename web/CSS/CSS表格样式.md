---
title: CSS表格样式
tags: css
categories: CSS

---



## CSS表格样式

### table属性

> `border-collapse: collapse | separete | inherit; `
>
> - collapse：如果可能，边框会合并为单一的边框。忽略border-spacing和empty-cells属性。
> - separate：【默认】边框会被分开。
> - inherit：从父元素继承。

```html
<html>
    <head>
        <style type="text/css">
            table {
                border-collapse: separate;
                border-spacing: 20px 40px; 
            }
        </style>
    </head>
    <body>
        <table border="5">
            <tr>
            	<td>a_11</td>
                <td>a_12</td>
                <td>a_13</td>
            </tr>
            <tr>
            	<td>a_21</td>
                <td>a_22</td>
                <td>a_23</td>
            </tr>
            <tr>
            	<td>a_31</td>
                <td>a_32</td>
                <td>a_33</td>
            </tr>
        </table>
    </body>
</html>
```

### caption-side属性

> caption-side属性指定表标题的位置。
>
> `caption-side: top | bottom;`

### empty-cells属性

> empty-cells属性设置是否显示表格中的空单元格（仅用于“分离边框”模式）。
>
> `empty-cells: show | hide | inherit; `

```html
<html>
    <head>
        <style type="text/css">
            table {
                border-collapse: separate;
                empty-cells: hide; 
            }
        </style>
    </head>
    <body>
        <table border="5">
            <tr>
                <td>HTML</td>
                <td>CSS</td>
            </tr>
            <tr>
                <td>JavaScript</td>
                <td></td>
            </tr>
        </table>
    </body>
</html>
```

<table border="5"  border-collapse="separate" empty-cells="hide">
    <tr>
    	<td>HTML</td>
        <td>CSS</td>
    </tr>
    <tr>
    	<td>JavaScript</td>
        <td></td>
    </tr>
</table>


### table-layout属性

> table-layout属性指定如何计算表格列的宽度。
>
> `table-layout: auto | fixed; `
>
> - auto：【默认】列宽度由单元格内容设定。
> - fixed：列宽由表格宽度和列宽度设定。

```html
<html>
    <head>
        <style type="text/css">
            table {
                border-collapse: separate; 
                width: 100%; 
                border: 1px solid green; 
            }
            td {
                border: 1px solid green; 
            }
            table.auto {
                table-layout: auto; 
            }
            table.fixed {
                table-layout: fixed; 
            }
        </style>
    </head>
    <body>
        <p>
            Table-layout is set to <b>auto</b>.
        </p>
        <table class="auto">
            <tr>
            	<td width="10%">500.000.000.000.000</td>
                <td width="90%">20.000</td>
            </tr>
        </table>
        <p>
            Table-layout is set to <b>fixed</b>.
        </p>
        <table class="fixed">
            <tr>
            	<td width="10%">500.000.000.000.000</td>
                <td width="90%">20.000</td>
            </tr>
        </table>
    </body>
</html>
```





