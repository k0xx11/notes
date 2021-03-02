# HTML表格

### HTML表格标签

> \<table>
>
> \<tr>:table row（一行）
>
> \<th>:table header cell（表头）
>
> \<td>:table data cell（单元格）

```html
<table border='1'>
    <tr>
    	<td>row 1, cell 1</td>
        <td>row 1, cell 2</td>
        <td>row 1, cell 3</td>
    </tr>
    <tr>
    	<td>row 2, cell 1</td>
        <td>row 2, cell 2</td>
        <td>row 2, cell 3</td>
    </tr>
</table>
```

> \<caption>:定义表格的标题。
>
> \<colgroup>:定义表格列的组。
>
> \<col>:定义表格列的属性。
>
> \<thead>:定义表格的页眉。
>
> \<tbody>:定义表格的主体。
>
> \<tfoot>:定义表格的页脚。

> 属性
>  border 设置边框(默认为0px)
>  cellspacing 设置单元格与单元格边框之间的空白间距(默认2像素)
>  cellpadding 设置单元格内容与单元格边框之间的空白间距(默认1px)
>  width 设置表格宽度
>  height 设置表格高度
>  align 设置表格再网页中水平对齐方式



### HTML合并单元格

> rowspan属性定义单元格横跨的行数。
>
> colspan属性定义单元格横跨的列数。
>
> 跨行合并：rowspan=”合并单元格的个数”
> 跨列合并：colspan=”合并单元格的个数”

```html
<table border="1">
    <tr>
    	<td>Name:</td>
        <td>wang tsinghua</td>
    </tr>
    <tr>
    	<td rowspan="2">mail:</td>
        <td>wang__qing__hua@163.com</td>
    </tr>
    <tr>
    	<td>3372938775@qq.com</td>
    </tr>
</table>
```

```html
<table border="1">
    <tr>
    	<th>Month</th>
    	<th>Savings</th>
    </tr>
    <tr>
    	<td>January</td>
        <td>$500</td>
    </tr>
    <tr>
    	<td>February</td>
        <td>$480</td>
    </tr>
    <tr>
    	<td colspan="2">Sum:$980</td>
    </tr>
</table>
```