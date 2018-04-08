---
title: Notes-HTML
tags:
  - html
  - 学习笔记
categories: Web
comments: true
abbrlink: 1b9dba06
date: 2018-04-03 22:36:54
---

# HTML

HTML超文本标记语言

<!-- more -->

## HTML基本结构

HTML注释：`<!-- HTML注释格式 -->`

```html
<!-- HTML注释格式 -->
<!-- 基本HTML文档格式 -->
<html>
<head>
	<title>文档标题</title>
</head>
<body>
	文档主体内容
</body>
</html>
```

```html
<!-- 标准HTML文档格式 -->
<!DOCTYPE html>  <!-- H5文档类型=html -->
<html lang="en">  <!-- language=English -->
<head>
    <meta charset="UTF-8"> <!-- 字符集 -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>
    文档主体
</body>
</html>
```
## HTML-头部标签

### meta标签-元信息

1. meta标签：提供页面元信息，位于`<head></head>`中。

- `<meta name="" content=""/>`
- `<meta http-equiv="" content=""/>`

2. meta标签属性：以**键值对**形式传递

- name:content
- http-equiv:content

| `<meta/>`属性 | 值                                                           | 描述                                       |
| ------------- | ------------------------------------------------------------ | ------------------------------------------ |
| content       | some_text                                                    | 定义与 http-equiv 或 name 属性相关的元信息 |
| name          | author<br/>**description**<br />**keywords**<br />generator<br/>revised<br/>others | 把 content 属性关联到一个name。            |
| http-equiv    | content-type<br />expires<br />refresh<br />set-cookie       | 把 content 属性关联到 http 头部            |
| scheme        | some_text                                                    | 定义用于翻译 content 属性值的格式          |

### link标签-链接外部资源

- `<link rel="stylesheet" type="text/css" href="文件url" />`

  多用于链接外部css文件。

### base标签-基准链接

base标签：为页面所有链接规定默认url或默认target。

- `<base href="" target="" />`

| `<base/>`属性 | 值               | 描述                           |
| ------------- | ---------------- | ------------------------------ |
| herf          | url              | 规定页面所有链接的默认url      |
| target        | _self<br>\_blank | 规定页面所有链接的默认打开方式 |

## HTML标签

HTML元素：从开始标签（start tag）到结束标签（end tag）的所有代码；

空元素：没有内容的 HTML 元素；推荐**在开始标签中关闭**；如`<br/>`；

### HTML标签分类
按标签类型分类：
- 单标签：`<br/>`，`<hr/>`，`<img/>`，`<input/>`...
- 双标签：`<head></head>`，`<body></body>`，`<p></p>`，`<div></div>`...

按标签显示模式分类：
- **块级元素**：`<div></div>`，`<ul></ul>`，`<h1>~<h6>`，`<p></p>`...
- **行级元素**：`<span></span>`，`<a></a>`...
- **行内块元素**：`<img/>`、`<input/>`、`<td></td>`...

### HTML标签属性
HTML标签属性格式：**name="value"** ；
> 详细参考[《HTML标准属性参考手册》](http://www.w3school.com.cn/tags/html_ref_standardattributes.asp)

| 属性  | 值               | 描述                                     |
| ----- | ---------------- | ---------------------------------------- |
| id    | id               | 规定元素的唯一 id                        |
| class | classname        | 规定元素的类名（classname）              |
| style | style_definition | 规定元素的行内样式（inline-style）       |
| title | text             | 规定元素的额外信息（可在工具提示中显示） |

### 排版标签
- 标题标签：`<h1>一级标题</h1>`~`<h6>六级标题</h6>`
- 段落标签：`<p>这是一个段落</p>`
- 换行标签：`<br/>`
- 水平线标签：`<hr/>`
- 块标签：`<div></div>`
- 行标签：`<span></span>`

### 文本格式化标签

| 文本格式 | HTML4               | HTML5               |
| -------- | ------------------- | ------------------- |
| 加粗     | `<b></b>`           | `<strong></strong>` |
| 斜体     | `<i></i>`           | `<em></em>`         |
| 下划线   | `<u></u>`不推荐使用 | `<ins></ins>`       |
| 删除线   | `<s></s>`不推荐使用 | `<del></del>`       |

### 图片标签-img★
- `<img src="url" alt="替代文本" />`

| `<img/>`属性 | 值    | 描述                       |
| ------------ | ----- | -------------------------- |
| **src**      | url   | 本地图片路径 / 网络图片url |
| **alt**      | text  | 图片非正常显示的替代文本   |
| width&height | px，% | 设置图像宽&高              |
| title        | text  | 鼠标悬停时的显示文本       |
| border       | px    | 图像边框宽度               |

> 避免图片失真：推荐width&height只设置一个值；

### 链接标签-a★

- `<a herf="url" target="_blank"></a>`

| `<a>`属性 | 值                | 描述                                 |
| --------- | ----------------- | ------------------------------------ |
| **href**  | url               | 超链接url / #id                      |
| target    | \_self<br>\_blank | 本标签页打开（默认）<br>新标签页打开 |
| name      | text              | 锚点名称                             |

> **锚点定位：`<a href="#id/name"></a>`**；

### 列表标签

#### 无序列表-ul
```html
<ul>
	<li>表项1</li>
	<li>表项2</li>
</ul>
```
#### 有序列表-ol
```html
<ol>
	<li>表项1</li>
	<li>表项2</li>
</ol>
```
#### 自定义列表-dl
```html
<dl>
	<dt>上级表项1</dt>
		<dd>下级表项11</dd>
		<dd>下级表项12</dd>
	<dt>上级表项2</dt>
		<dd>下级表项21</dd>
		<dd>下级表项22</dd>
</dl>
```
> 列表项计数问题：从1开始计数，dl从dt开始计数；

### 表格标签-table
```html
<table border="1px">
	<thead>
		<tr>
			<th>表头1</th>
			<th>表头2</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>第1行第1格</td>
			<td>第1行第2格</td>
		</tr>
		<tr>
			<td>第2行第1格</td>
			<td>第2行第2格</td>
		</tr>
	</tbody>
</table>
```
> 空单元格边框未显示问题：在空单元格中添加一个空格占位符`&nbsp;`；

`<table>`属性：
- `border`：设置边框；
- `cellspaceing`：单元格间距；
- `cellpadding`：单元格边距；

`<td>`属性：
- **合并单元格**：`rowspan=""`跨行， `colspan=""`跨列；
- `align="left/center/right"`：水平对齐方式；




### 表单标签-form
```html
<form action="" method="GET">
	表单域：表单元素；
</form>
```
| `<form>`属性 | 值                  | 描述                         |
| ------------ | ------------------- | ---------------------------- |
| action       | url                 | 规定提交表单的目的地址url    |
| method       | **GET**<br>**POST** | 规定提交表单使用的 HTTP 方法 |
| target       | _self<br>\_blank    | 规定action的打开方式         |
> **HTTP 方法**：
> - **GET**：表单数据在地址栏可见，明文；（默认）
> - **POST**：表单数据在地址栏不可见，密文；



#### input标签★

`<input type="" name="" value="" />`

| `<input/>`属性 | 值                                                           | 描述                                                         |
| -------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **type**       | text<br>password<br>radio<br>checkbox<br>button<br>submit<br>reset<br>image<br>file | 单行文本输入框<br>密码输入框<br>单选框<br>复选框<br>普通按钮<br>提交按钮<br>重置按钮<br>图片<br>文件 |
| name           | 用户自定义                                                   | input控件名称                                                |
| value          | 用户自定义                                                   | input控件初始文本值                                          |
| **checked**    | **checked**                                                  | 定义选框预选项                                               |
| **disabled**   | **disabled**                                                 | 禁用表单元素                                                 |
| size           | number                                                       | 字段显示宽度                                                 |
| maxlength      | number                                                       | 字段最大长度                                                 |

**H5新增input属性：**

| `<input/>`属性（H5） | 值        | 描述                                                        |
| -------------------- | --------- | ----------------------------------------------------------- |
| placeholder          | text      | 输入字段的提示                                              |
| autofocus            | autofocus | 规定在页面加载时是否获得焦点<br> （不适用于 type="hidden"） |
| multiple             | multiple  | 多文件上传                                                  |
| autocomplete         | on<br>off | 是否使用字段的自动完成功能                                  |
| required             | required  | 必填项，不能为空                                            |

**H5新增input type值：**

| input  type值（H5） | 描述         |
| ------------------- | ------------ |
| email               | 邮箱格式     |
| tel                 | 手机号码     |
| url                 | url格式      |
| number              | 数字格式     |
| search              | 搜索框       |
| range               | 自由拖动滑块 |
| time                | 时分         |
| date                | 年月日       |
| datetime            | 时间         |
| month               | 月年         |
| week                | 星期 年      |

#### label标签
label标签：为 input 元素定义标注
- `<label for=""></label>`

| `<label>`属性 | 值      | 描述                                  |
| ------------- | ------- | ------------------------------------- |
| for           | id      | 规定 label 绑定到哪个表单元素。       |
| form          | form_id | 规定 label 字段所属的一个或多个表单。 |

#### select标签-下拉列表

```html
<select name="" id="">
	<option value="">下拉项1</option>
	<option value="">下拉项2</option>
</select>
```

| `<option>`属性 | 值           | 描述                   |
| -------------- | ------------ | ---------------------- |
| **selected**   | **selected** | 定义下拉列表预选项     |
| **disabled**   | **disabled** | 禁用表单元素           |
| value          | text         | 定义送往服务器的选项值 |

#### textarea标签-文本域

```html
<textarea name="" id="" cols="30" rows="10">
	文本域：多行文本
</textarea>
```

- `rows`&`cols`：定义文本的可见行&列；


#### fieldset标签-元素分组

```html
<fieldset>
	<legend>元素组标题</legend>
	表单元素1: <input type="text" />
	表单元素2: <input type="text" />
</fieldset>
```

#### datalist标签-input可能值（H5）

datalist标签：定义选项列表。与 input 连用，定义 input 可能的值。

```html
<input list="datalist-id" />
<datalist id="datalist-id">
	<option value="input可能值_01">
	<option value="input可能值_02">
	<option value="input可能值_03">
</datalist>
```



### 多媒体标签

#### embed标签-嵌入内容

- `<embed src="" type=""/>`

| `<embed/>`属性 | 值   | 描述            |
| -------------- | ---- | --------------- |
| src            | url  | 嵌入内容的url   |
| type           | type | 嵌入内容的类型  |
| width&height   | px   | 嵌入内容的宽&高 |

#### audio标签-音频

- `<audio src=""></audio>`

| `<audio>`属性 | 值       | 描述         |
| ------------- | -------- | ------------ |
| src           | url      | 音频的url    |
| autoplay      | autoplay | 自动播放     |
| control       | control  | 显示音频控件 |
| loop          | loop     | 循环播放     |

#### video标签-视频

- `<video src=""></video>`

| `<video>`属性 | 值       | 描述         |
| ------------- | -------- | ------------ |
| src           | url      | 音频的url    |
| autoplay      | autoplay | 自动播放     |
| control       | control  | 显示视频控件 |
| loop          | loop     | 循环播放     |
| width&height  | px       | 视频的宽&高  |

### HTML代码约束

- 始终首行声明文档类型`<!DOCTYPE html>`；
- 建议关闭所有 HTML 元素；**空元素**，推荐**在开始标签中关闭**；
- HTML标签对大小写不敏感，推荐使用**小写标签**；
