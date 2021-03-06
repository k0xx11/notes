---
title: CSS定位与布局
tags: css
categories: CSS
---

# CSS定位与布局

## 定位

### CSS 布局的三种机制

网页布局的核心 —— 就是**用 CSS 来摆放盒子位置**。

> CSS 提供了 **3 种机制**来设置盒子的摆放位置，分别是**普通流**、**浮动**和**定位**，其中：
>
> **普通流**（**标准流**）
>
> **浮动**
>
> - 让盒子从普通流中**浮**起来 —— **让多个盒子(div)水平排列成一行**。
>
> **定位**
>
> - 将盒子**定**在某一个**位**置 自由的漂浮在其他盒子的上面 —— CSS     离不开定位，特别是后面的 js 特效。

### 定位详解

> 定位也是用来布局的，它有两部分组成：
>
> 定位 = 定位模式 + 边偏移

### 边偏移

> 简单说， 我们定位的盒子，是通过边偏移来移动位置的。

在 CSS 中，通过 top、bottom、left 和 right 属性定义元素的**边偏移**：（方位名词）

| 边偏移属性 | 示例         | 描述                                                     |
| ---------- | ------------ | -------------------------------------------------------- |
| top        | top: 80px    | **顶端**偏移量，定义元素相对于其父元素**上边线的距离**。 |
| bottom     | bottom: 80px | **底部**偏移量，定义元素相对于其父元素**下边线的距离**。 |
| left       | left: 80px   | **左侧**偏移量，定义元素相对于其父元素**左边线的距离**。 |
| right      | right: 80px  | **右侧**偏移量，定义元素相对于其父元素**右边线的距离**   |

> 定位的盒子有了边偏移才有价值。 一般情况下，凡是有定位地方必定有边偏移



### 定位模式 (position)

> 在 CSS 中，通过 position 属性定义元素的**定位模式**，

```
语法如下：

选择器 { position: 属性值; }
```

> 定位模式是有不同分类的，在不同情况下，我们用到不同的定位模式。

| 值       | 语义         |
| -------- | ------------ |
| static   | **静态**定位 |
| relative | **相对**定位 |
| absolute | **绝对**定位 |
| fixed    | **固定**定位 |

#### 静态定位static

> - **静态定位**是元素的默认定位方式，无定位的意思。它相当于 border 里面的none， 不要定位的时候用。
> - 静态定位     按照标准流特性摆放位置，它没有边偏移。
> - 静态定位在布局时我们几乎不用的

#### 相对定位relative(重点)

> **相对定位**是元素**相对**于它 原来在标准流中的位置 来说的。（自恋型）

> 相对定位的特点：（务必记住）
>
> - 相对于     自己原来在标准流中位置来移动的
> - 原来**在标准流的区域继续占有**，后面的盒子仍然以标准流的方式对待它。

#### 绝对定位absolute(重要)

> **绝对定位**是元素以带有定位的父级元素来移动位置 （拼爹型）
>
> **完全脱标** —— 完全不占位置；
>
> **父元素没有定位**，则以**浏览器**为准定位（Document 文档）。

> **父元素要有定位**
>
> - 将元素依据最近的已经定位（绝对、固定或相对定位）的父元素（祖先）进行定位。
>
> <img src="./images/06_绝对定位_父级有定位.png" width="700" />

> 绝对定位的特点：（务必记住）
>
> - 绝对是以带有定位的父级元素来移动位置     （拼爹型） 如果父级都没有定位，则以浏览器文档为准移动位置
> - 不保留原来的位置，完全是脱标的。
>
> 因为绝对定位的盒子是拼爹的，所以要和父级搭配一起来使用。

##### 定位口诀 —— 子绝父相

> 刚才咱们说过，绝对定位，要和带有定位的父级搭配使用，那么父级要用什么定位呢？
>
> **子绝父相** —— **子级**是**绝对**定位，**父级**要用**相对**定位。
>
> **子绝父相**是使用绝对定位的口诀，要牢牢记住！

#### 固定定位fixed(重要)

> **固定定位**是**绝对定位**的一种特殊形式： （认死理型） 如果说绝对定位是一个矩形 那么 固定定位就类似于正方形
>
> **完全脱标** —— 完全不占位置；
>
> 只认**浏览器的可视窗口** —— 浏览器可视窗口 + 边偏移属性 来设置元素的位置；
>
> - 跟父元素没有任何关系；单独使用的
> - 不随滚动条滚动。



> **子绝父相** —— **子元素**使用**绝对定位**，**父元素**使用**相对定位**；
>
> **与浮动的对比**：
>
> - **绝对定位**：脱标，**利用边偏移指定准确位置**；
> - **浮动**：脱标，不能指定准确位置，**让多个块级元素在一行显示**。



#### 定位(position)的扩展

##### 绝对定位的盒子居中

> **注意**：**绝对定位/固定定位的盒子**不能通过设置 margin: auto 设置**水平居中**。
>
> 在使用**绝对定位**时要想实现水平居中,
>
> left: 50%;：让**盒子的左侧**移动到**父级元素的水平中心位置**；
>
> margin-left: -100px;：让盒子**向左**移动**自身宽度的一半**。



##### 堆叠顺序z-index属性

> z-index属性指定元素的堆栈顺序（通过z-index的值可以决定那个元素应该放置在其他元素的前面或后面）。
>
> 当元素位于正常流程顺序之外时（受position等属性影响时），它们可以重叠于其他元素。

> 在使用**定位**布局时，可能会**出现盒子重叠的情况**。
>
> 加了定位的盒子，默认**后来者居上**， 后面的盒子会压住前面的盒子。
>
> 应用 z-index 层叠等级属性可以**调整盒子的堆叠顺序**

```html
<html>
    <head>
        <style type="text/css">
            .blue {
                background-color: #8ec4d0; 
                margin-bottom: 15px; 
                width: 120px; 
                height: 120px; 
                color: #fff; 
            }
            .red {
                background-color: #ff4d4d; 
                position: relative; 
                width: 120px; 
                height: 120px; 
                color: #fff; 
                margin: -50px 50px; 
            }
        </style>
    </head>
    <body>
        <div class="blue">
            blue<br/>(w3cschool)
        </div>
        <div class="red">
            red<br/>(w3cschool)
        </div>
    </body>
</html>
```

<div style="background-color: #8ec4d0; 
                margin-bottom: 15px; 
                width: 120px; 
                height: 120px; 
                color: #fff; ">
    blue<br/>(w3cschool)
</div>


<div style="background-color: #ff4d4d; 
                position: relative; 
                width: 120px; 
                height: 120px; 
                color: #fff; 
                margin: -50px 50px; ">
    red<br/>(w3cschool)
</div>




> 红框与蓝框重叠，红框位于蓝框上方，因为红框是后加载的。设置z-index属性可以改变这个顺序。

```html
<html>
    <head>
        <style type="text/css">
            .blue {
                background-color: #8ec4d0; 
                margin-bottom: 15px; 
                width: 120px; 
                height: 120px; 
                color: #fff; 
                z-index: 3; 
            }
            .red {
                background-color: #ff4d4d; 
                position: relative; 
                width: 120px; 
                height: 120px; 
                color: #fff; 
                margin: -50px 50px; 
                z-index: 2; 
            }
        </style>
    </head>
    <body>
        <div class="blue">
            blue<br/>(w3cschool)
        </div>
        <div class="red">
            red<br/>(w3cschool)
        </div>
    </body>
</html>
```

<div style="background-color: #8ec4d0; 
                margin-bottom: 15px; 
                width: 120px; 
                height: 120px; 
                color: #fff; 
                z-index: 3;">
    blue<br/>(w3cschool)
</div>


<div style="background-color: #ff4d4d; 
                position: relative; 
                width: 120px; 
                height: 120px; 
                color: #fff; 
                margin: -50px 50px; 
                z-index: 2; ">
    red<br/>(w3cschool)
</div>




> z-index仅适用于定位元素absolute, relative, fixed!

> z-index 的特性如下：
>
> **属性值**：**正整数**、**负整数**或 **0**，默认值是 0，数值越大，盒子越靠上；
>
> 如果**属性值相同**，则按照书写顺序，**后来居上**；
>
> **数字后面不能加单位**



> **注意**：z-index 只能应用于**相对定位**、**绝对定位**和**固定定位**的元素，其他**标准流**、**浮动**和**静态定位**无效



##### 定位改变display属性

> 前面我们讲过， display 是 显示模式， 可以改变显示模式有以下方式:
>
> - 可以用inline-block     转换为行内块
> - 可以用浮动 float     默认转换为行内块（类似，并不完全一样，因为浮动是脱标的）
> - 绝对定位和固定定位也和浮动类似，     默认转换的特性 转换为行内块。
>
> 所以说， 一个行内的盒子，如果加了**浮动**、**固定定位**和**绝对定位**，不用转换，就可以给这个盒子直接设置宽度和高度等。



> **同时注意：**
>
> 浮动元素、绝对定位(固定定位）元素的都不会触发外边距合并的问题。 （我们以前是用padding border overflow解决的）
>
> 也就是说，我们给盒子改为了浮动或者定位，就不会有垂直外边距合并的问题了。



## 圆角矩形设置4个角

> 圆角矩形可以为4个角分别设置圆度， 但是是有顺序的
>
> border-top-left-radius:20px;
>  border-top-right-radius:20px;
>  border-bottom-right-radius:20px;
>  border-bottom-left-radius:20px;



> - 如果4个角，数值相同
>             border-radius: 15px;
> - 里面数值不同，我们也可以按照简写的形式，具体格式如下:
>
> border-radius: 左上角 右上角 右下角 左下角;
>
> 还是遵循的顺时针。



### **注意**：

> **边偏移**需要和**定位模式**联合使用，**单独使用无效**；
>
> top 和 bottom 不要同时使用；
>
> left 和 right 不要同时使用。



##  网页布局总结

一个完整的网页，有标准流 、 浮动 、 定位 一起完成布局的。每个都有自己的专门用法。

1). 标准流

可以让盒子上下排列 或者 左右排列的

2). 浮动

可以让多个块级元素一行显示 或者 左右对齐盒子 浮动的盒子就是按照顺序左右排列

3). 定位

定位最大的特点是有层叠的概念，就是可以让多个盒子 前后 叠压来显示。 但是每个盒子需要测量数值。