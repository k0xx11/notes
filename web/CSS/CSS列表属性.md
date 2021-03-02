---
title: CSS列表属性
tags: css
categories: CSS

---

## CSS列表样式

### list-style-type属性

> list-style-type属性允许我们设置不同的列表项标记。
>
> - none：无标记。在使用ul/ol进行一些网页布局（如菜单）时候较常使用。取消原来的样式
> - disc：【默认】实心圆。
> - circle：空心圆。
> - square：实心方块。
> - decimal：数字。
> - decimal-leading-zero：0开头的数字（01， 02， 03等）。
> - lower-roman：小写罗马数字。
> - upper-roman：大写罗马数字。
> - lower-alpha：小写英文字母。
> - upper-alpha：大写英文字母。

> 取值:disc | circle | square | decimal | decimal-leading-zero | lower-roman | upper-roman | lower-greek | lower-latin | upper-latin | armenian | georgian | lower-alpha 
>
> | upper-alpha | none | inherit
>
>      disc: 点
>      circle: 圆圈
>      square: 正方形
>      decimal: 数字
>      decimal-leading-zero: 十进制数，不足两位的补齐前导0，例如: 01, 02, 03, ..., 98, 99
>      lower-roman: 小写罗马文字，例如: i, ii, iii, iv, v, ...
>      upper-roman: 大写罗马文字，例如: I, II, III, IV, V, ...
>      lower-greek: 小写希腊字母，例如: α(alpha), β(beta), γ(gamma), ...
>      lower-latin: 小写拉丁文，例如: a, b, c, ... z
>      upper-latin: 大写拉丁文，例如: A, B, C, ... Z
>      armenian: 亚美尼亚数字
>      georgian: 乔治亚数字，例如: an, ban, gan, ..., he, tan, in, in-an, ...
>      lower-alpha: 小写拉丁文，例如: a, b, c, ... z
>      upper-alpha: 大写拉丁文，例如: A, B, C, ... Z
>      none: 无(取消所有的list样式)
>      inherit:继承

### list-style-image属性

> list-style-image属性设置图像为列表中的项目标记。

### list-style-position属性

> list-style-position属性指定标记框的位置。
>
> `list-style-position: inside | outside; `

```html
<html>
    <head>
        <style type="text/css">
            ul {
                list-style-image: url("img/0005.ico"); 
                list-style-position: inside; 
            }
        </style>
    </head>
    <body>
        <p>
            以下列使用list-style-position: <b>inside</b> 属性。
        </p>
        <ul>
            <li>w3cschool01</li>
            <li>w3cschool02</li>
            <li>w3cschool03</li>
        </ul>
    </body>
</html>
```

### list-style属性

> `list-style: list-style-type list-style-position list-style-image; `

### inherit属性

> 规定应该从父元素继承 list-style 属性的值

