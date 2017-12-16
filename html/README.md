# HTML 编码规范

## 1 规范制定原则

* 1．方便代码的交流和维护。
* 2．使代码更美观、阅读更方便。
* 3．符合 W3C HTML 标准。
* 4．当第二点和第三点原则和实际项目开发中的需求产生实质冲突,以实际项目为主。

## 2 书写建议

### 2.1 给你的文档加个 DOCTYPE

HTML5 的 DTD（文档类型定义）声明可以选择:

```html
<!DOCTYPE HTML>
```

HTML 4.01 中有 3 种 DTD（文档类型定义）声明可以选择:

1．Transitional 过渡的一种要求不很严格的 DTD，允许在页面中使用 HTML4.01 的标识（符合 xhtml 语法标准）。过渡的 DTD 的写法如下：

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"
   "http://www.w3.org/TR/html4/loose.dtd">  
```

2．Strict 严格的一种要求严格的 DTD，不允许使用任何表现层的标识和属性，例如<br/>等。严格的 DTD 的写法如下：

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
```

3．Frameset 框架的一种专门针对框架页面所使用的 DTD，当页面中含有框架元素时，就要采用这种 DTD。框架的 DTD 的写法如下：

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN"
   "http://www.w3.org/TR/html4/frameset.dtd">
```

目前，我们使用最多的是 Transitional，即 XHtml 1.0 Transitional。如果你的 Html 代码书写的还算良好，那把现有的 Transitional 转为 Strict 还是比较方便的。反之，也不用太急着转，个人觉得 Strict 更严谨，但用 Transitional 也并没有太大影响。

默认的 Html 页面示例:

```html
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" >
<head>
    <title>标题</title>
</head>
<body>
页面内容
</body>
</html>
```

### 2.2.所有的标记都必须要有一个相应的结束标记

在 HTML 中，你可以打开许多标签，例如`<p>`和`<li>`而不一定写对应的`</p>`和`</li>`来关闭它们。但是从代码的严谨性考虑我们推荐所有标签必须关闭。如果是单独不成对的标签，在标签最后加一个"/"来关闭它。

例如:

```html
<img alt="image name" src="../images/logo.png" />
<br />
```

### 2.3.所有标签的元素和属性的名字都必须使用小写

虽然 HTML 对大小写是不敏感的，`<title>`和`<TITLE>`是表示相同的标签，但是我们推荐所有的标签和属性的名字都必须用小写。

例如：

```html
<BODY>
```

需要修改为

```html
<body>
```

大小写夹杂也是不被认可的。

例如：

````html
<input onMouseOve="message();" >
```需要修改为
``` html
<input onmouseover="message();" >
````

### 2.4.所有的 HTML 标记都必须合理嵌套

我们推荐 HTML 结构要严谨，所有的嵌套都必须按顺序。

例如：

```html
<p><b></p></b>
```

需要修改为：

```html
<p><b></b></p>
```

一层一层的嵌套必须是严格对称。

在我们的页面标题里面，我们使用`<h1>`作为网站标题标签，这是完美的。并且添加了一个到首页的链接，你可能会这么写`<a href=”index.html”><h1>`标题`</h1></a>` 这里面有一个错误就出在把链接放到 了`<h1>`外面，`<a>`链接包围了`<h1>`。这种简单的嵌套错误，大多数浏览器都能良好的处理，但从技术上来说，这是不行的。

例如：

```html
<a href="index.html" ><h1>标题</h1></a>
```

需要修改为：

```html
<h1><a href="index.html" >标题</a></h1>
```

因为锚链接是一个内联元素，而<h1>标题是一个区块元素，区块元素不应该被放在内联元素中。

### 2.5.所有的属性必须用引号""括起来

在 HTML 中，你可以不需要给属性值加引号，但是推荐给它们加引号。例如:

```html
<height=80>
```

需要修改为：

```html
<height="80">
```

特殊情况，你需要在属性值里使用双引号可以用&quot;，单引号可以使用&apos;，例如：

```html
<alt="say&apos;hello&apos;">
```

### 2.6.把所有<和&等特殊符号用转义字符表示

* 任何小于号（<），不是标签的一部分，都必须被编码为&lt; 。
* 任何大于号（>），不是标签的一部分，都必须被编码为&gt; 。
* 任何与号（&），不是实体的一部分的，都必须被编码为&amp; 。

常用 HTML 转义字符表
| 样式表名称 | 转义字符 | 描述信息 |
| -- | -- | -- |
| | `&nbsp;` | 空格 |
|& | `&amp;` | 和 |  
|< | `&lt;` | 小于号 |
|> | `&gt;` | 大于号 |
|" | `&quot;` | 双引号 |
|’ | `&apos;` | 单引号 |
|© | `&copy;` | 版权符 |
|® | `&reg;` | 注册符 |

注：以上转义字符以&开头, 全部小写, 字符之间无空格。

### 2.7 头部使用共用的外部 CSS 和 JavaScript 文件

我们有一些 CSS 代码已经延伸到我们的<head>部分。例如:

```html
<head>
<title>标题</title>
<style tyle=”text/css”>body{backgroud-color:#000;}</style>
</head>
```

这是一个严重的犯规，因为它它只能适用于单一的 Html 网页。保持独立的 CSS 文件意味着未来的网页可以链接到它们，并使用相同的代码。Javascript 也是同样的道理。

良好的头部信息格式

```html
<head>
<title>帐号管理 - 人员及权限管理 - X3</title>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<meta name="Copyright" content="X3Platform (C) 2010" />
<meta name="Keywords" content="" />
<link rel="shortcut icon" href="/favorite.ico" />
<link rel="stylesheet" media="all" href="static/styles/default/styles.min.css" type="text/css" />
<script type="text/javascript" src="static/scripts/jquery.min.js" ></script>
</head>
```

### 2.8.不要在注释内容中使“--”

在 HTML 中“--”只能发生注释的开头和结束，也就是说，在内容中它们不再有效。例如下面的代码是无效的:

```html
<!--这里是注释-----------这里是注释-->
```

用等号或者空格替换内部的虚线。

```html
<!--这里是注释============这里是注释-->
```

### 2.10. 验证

一些小的 Html 代码错误可能并不会对网页内容有多大影响，但通过 W3C 验证的代码将更有利于网页内容展示。比如以下示例中的图象，缺少自关闭标记 和 ALT 属性。

例如:

```html
<p>文本信息..<p>
<img src=”image/logo.jpg” >
```

## 相关工具

[The W3C Markup 验证服务](http://validator.w3.org/)
