---
title: CSS链接与鼠标样式
tags: css
categories: CSS
---

## CSS链接样式

> 链接可以使用任何CSS属性（如color，font-family，background等）来设置样式。
>
> 依以下顺序依次设置：
>
> - a: link 定义普通的、未被访问的链接。
> - a: visited 定义访问后的链接。
> - a: hover 定义鼠标指针位于连接上方时刻。
> - a: active 定义链接被点击的时刻。

```html
<html>
    <head>
        <style type="text/css">
            a: hover {
                color: red; 
            }
        </style>
    </head>
    <body>
        <p>
            <a href="http://127.0.0.1" target="_blank">here is 80 port in your computer</a>
        </p>
    </body>
</html>
```

<p><a a:hover="red" href="http://127.0.0.1" target="_blank">here is 80 port in your computer</a></p>

### 文本链接的样式

> `text-decoration: none; `可以删除下划线。
>
> `border: none; `从包含连接的图像中删除边框。
>
> `outline: none; `删除IE中点击链接行上的虚线边框。

## CSS自定义鼠标光标样式

### cursor参数值

> cursor属性规定要显示的光标的类型（形状）。该属性定义了鼠标指针放在一个元素边界范围内时所用的光标形状。

\![0006]\(img/0006.jpg)

![0006](https://i.loli.net/2021/01/29/ybWl2Pa9GdMpgJL.jpg)

```html
<span style="cursor: help; ">need help?</span>
```

<span style="cursor: help; ">need help?</span>

```html
<html>
    <body>
        <p style="cursor: auto; ">
            The cursor of this paragraph has been set to auto.
        </p>
        <p style="cursor: move; ">
            The cursor of this paragraph has been set to move.
        </p>
        <p style="cursor: wait; ">
            The cursor of this paragraph has been set to wait.
        </p>
        <p style="cursor: pointer; ">
            The cursor of this paragraph has been set to pointer.
        </p>
        <p style="cursor: no-drop; ">
            The cursor of this paragraph has been set to no-drop.
        </p>
        <p style="cursor: s-resize; ">
            The cursor of this paragraph has been set to s-resize.
        </p>
        <p style="cursor: crosshair; ">
            The cursor of this paragraph has been set to crosshair.
        </p>
        <p style="cursor: text; ">
            The cursor of this paragraph has been set to text.
        </p>
        <p style="cursor: progress; ">
            The cursor of this paragraph has been set to progress.
        </p>
        <p style="cursor: not-allowed; ">
            The cursor of this paragraph has been set to not-allowed.
        </p>
    </body>
</html>
```