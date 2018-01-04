---
layout: archive
title: "css"
date: 2018-01-03T11:40:45-04:00
modified:
excerpt: "css"
tags: []
image: 
  feature: 
  teaser:
---
CSS书写顺序：
1.位置属性(position, top, right, z-index, display, float等)
2.大小(width, height, padding, margin)
3.文字系列(font, line-height, letter-spacing, color- text-align等)
4.背景(background, border等)
5.其他(animation, transition等)
//代表当前所有的标签 通配符（兼容任何浏览器打开页面内容的边距都为0）。
目前最常用的是Normalize.css ，它是一个可定制的 CSS 文件，使浏览器呈现的所有元素，更一致和符合现代标准。
它正是针对只需要统一的元素样式，依赖于研究浏览器默认元素风格之间的差异，精确定位需要重置的样式。

-ms-（私有属性）；//IE
-moz-（私有属性）；//Firefox 
-webkit-（私有属性）；//Safari 和 Chrome 
-o-（私有属性）；// Opera
如：-moz-column-count:4;（分成4块显示） // Firefox 
 
盒子3D模型（由外到内）：
```
border(边框)>content-padding(内边距)>background-image(背景图像)>background-color(背景颜色)>margin(外边距)
```
盒子尺寸大小 = 边框+外边距+内边距+盒子里的内容大小
稳定性最好的就是盒子本身的高度和宽度了，我们优先考虑这个。 
因此，很多情况下，我们会考虑利用高度剩余法，宽度剩余法来做，而不是padding和margin。
其次，我们才考虑padding ，因为padding也可以看做特殊的盒子高度和宽度，最后我们再用margin来做。因为margin会有边距合并的问题。
 
属性笔记：
垂直居中最常用的方法：父元素设置display: table;子元素设置display: table-cell;vertical-align: middle;则子元素容器里面的内容垂直居中。
 
1em=16px;//ie无法调整px作为单位的网页字体大小,em具有继承性。(如果定义了body{font-size=12px;} #title{font-siez=2.6em;}而id=title恰好在body里面,那么id=title的字体大小就是2.6*16-12=29.6px)
 
z-index:9;//并级的对象，此属性参数值越大，则被层叠在最上面(只有在定位的情况下才能设置),属性只能工作于那些被定义了position属性的元素中。 
 
absolute完全脱离文档流，不占据任何空间，不影响整体布局和结构，和relative更没有任何依赖关系。absolute最好不要和父元素有依赖关系，防止整体变动时崩塌，使用absolute和margin定位能达到最佳效果，而且absolute具有跟随性，如果前一个元素是inline或者inline-block，那么就算是0空间它一样会跟随前一个元素的位置并排显示，还能自适应浏览器大小在当前位置显示不动。元素进行绝对定位后脱离文档流，其宽度是根据元素内容所占宽度来计算的，为这能让其视觉效果更好，最好给元素定义一个宽度值。float属性也是如此，其宽度是根据元素内容所占宽度来计算的。 
 
单行溢出文本显示省略号...的方法：white-space:nowrap;  //文字一行显示  overflow:hidden;   text-overflow:ellipsis;  //超出的...显示（超出部分省略号显示）
参考地址：[](http://jssl915.github.io/overflow.html)
 
text-indent:-999px;overflow：hidden;  （隐藏按钮文字的小技巧）

块元素可以设置margin和padding值，行元素只能设置水平方向的padding和margin值。
行内元素中间有空隙，产生原因：换行符、tab（制表符）、空格产生间隙。
解决方法：1.元素写成一行（代码格式不规范，不建议使用） 2.设置父容器font-size：0；
 
li中插入img图片间有空隙的解决方案: 父容器font-size:0或img{vertical-align:bottom/top; display:block;}
 
高度不适应是当内层对象的高度发生变化时外层高度不能自动进行调节，特别是当内层对象使用margin或padding时。
解决方法：为父DIV添加overflow:hidden;需要给父div设置边框，当然可以设置边框为透明;为父DIV添加padding，或者至少添加padding-top;
 
visibility隐藏后，仍然占据空间（效率高，不经常用）
display隐藏后，不占据空间（效率低，经常用） 
display:block(块元素)/inline（行内元素）/inline-block（行内块元素）;//由行元素转变为块元素
 
为盒子添加contentEditable="true"，盒子将变为可编辑的文本框。
 
ul li:nth-child(1) //代表父亲li里面的第一个儿子
 
当值是0时，除了RGB颜色值0%必须跟百分号，其他情况后面可以不跟单位"px"。
清除浮动：
其一（最有效的方法），1.给浮动元素紧邻后面的元素设置clear：both；2.给浮动元素的父容器设置overflow：hidden；
其二，通过在浮动元素的末尾添加一个空元素，div设置 clear：both属性br设置clear："all"，after伪元素其实也是通过 content 在元素的后面生成了内容为一个点的块级元素（空标签无意义，不建议使用）；
其三，给浮动元素紧邻后面的元素设置with：100%（或者固定宽度）+overflow：hidden；
清楚区域是在元素上外边距之上增加的额外间隔，不允许任何浮动元素进入这个范围内。这意味着元素设置clear属性时，它的外边距并不会改变。要确保一个清楚元素的顶端与一个浮动元素的底端之间有一定的空间，可以为浮动元素本身设置一个下外边距。
 
上下相邻的普通元素，上下边距，并非简单的相加，而是取其中较大的边距值，这种现象叫做margin重叠。如果不是普通元素，两相邻元素边距相加。外边距合并只出现在块级元素上，浮动元素不会和相邻的元素产生外边距合并，绝对定位元素不会和相邻的元素产生外边距合并，内联块级元素间不会产生外边距合并。 
 
vertical-align属性只对行内元素有效果，对块级元素没有任何效果。
 
align="abbsmiddle" //插入一张图片和文字，使图片和文字在竖直居中
 
不使用list-style-image来定义列表项目标记符号，而用background-image来代替，并通过background-position来进行定位。
 
当子元素为绝对定位元素，同时，父容器的position值为static的时候，为子元素添加height:inherit，如果容器高度变化了，里面的绝对定位元素依然高度自适应。如果页面很复杂，避免使用position: relative会让你少去很多z-index混乱层级覆盖的麻烦。附地址：http://www.zhangxinxu.com/wordpress/2015/02/different-height-100-height-inherit/
 
Web安全颜色的简写十六进制值是0,3,6,9,C,F，因此#693，#0C6，#F0F都是Web安全颜色的例子。十六进制的颜色值的简写形式是浏览器会取每一位，并将其复制成两位，例如#F00等价于#FF0000。
 
关于固定宽度的DIV中英文不能自动换行的问题，解决方法是：
word-break:break-all；或word-wrap:break-word；
两者区别：
    1、word-break:break-all;内容到达固定宽度处会自动换行，如果该行末端有个英文单词很长，则把单词截断。对FF无效。
    2、word-wrap:break-word;如果该a行末端宽度不够显示整个单词，它会自动把整个单词放到下一行b行，而不会在 a行 把单词截断。若b行整行都不够一个单词宽，则将单词截断以对齐。对FF、IE有效。
3.表格中处理长英文换行办法：table-layout:fixed;word-wrap:break-word;
优缺点：
word-break:break-all能很好的让文本对齐，显得整洁，但是100%切断单词，易读性降低
word-wrap:break-word比较人性化，但行末会参差不齐。
 
font属性的前三个值允许采用任意的顺序，但后两个值要严格得多。font-size和font-family不仅要以此顺序（font-size在前，font-family在后）作为声明中的最后两个值，而且font声明中必须有这两个值，这很明确。
如果少了其中某个属性，那么整个规则都是无效的。
 
表格td中设置overflow:hidden不起作用，添加table-layout:fixed属性即可解决。如果想去除页面默认滚动条，添加overflow:hidden即可。
 
```position:absolute;left:0;right:0;top:0;bottom:0;的效果和width:100%;height:100%;position:absolute;left:0;top:0;```一样，相当于全屏拉伸占据当前可见视窗。
 
如果元素(包括select，input等)边框未设置颜色的话(前提是边框已经设置了border-style)，color会影响元素周围的边框颜色。
 
子元素上下左右内、外边距的百分比都是相当于父元素的宽度来计算的。
 
如果background-position用百分数设置，水平值必须先出现，否则实际效果不对。
 
行内元素与一个浮动元素重叠时，其边框、背景和内容都在该浮动元素"之上"显示。
块元素与一个浮动元素重叠时，其边框和背景在该浮动元素"之下"显示，而内容在浮动元素"之上"显示。
 ```
a标签的样式规划（避免过度设计）：
a{color:#06C;text-decoration:none;}
a:hover{color:#F90;text-decoration:underline;}
.normal a{color:#666;}
.normal a:hover{color:#000;}
.list a:visied{color:#969;}
```






<div class="tiles">
{% for post in site.categories.pagenotes %}
{% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles 把所有categories 有 pagenotes 的列出来-->
