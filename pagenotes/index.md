---
layout: archive
title: "网页笔记"
date: 2017-12-30T11:40:45-04:00
modified:
excerpt: "等一下"
tags: []
---

<!--HTML简介
• HTML 是用来描述网页的一种语言。
• HTML 指的是超文本标记语言: HyperText Markup Language
• HTML 不是一种编程语言，而是一种标记语言，标记语言是一套标记标签 (markup tag)
• HTML 使用标记标签来描述网页
• HTML 文档包含了HTML 标签及文本内容
• HTML文档也叫做 web 页面

HTML 标签
• HTML 标记标签通常被称为 HTML 标签 (HTML tag)。
• HTML 标签是由尖括号包围的关键词，比如 <html>
• HTML 标签通常是成对出现的，比如 <b> 和 </b>

HTML 元素
"HTML 标签" 和 "HTML 元素" 通常都是描述同样的意思.
但是严格来讲, 一个 HTML 元素包含了开始标签与结束标签-->


<!--HTML 标题
标题（Heading）是通过 <h1> - <h6> 标签进行定义的
<h1> 定义最大的标题。 <h6> 定义最小的标题
浏览器会自动地在标题的前后添加空行

标题很重要
• 搜索引擎使用标题为您的网页的结构和内容编制索引
• 因为用户可以通过标题来快速浏览您的网页，所以用标题来呈现文档结构是很重要的

HTML 水平线
<hr> 标签在 HTML 页面中创建水平线-->


<!--不能通过在 HTML 代码中添加额外的空格或换行来改变输出的效果
当显示页面时，浏览器会移除源代码中多余的空格和空行。所有连续的空格或空行都会被算作一个空格。
需要注意的是，HTML 代码中的所有连续的空行（换行）也被显示为一个空格-->
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <title>TestJs</title>
</head>

<body>

<h1>春晓</h1>

<p>
    春眠不觉晓，
            处处闻啼鸟。
    夜来风雨声，
            花落知多少。
</p>

<p>注意，浏览器忽略了源代码中的排版（省略了多余的空格和换行）</p>

</body>
</html>


<!--HTML 文本格式化
通常标签 <strong> 替换加粗标签 <b> 来使用, <em> 替换 <i>标签使用。
然而，这些标签的含义是不同的：<b> 与<i> 定义粗体或斜体文本。
<strong> 或者 <em>意味着你要呈现的文本是重要的，所以要突出显示。-->
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <title>TestJs</title>
</head>
<body>

<b>加粗文本</b><br/>
<i>斜体文本</i><br/>
<code>电脑自动输出</code><br/>
这是 <sub> 下标</sub> 和 <sup> 上标</sup>

<br/>
<pre>
此例演示如何使用 pre 标签
对空行和空格     进行控制
</pre>

<code>计算机输出</code>
<br/>
<kbd>键盘输入</kbd>
<br/>
<samp>计算机代码样本</samp>
<br/>
<var>计算机变量</var>
<br/>

<br/>
<address>
    Written by <a href="https://www.baidu.com">Jon Doe</a>.<br/>
    Visit us at:<br/>
    Example.com<br/>
    Box 564, Disneyland<br/>
    USA
</address>

<br/>
<abbr title="etcetera">etc.</abbr>
<br />
<acronym title="World Wide Web">WWW</acronym>
<p>在某些浏览器中，当您把鼠标移至缩略词语上时，title 可用于展示表达的完整版本。</p>
<p>仅对于 IE 5 中的 acronym 元素有效。</p>
<p>对于 Netscape 6.2 中的 abbr 和 acronym 元素都有效。</p>

<br/>
<p>该段落文字从左到右显示。</p>
<p><bdo dir="rtl">该段落文字从右到左显示。</bdo></p>

<br/>
&lt;!&ndash;语义化网页结构有助于搜索引擎的收录。同一个效果可以用很多钟方式实现，但这只方便了浏览者，而搜索引擎不知道这里到底是什么内容，
这里如果你使用<q>标签，那么就告诉浏览器这里是引用的话。而且在手持设备或移动设备不能很好支持css的基础上，
浏览器会使用默认的效果，因而提供较好可读性&ndash;&gt;
<p>WWF's goal is to:
    <q>Build a future where people live in harmony with nature.</q>
    We hope they succeed.</p>

<br/>
<p>My favorite color is <del>blue</del> <ins>red</ins>!</p>

<br/>
&lt;!&ndash;定义一个摘自另一个源的块引用&ndash;&gt;
<blockquote cite="http://www.worldwildlife.org/who/index.html">
    For 50 years, WWF has been protecting the future of nature.
    The world’s leading conservation organization, WWF works in 100 countries and
    is supported by 1.2 million members in the United States and close to 5 million globally.
</blockquote>

<br/>
&lt;!&ndash;dfn 是 Definition（定义）的缩写。对特殊术语或短语的定义可以用&ndash;&gt;
<dfn>定义项目</dfn>

<br/>
&lt;!&ndash;在当前页面链接到指定位置&ndash;&gt;
<p><a href="#C2">查看章节 2</a></p>

<h2>章节 1</h2>
<p>这边显示该章节的内容……</p>

<h2><a id="C2">章节 2</a></h2>
<p>这边显示该章节的内容……</p>

<h2>章节 3</h2>
<p>这边显示该章节的内容……</p>

</body>
</html>


<!--HTML <head>
<head> 元素包含了所有的头部标签元素。在 <head>元素中你可以插入脚本（scripts）, 样式文件（CSS），及各种meta信息。
可以添加在头部区域的元素标签为: <title>, <style>, <meta>, <link>, <script>, <noscript>, and <base>.

<title> 元素:
• 定义了浏览器工具栏的标题
• 当网页添加到收藏夹时，显示在收藏夹中的标题
• 显示在搜索引擎结果页面的标题

HTML <base> 元素
<base> 标签描述了基本的链接地址/链接目标（链接的公共部分），该标签作为HTML文档中所有的链接标签的默认链接
<head>
    <base href="http://www.runoob.com/images/" target="_blank">
</head>

HTML <link> 元素
<link> 标签定义了文档与外部资源之间的关系。
<link> 标签通常用于链接到样式表:
<head>
    <link rel="stylesheet" type="text/css" href="mystyle.css">
</head>

HTML <style> 元素
<style> 标签定义了HTML文档的样式文件引用地址.
在<style> 元素中你需要指定样式文件来渲染HTML文档:
<head>
 <style type="text/css">
body {background-color:yellow}
p {color:blue}
</style>
</head>

HTML <meta> 元素
meta标签描述了一些基本的元数据。
<meta> 标签提供了元数据.元数据也不显示在页面上，但会被浏览器解析。
META元素通常用于指定网页的描述，关键词，文件的最后修改时间，作者，和其他元数据。
元数据可以使用于浏览器（如何显示内容或重新加载页面），搜索引擎（关键词），或其他Web服务。
<meta>一般放置于 <head>区域

<meta> 标签- 使用实例
为搜索引擎定义关键词:
<meta name="keywords" content="HTML, CSS, XML, XHTML, JavaScript">
为网页定义描述内容:
<meta name="description" content="Free Web tutorials on HTML and CSS">
定义网页作者:
<meta name="author" content="Hege Refsnes">
每30秒中刷新当前页面:
<meta http-equiv="refresh" content="30">-->


<!--HTML 样式- CSS

如何使用CSS
CSS 是在 HTML 4 开始使用的,是为了更好的渲染HTML元素而引入的.
CSS 可以通过以下方式添加到HTML中:
• 内联样式- 在HTML元素中使用"style" 属性
• 内部样式表 -在HTML文档头部 <head> 区域使用<style> 元素 来包含CSS
• 外部引用 - 使用外部 CSS 文件
• 最好的方式是通过外部引用CSS文件-->

<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <style type="text/css">
        body {background-color:lightgray;}
        p {color:blue;}
    </style>
    <title>TestJs</title>
</head>
<h2 style="background-color:mediumpurple;text-align:center;">这是一个标题</h2>
<p style="font-family:arial;font-size:20px;">这是一个段落。</p>
</body>
</html>


<!--HTML 图像
<img> 是空标签，意思是说，它只包含属性，并且没有闭合标签。
要在页面上显示图像，你需要使用源属性（src）。src 指 "source"。源属性的值是图像的 URL 地址。
定义图像的语法是：
<img src="url" alt="some_text">
浏览器将图像显示在文档中图像标签出现的地方。如果你将图像标签置于两个段落之间，
那么浏览器会首先显示第一个段落，然后显示图片，最后显示第二段

alt 属性用来为图像定义一串预备的可替换的文本。
替换文本属性的值是用户定义的。在浏览器无法载入图像时，替换文本属性告诉读者她们失去的信息
<img src="boat.gif" alt="Big Boat">

height（高度） 与 width（宽度）属性用于设置图像的高度与宽度。
属性值默认单位为像素-->

<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <title>TestJs</title>
    <base href="http://www.runoob.com/images/" target="_blank">
</head>
<body>

<p>
    <img src="pulpit.jpg" alt="Smiley face" style="float:left" width="32" height="32">
    一个带图片的段落，图片浮动在这个文本的左边。
</p>

<p>
    一个带图片的段落，不使用浮动。
    <img src="pulpit.jpg" alt="Smiley face" style="float:none" width="32" height="32">
</p>

<p>创建图片链接:
    <a href="//www.runoob.com/html/html-tutorial.html">
        <img src="http://www.runoob.com/try/demo_source/smiley.gif"
             alt="HTML 教程" width="32" height="32"></a></p>

<p><b>注意:</b> 在这里我们使用了 CSS "float" 属性，在HTML 4中 align 属性已废弃，
    HTML5 已不支持该属性，可以使用 CSS 代替。</p>

</body>
</html>

<!--创建图像映射-->
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <title>TestJs</title>
    <base href="http://www.runoob.com/try/demo_source/" target="_blank">
</head>
<body>

<p>点击太阳或其他行星，注意变化：</p>

<img src="planets.gif" width="145" height="126" alt="Planets" usemap="#planetmap">

<map name="planetmap">
    <area shape="rect" coords="0,0,82,126" alt="Sun" href="sun.htm">
    <area shape="circle" coords="90,58,3" alt="Mercury" href="mercur.htm">
    <area shape="circle" coords="124,58,8" alt="Venus" href="venus.htm">
</map>

</body>
</html>


<!--HTML 表格
HTML 表格标签
标签          描述
<table>     定义表格
<th>        定义表格的表头
<tr>        定义表格的行
<td>        定义表格单元
<caption>   定义表格标题
<colgroup>  定义表格列的组
<col>       定义用于表格列的属性
<thead>     定义表格的页眉
<tbody>     定义表格的主体
<tfoot>     定义表格的页脚-->

<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <title>TestJs</title>
</head>
<body>

<p>
    每个表格从一个 table 标签开始。
    每个表格行从 tr 标签开始。
    每个表格的数据从 td 标签开始。
</p>

<h4>一列:</h4>
<table border="1">
    <tr>
        <td>100</td>
    </tr>
</table>

<h4>一行三列:</h4>
<table border="1">
    <tr>
        <td style='border:0px'>100</td>
        <td style='border-top:0px;border-bottom:0px'>200</td>
        <td>300</td>
    </tr>
</table>

<h4>两行三列:</h4>
<table border="1" cellpadding="10" cellspacing="0" style="border-collapse: collapse" bordercolor="#000000">
    <tr>
        <th>Header 1</th>
        <th colspan="2">Header 2</th>
    </tr>
    <tr>
        <td>100</td>
        <td>200</td>
        <td>300</td>
    </tr>
    <tr>
        <td>400</td>
        <td>500</td>
        <td>600</td>
    </tr>
</table>

</body>
</html>


<!--HTML 列表
HTML 列表标签
标签      描述
<ol>    定义有序列表
<ul>    定义无序列表
<li>    定义列表项
<dl>    定义定义列表
<dt>    自定义列表项目
<dd>    定义自定列表项的描述-->
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <title>TestJs</title>
</head>
<body>

<h4>无序列表:</h4>
<ul>
    <li>Coffee</li>
    <li>Tea</li>
    <li>Milk</li>
</ul>

<h4>编号列表：</h4>
<ol>
    <li>Apples</li>
    <li>Bananas</li>
    <li>Lemons</li>
    <li>Oranges</li>
</ol>

<h4>大写字母列表：</h4>
<ol type="A">
    <li>Apples</li>
    <li>Bananas</li>
    <li>Lemons</li>
    <li>Oranges</li>
</ol>

<h4>小写字母列表：</h4>
<ol type="a">
    <li>Apples</li>
    <li>Bananas</li>
    <li>Lemons</li>
    <li>Oranges</li>
</ol>

<h4>罗马数字列表：</h4>
<ol type="I">
    <li>Apples</li>
    <li>Bananas</li>
    <li>Lemons</li>
    <li>Oranges</li>
</ol>

<h4>小写罗马数字列表：</h4>
<ol type="i">
    <li>Apples</li>
    <li>Bananas</li>
    <li>Lemons</li>
    <li>Oranges</li>
</ol>

<p><b>注意：</b> 在 HTML 4中 ul 属性已废弃，HTML5 已不支持该属性，因此我们使用 CSS 代替来定义不同类型的无序列表如下：</p>

<h4>圆点列表：</h4>
<ul style="list-style-type:disc">
    <li>Apples</li>
    <li>Bananas</li>
    <li>Lemons</li>
    <li>Oranges</li>
</ul>

<h4>圆圈列表：</h4>
<ul style="list-style-type:circle">
    <li>Apples</li>
    <li>Bananas</li>
    <li>Lemons</li>
    <li>Oranges</li>
</ul>

<h4>正方形列表：</h4>
<ul style="list-style-type:square">
    <li>Apples</li>
    <li>Bananas</li>
    <li>Lemons</li>
    <li>Oranges</li>
</ul>

<h4>一个自定义列表：</h4>
<dl>
    <dt>Coffee</dt>
    <dd>• black hot drink</dd>
    <dt>Milk</dt>
    <dd>• white cold drink</dd>
</dl>

</body>
</html>


<!--HTML <div> 和<span>
HTML 可以通过 <div> 和 <span>将元素组合起来

HTML 区块元素
大多数 HTML 元素被定义为块级元素或内联元素。
块级元素在浏览器显示时，通常会以新行来开始（和结束）。
实例: <h1>, <p>, <ul>, <table>

HTML 内联元素
内联元素在显示时通常不会以新行开始。
实例: <b>, <td>, <a>, <img>

HTML <div> 元素
HTML <div> 元素是块级元素，它可用于组合其他 HTML 元素的容器。
<div> 元素没有特定的含义。除此之外，由于它属于块级元素，浏览器会在其前后显示折行。
如果与 CSS 一同使用，<div> 元素可用于对大的内容块设置样式属性。
<div> 元素的另一个常见的用途是文档布局。它取代了使用表格定义布局的老式方法。
使用 <table> 元素进行文档布局不是表格的正确用法。<table> 元素的作用是显示表格化的数据。

HTML <span> 与元素
HTML <span> 元素是内联元素，可用作文本的容器
<span> 元素也没有特定的含义。
当与 CSS 一同使用时，<span> 元素可用于为部分文本设置样式属性。-->

<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <title>TestJs</title> 
</head>
<body>

<p>这是一些文本。</p>

<div style="color:#0000FF">
    <h3>这是一个在 div 元素中的标题。</h3>
    <p>这是一个在 div 元素中的文本。</p>
</div>

<p>他的母亲有 <span style="color:blue;font-weight:bold">蓝色</span> 的眼睛，他的父亲有
    <span style="color:darkolivegreen;font-weight:bold">碧绿色</span> 的眼睛。</p>

<p>这是一些文本。</p>

</body>
</html>


<!--HTML 布局
HTML 布局 - 使用<div> 元素
div 元素是用于分组 HTML 元素的块级元素。
下面的例子使用五个 div 元素来创建多列布局：-->

<!DOCTYPE html>
<html>
<head> 
    <meta charset="utf-8"> 
    <title>TestJs</title> 
</head>
<body>

<div id="container" style="width:500px">

    <div id="header" style="background-color:#FFA500;">
        <h1 style="margin-bottom:0;">主要的网页标题</h1></div>

    <div id="menu" style="background-color:#FFD700;height:200px;width:100px;float:left;">
        <b>菜单</b><br>
        HTML<br>
        CSS<br>
        JavaScript</div>

    <div id="content" style="background-color:#EEEEEE;height:200px;width:400px;float:left;">
        内容在这里</div>

    <div id="footer" style="background-color:#FFA500;clear:both;text-align:center;">
        版权 © runoob.com</div>

</div>

</body>
</html>

<!--HTML 布局 - 使用表格
使用 HTML <table> 标签是创建布局的一种简单的方式
即使可以使用 HTML 表格来创建漂亮的布局，但设计表格的目的是呈现表格化数据 - 表格不是布局工具！-->

<!DOCTYPE html>
<html>
<head> 
    <meta charset="utf-8"> 
    <title>TestJs</title> 
</head>
<body>

<table width="500" border="0">
    <tr>
        <td colspan="2" style="background-color:#FFA500;">
            <h1>主要的网页标题</h1>
        </td>
    </tr>

    <tr>
        <td style="background-color:#FFD700;width:100px;">
            <b>菜单</b><br>
            HTML<br>
            CSS<br>
            JavaScript
        </td>
        <td style="background-color:#eeeeee;height:200px;width:400px;">
            内容在这里</td>
    </tr>

    <tr>
        <td colspan="2" style="background-color:#FFA500;text-align:center;">
            版权 © runoob.com</td>
    </tr>
</table>

</body>
</html>


<!--HTML 表单和输入
HTML 表单用于搜集不同类型的用户输入
HTML 表单
表单是一个包含表单元素的区域。
表单元素是允许用户在表单中输入内容,比如：文本域(textarea)、下拉列表、单选框(radio-buttons)、复选框(checkboxes)等等。
表单使用表单标签 <form> 来设置:
<form>
    .
    input 元素
    .
</form>

HTML 表单 - 输入元素
多数情况下被用到的表单标签是输入标签（<input>）。
输入类型是由类型属性（type）定义的。大多数经常被用到的输入类型如下：

文本域（Text Fields）
文本域通过<input type="text"> 标签来设定，当用户要在表单中键入字母、数字等内容时，就会用到文本域。
<form>
    First name: <input type="text" name="firstname"><br>
    Last name: <input type="text" name="lastname">
</form>

密码字段
密码字段通过标签<input type="password"> 来定义:
<form>
    Password: <input type="password" name="pwd">
</form>

单选按钮（Radio Buttons）
<input type="radio"> 标签定义了表单单选框选项
<form>
    <input type="radio" name="sex" value="male">Male<br>
    <input type="radio" name="sex" value="female">Female
</form>

复选框（Checkboxes）
<input type="checkbox"> 定义了复选框. 用户需要从若干给定的选择中选取一个或若干选项。
<form>
<input type="checkbox" name="vehicle" value="Bike">I have a bike<br>
<input type="checkbox" name="vehicle" value="Car">I have a car
</form>

提交按钮(Submit Button)
<input type="submit"> 定义了提交按钮.
当用户单击确认按钮时，表单的内容会被传送到另一个文件。表单的动作属性定义了目的文件的文件名。
由动作属性定义的这个文件通常会对接收到的输入数据进行相关的处理:
<form name="input" action="javascript:void(0)" method="get">
Username: <input type="text" name="user">
<input type="submit" value="Submit">
</form>-->

<!DOCTYPE html>
<html>
<head> 
    <meta charset="utf-8"> 
    <title>TestJs</title> 
</head>
<body>

<p><b>单选按钮</b></p>
<form action="">
    <input type="radio" name="sex" value="male">Male<br>
    <input type="radio" name="sex" value="female">Female
</form>

<br/>
<p><b>复选框</b></p>
<form action="">
    <input type="checkbox" name="vehicle" value="Bike">I have a bike<br>
    <input type="checkbox" name="vehicle" value="Car">I have a car
</form>

<br/>
<p><b>简单下拉列表</b></p>
<form action="">
    <select name="cars">
        <option value="volvo">Volvo</option>
        <option value="saab">Saab</option>
        <option value="fiat">Fiat</option>
        <option value="audi">Audi</option>
    </select>
</form>

<br/>
<p><b>预选下拉列表</b></p>
<form action="">
    <select name="cars">
        <option value="volvo">Volvo</option>
        <option value="saab">Saab</option>
        <option value="fiat" selected>Fiat</option>
        <option value="audi">Audi</option>
    </select>
</form>

<br/>
<p><b>文本域（textarea）</b></p>
<textarea rows="10" cols="30">
我是一个文本框。
</textarea>

<br/>
<p><b>创建按钮</b></p>
<form action="">
    <input type="button" value="Hello world!">
</form>

<br/>
<p><b>文本域（text filed）</b></p>
<form>
    First name: <input type="text" name="firstname"><br>
    Last name: <input type="text" name="lastname">
</form>

<br/>
<p><b>密码字段</b></p>
<form>
    Password: <input type="password" name="pwd">
</form>

<br/>
<p><b>带边框的表单</b></p>
<form action="">
    <fieldset>
        <legend>Personal information:</legend>
        Name:           <input type="text" size="30"><br>
        E-mail:         <input type="text" size="30"><br>
        Date of birth:  <input type="text" size="10">
    </fieldset>
</form>

<br/>
<p><b>选项组</b></p>
<select>
    <optgroup label="Swedish Cars">
        <option value="volvo">Volvo</option>
        <option value="saab">Saab</option>
    </optgroup>
    <optgroup label="German Cars">
        <option value="mercedes">Mercedes</option>
        <option value="audi">Audi</option>
    </optgroup>
</select>

<br/>
<p><b>指定一个预先定义的输入控件选项列表</b></p>
<p><strong>注意:</strong> Internet Explorer 9（更早 IE 版本），Safari 不支持 datalist 标签。</p>
<form action="javascript:void(0)" method="get">
    <input list="browsers" name="browser">
    <datalist id="browsers">
        <option value="Internet Explorer">
        <option value="Firefox">
        <option value="Chrome">
        <option value="Opera">
        <option value="Safari">
    </datalist>
    <input type="submit">
</form>

<br/>
<p><b>定义一个计算结果</b></p>
<p><strong>注意:</strong>  Internet Explorer 不支持 output 标签。</p>
<form oninput="x.value=parseInt(a.value)+parseInt(b.value)">0
    <input type="range" id="a" value="50">100
    +<input type="number" id="b" value="50">
    =<output name="x" for="a b"></output>
</form>

</body>
</html>


<!--
HTML 框架
iframe语法:
<iframe src="URL"></iframe>
该URL指向不同的网页
-->

<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <title>TestJs</title>
</head>
<body>

<iframe src="http://www.runoob.com/try/demo_source/demo_iframe.htm" name="iframe_a" frameborder="0"></iframe>
<p><a href="//www.runoob.com" target="iframe_a">RUNOOB.COM</a></p>

<p><b>注意：</b> 因为 a 标签的 target 属性是名为 iframe_a 的 iframe 框架，所以在点击链接时页面会显示在 iframe框架中。</p>

</body>
</html>

<div class="tiles">
{% for post in site.categories.pagenotes %}
  {% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles 把所有categories 有 pagenotes 的列出來-->
