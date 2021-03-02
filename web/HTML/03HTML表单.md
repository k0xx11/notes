# HTML表单

> 表单是一个包含表单元素的区域。
>
> 表单元素允许用户在表单中插入内容，如：文本框、下拉列表、单选框、复选框等等。
>
> HTML表单用于收集不同类型的用户输入。

### HTML\<form>标签

> ```html
> <!-- 语法：-->
> <form action="url地址" method="提交方式" name="表单名称"> 不写name值，服务器获取不到参数
> </form>
> ```

#### action属性：

> 规定当提交表单时，向何处发送表单数据。

```html
<form action="URL">
```

> URL:
>
> - 绝对URL - 指向另一个网站（比如action="https://www.w3cschool.cn/index.html"）
> - 相对URL - 指向网站内的一个文件（如action="index.html"）

#### method属性：

> 规定如何发送表单数据。

```html
<form method="get | post">
```

> get:以查询字符串形式提交，在地址栏中能看到，长度有限制，不安全。
>
> post:以表单数据组形式提交，在地址栏中看不到，长度无限制，安全。

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <titile>use "get" to submit a form</titile>
    </head>
    <body>
        <form action="get_method.php" method="get" target="_blank">
            user: <input type="text" name="user"><br/>
            password: <input type="password" name="password"><br/>
            <input type="submit" value="sign in">
        </form>
        <p>
            click the "sign in" button,the statics in inputing area will be sent to get_method.php!
        </p>
    </body>
</html>
```

#### enctype属性：

> 规定在将表单数据发送到服务器之前如何对其进行编码。

> 注意：只有method="post"时才使用enctype属性。
>
> enctype属性值有：
>
> - application/x-www-form-urlencoded:【**普通表单默认**】在发送前对所有字符进行编码（将空格转换为"+"符号，特殊字符转换为ASCII HEX值）。
> - multipart/form-data:不对字符编码。当使用有文件上传控件的表单时，该值是必须的(**上传文件时编码**)
> - text/plain **不进行编码**



### HTML表单输入元素

> ```html
> name：同样是表示的该文本输入框名称。
> size：输入框的长度大小。
> maxlength：输入框中允许输入字符的最大数。
> value：输入框中的默认值
> readonly：表示该框中只能显示，不能添加修改。
> ```

> 输入标签\<input>
>
> 输入类型type:
>
> - 文本框（text）
> - 密码字段（password）
> - 单选按钮（radio）
> - 复选框（checkbox）
> - 提交按钮（submit）
> - 文件上传(file)
> - 隐藏域(hidden)
> - 重置按钮(reset)

> input类型
> type=password 密码输入框
> type=file 文件上传
> type=hidden 隐藏域
> type=buttom 按钮
> radio 多选框 
> checked="checked" 默认选择 
> type=submit 提交按钮
> eg： \<input type="submit" value="搜索"> 做成一个搜索框
> type=reset 重置按钮
> type=checkbox 复选框
> 账号\<input type="text" > 不写name值，服务器获取不到参数
> 密码\<input type="password" > 不写name值，服务器获取不到参数

#### 文本框

```html
<form>
    Username: <input type="text" name="username">
</form>
```

#### 密码字段

```html
<form>
    Password: <input type="password" name="pwd">
</form>
```

#### 单选按钮

```html
<form>
    Sex:<br/>
    <input type="radio" name="sex" value="male">Male<br/>
    <input type="radio" name="sex" value="female">Female<br/>
</form>
```

#### 复选框

```html
<form>
    check what you want:<br/>
    <input type="checkbox" name="Fruit" value="apple">Apple<br/>
    <input type="checkbox" name="Fruit" value="banana">Banana<br/>
</form>
```

#### 提交按钮

```html
<form action="html_form_action.php" method="post" name="myForm">
    invation: <input type="password" name="invation">
    <input type="submit" value="Corfirm">
</form>
```

### HTML特殊表单元素

#### 下拉列表select

> \<select>标签定义了下拉选项列表。
>
> \<select>中的\<option>标签定义列表中的可用选项。
>
> 在option 中定义selected =” selected “时，当前项即为默认选中项。

```html
<select>
    <option value="1">Apple</option>
    <option value="2">Banana</option>
    <option value="3">Orange</option>
    <option selected="selected">4</option>
</select>
```

#### 文本域textarea

> \<textarea>标签定义文本域。
>
> cols、rows属性分别规定了文本区域内可见的宽度和高度。
>
> cols 每行的字符数
> rows 显示的行数

```html
<textarea rows="3" cols="20">input something</textarea>
```

### HTML其他表单元素

#### \<label>

> \<label>标签定义了\<input>元素的标签，一般为输入标题。

```html
<form action="label_form.php">
    <label for="1">Male</label>
    <input type="radio" name="sex" id="1" value="male"><br/>
    <label for="2">Female</label>
    <input type="radio" name="sex" id="2" value="female"><br/>
    <input type="submit" value="I am a human.">
</form>
```

> 点击\<label>标签，浏览器会自动将焦点转移到和标签相关的表单控件上。

#### \<button>

> \<button>标签定义一个按钮。
>
> 在\<button>元素内部可以放置内容，如文本或图像。
>
> \<button>type属性值有：
>
> - submit：【默认】提交按钮
> - button：可点击按钮
> - reset：重置按钮

```html
<button type="button">a magic button!</button>
```

#### \<fieldset>

> \<fieldset>标签定义了一组相关的表单元素，并使用外框包含起来。
>
> \<legend>标签定义了\<fieldset>元素的标题。

```html
<form>
    <fieldset>
        <legend>
            Author: 
        </legend>
        Name: <input type="text"><br/><br/>
        Telephone: <input type="text"><br/><br/>
        Email: <input type="text">
    </fieldset>
</form>
```

