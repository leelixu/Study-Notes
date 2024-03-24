---
Title: HTML学习
C_time: 2023-07-22-16:58
Done_time: NA
Status: Undone
draft: false
Tag:
- HTML
---


链接：[HTML 教程](https://www.runoob.com/html/html-tutorial.html)

# 一、简介

## 超文本标记语言
（HyperText Markup Language，简称：HTML）是一种用于创建网页的标准标记语言。

HTML 是用来描述网页的一种语言。

- HTML 指的是超文本标记语言: **H**yper**T**ext **M**arkup **L**anguage
- HTML 不是一种编程语言，而是一种**标记**语言
- 标记语言是一套**标记标签** (markup tag)
- HTML 使用标记标签来**描述**网页
- HTML 文档包含了HTML **标签**及**文本**内容
- HTML文档也叫做 **web 页面**

可以使用 HTML 来建立自己的 WEB 站点，HTML 运行在浏览器上，由浏览器来解析。

## HTML文档的后缀名

- .html
- .htm

以上两种后缀名没有区别，都可以使用

## 实例解析

![[Pasted image 20230730005802.png]]

- **<!DOCTYPE html>** 声明为 HTML5 文档
- **\<html>** 元素是 HTML 页面的根元素
- **\<head>** 元素包含了文档的元（meta）数据，如 \<meta charset="utf-8"> 定义网页编码格式为 **utf-8**。
- **\<title>** 元素描述了文档的标题
- **\<body>** 元素包含了可见的页面内容
- **\<h1>** 元素定义一个大标题
- **\<p>** 元素定义一个段落

**注：**在浏览器的页面上使用键盘上的 F12 按键开启调试模式，就可以看到组成标签。

## HTML 标签

HTML 标记标签通常被称为 HTML 标签 (HTML tag)。

- HTML 标签是由_尖括号_包围的关键词，比如\<html> 
- HTML 标签通常是_成对出现_的，比如 \<b> 和 \</b>
- 标签对中的第一个标签是**开始标签**，第二个标签是**结束标签**
- 开始和结束标签也被称为**开放标签**和**闭合标签**

> <标签>内容</标签>

## HTML 元素

"HTML 标签" 和 "HTML 元素" 通常都是描述同样的意思.

但是严格来讲, 一个 HTML 元素包含了开始标签与结束标签，如下实例:

HTML 元素:

>\<p>这是一个段落。\</p>

## Web 浏览器

Web浏览器（如谷歌浏览器，Internet Explorer，Firefox，Safari）是用于读取HTML文件，并将其作为网页显示。

浏览器并不是直接显示的HTML标签，但可以使用标签来决定如何展现HTML页面的内容给用户：

![[Pasted image 20230730011037.png]]

## HTML 网页结构

下面是一个可视化的HTML页面结构：

![[Pasted image 20230730011118.png]]

>只有 \<body> 区域 (白色部分) 才会在浏览器中显示。

## HTML版本

从初期的网络诞生后，已经出现了许多HTML版本:

|版本|发布时间|
|---|---|
|HTML|1991|
|HTML+|1993|
|HTML 2.0|1995|
|HTML 3.2|1997|
|HTML 4.01|1999|
|XHTML 1.0|2000|
|HTML5|2012|
|XHTML5|2013|

## <!DOCTYPE> 声明

\<!DOCTYPE>声明有助于浏览器中正确显示网页。

网络上有很多不同的文件，如果能够正确声明HTML的版本，浏览器就能正确显示网页内容。

doctype 声明是不区分大小写的，以下方式均可：
```
<!DOCTYPE html>  
  
<!DOCTYPE HTML>  
  
<!doctype html>  
  
<!Doctype Html>
```

## 通用声明

### HTML5
```
<!DOCTYPE html>
```

### HTML 4.01
```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"  
"http://www.w3.org/TR/html4/loose.dtd">
```

### XHTML 1.0
```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"  
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
```

## 中文编码

目前在大部分浏览器中，直接输出中文会出现中文乱码的情况，这时候我们就需要在头部将字符声明为 UTF-8 或 GBK。

```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>
页面标题</title>
</head>
<body>
 
<h1>我的第一个标题</h1>
 
<p>我的第一个段落。</p>
 
</body>
</html>
```


# 二、HTML 基础

## 1 HTML 标题

HTML 标题（Heading）是通过\<h1> - \<h6> 标签来定义的。

```
<h1>这是一个标题</h1>
<h2>这是一个标题</h2>
<h3>这是一个标题</h3>
```

**注释：** 浏览器会自动地在标题的前后添加空行。



## 2 HTML 段落

HTML 段落是通过标签 \<p> 来定义的。

```
<p>这是一个段落。</p>
<p>这是另外一个段落。</p>
```

## 3 HTML 链接

HTML 链接是通过标签 \<a> 来定义的。

```
<a href="https://www.runoob.com">这是一个链接</a>
```

**提示：** 在 href 属性中指定链接的地址。

## 4 HTML 图像

HTML 图像是通过标签 <img> 来定义的.

```
<img decoding="async" src="/images/logo.png" width="258" height="39" />
```

**注意：** 图像的名称和尺寸是以属性的形式提供的。



# 三、

