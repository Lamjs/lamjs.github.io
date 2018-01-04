---
layout: archive
title: "网页笔记"
date: 2017-12-30T11:40:45-04:00
modified:
excerpt: "等一下"
tags: []
---
1.标题：文字前插入1~6个#号
```
# 这是md语言笔记1
## 这是md语言笔记21
###### 这是md语言笔记6
```
效果如：
# 这是md语言笔记1
## 这是md语言笔记21
###### 这是md语言笔记6

2.有序列表：正常输入序号，自动纠错
```
1. 有序列表
1. 有序列表
4. 有序列表
```
效果如：
1. 有序列表
1. 有序列表
4. 有序列表

3.无序列表：文字前增加 * 或 - 号
```
* 无序列表
* 无序列表
```
效果如：
* 无序列表
* 无序列表

4. 插入图片： 
```！[]()```
![](http://cdn.wiz.cn/wp-content/uploads/2015/06/wiz_logo.png)

5. 粗体、斜体、删除线：
```
粗体：在文字前后添加 ** (注意符号与文字间不要有空格）
斜体：在文字前后添加 *
删除线：在文字前后添加 ~~
```
效果如：
**粗体**
*斜体*
~~删除线~~

6.引用：
```
在文字前 添加 
>你好，再见
```
效果如：
>你好，再见

7.表格
```
| 十年|二十年 | 三十年 |
|------------|-----------|--------|
| 是我 | 还是我| 不是我 |
```
效果如：
！[](https://github.com/Lamjs/Lamjs.github.io/blob/master/images/gongshi.jpg)

8.目录：顶部加[TOC]，配合#号使用

[TOC]
###Markdown 是什么
####Markdown 的好处

9.数学公式编辑：涉及Mathjax语法
```
可以创建行内公式，例如：$\Gamma(n) = (n-1)!\quad\forall n\in\mathbb N$
或者块级公式，
$$ x = \dfrac{-b \pm \sqrt{b^2 - 4ac}}{2a} $$
```
效果如：
$\Gamma(n) = (n-1)!\quad\forall n\in\mathbb N$
或者块级公式，
$$ x = \dfrac{-b \pm \sqrt{b^2 - 4ac}}{2a} $$

10.流程图：略显复杂，请仔细观看示例
```
Andrew->China: Says Hello
Note right of China: China thinks\nabout it
China-->Andrew: How are you?
Andrew->>China: I am good thanks!
```
效果如：
Andrew->China: Says Hello
Note right of China: China thinks\nabout it
China-->Andrew: How are you?
Andrew->>China: I am good thanks!
    
11.时序图：

```sequence
Alice->Bob: Hello Bob, how are you?
Note right of Bob: Bob thinks
Bob-->Alice: I am good thanks!
``` 
效果如：
Alice->Bob: Hello Bob, how are you?
Note right of Bob: Bob thinks
Bob-->Alice: I am good thanks!

以上就是我力所能及的事情，勿喷。
    
{% for post in site.categories.pagenotes %}
  {% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles 把所有categories 有 pagenotes 的列出來-->
