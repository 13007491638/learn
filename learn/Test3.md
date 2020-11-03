# 第三阶段

## 一、HTML



### HTML基础

**H**yper **T**ext **M**arkup **L**anguage，是一种标记语言而不是编程语言，标记语言本身就是一整套的标记标签来描述一个网页（告诉游览器如何构造整个页面）。

ps标记语言与编程语言的区别：标记语言是被动的，本身没有行为能力的，不处理逻辑问题（负责发号施令，像军师），所有的逻辑问题都会丢到后台给js脚本之类的来进行处理；而编程语言则是需要编译执行，且本身具有行为能力/逻辑能力的（可以处理问题）。

一句正常的HTML Element（HTML语句）前后分别有opening tag& closing tag,，tag中间就是Content文本内容。

### HTML语法

**<标签 属性="某某特定属性">**

每一个HTML标签元素都可以拥有其属性，主要属性为：

* class：规定元素类名
* id：规定元素唯一ID
* style：规定元素行内样式
* title：规定元素额外信息



### Tag

tag：不同的tag标志着其中的文本有不同的表现形式。 

```c
<html>:定义了整个HTML文档
<head>：对整个html文件起一个说明的作用
<body>：文本主体
<h1>:标题
<p>:paragraph
<div>:一整块,无特殊含义,仅为文本的容器
<span>:一整条(内联元素),无特殊含义,仅为文本容器

<br>:加一空行,编辑中需要换新行
<br/>:在编辑过程中不需要换新行也能达到输出效果换行
<hr>:分割线 
    
<q>:短引用
<blockquote>:长引用
<quote>:引用
<abbr>:下划线式的文本注释
<cite>:斜体引言
<address>:文档或文章的联系信息（一般是斜体显示）
<bdo>:一串文本反着写
    
<var>:数学变量
<input>:输入，通过改变输入的不同属性获得不同的输入结果
<button>:按钮
    
<!DOCTYPE html>:解释文档的类型
<ul> <li>:无序list
<ol> <li>:有序list
    
<table>:表格
<thead>:表头(table head格式控制标签)
<tr>:行内容(table row)
<th>:表头文本内容
<tbody>:表身内容
<td>:表身文本内容(table data) 
    
<img>:图像
    
<! -- 注释 -->
    
<link>:关联css文件(添加在head tag中)

```

![image-20201101161217701](C:\Users\29297\AppData\Roaming\Typora\typora-user-images\image-20201101161217701.png)

href即指定的超链接（可设定其他的属性：背景/居中/边框）

attribute：html属性

## Inline and Block Level Element

### 块级元素

* 在页面以块的形式展示

* 出现在新的一行

* 占全部宽度

<h 1> <div> <h6> <p>都是块级元素（或者说叫块级标签??）


### 内联元素

* 在块级元素内（相当于储物柜和抽屉）

* 不换行

* 只占所需的宽度

<a> <img> <em> <strong> 



## 二、CSS

### CSS基础

**C**ascading **S**tylesheets（层叠样式表），不是一门编程语言，是用来告诉游览器如何指定页面**样式**和**布局**



### 添加CSS的三种方法

* 外部样式表

  * CSS保存在.css文件中

  * 在HTML里使用<link>引用

  * ```
    <head>
    <link rel="stylesheet" type="text/css" href="mystyle.css">
    </head>
    ```

* 内部样式表

  * 不使用外部的CSS文件，直接写在当前的html文件内

  * 将CSS放在HTML的<style>里

  * ```
    <head>
    
    <style type="text/css">
    body {background-color: red}
    p {margin-left: 20px}
    </style>
    </head>
    ```

* 内联样式

  * 只影响单个元素（单个添加）

  * 在HTML元素的style属性中添加

  * 不推荐，难以维护

  * ```
    <p style="color: red; margin-left: 20px">
    This is a paragraph
    </p>
    ```

### CSS中三种属性的选择方法

![image-20201101205420342](C:\Users\29297\AppData\Roaming\Typora\typora-user-images\image-20201101205420342.png)

* 直接通过tag指定
* 通过类名——  **.class**来指定（class可以选择一个改变多个)
* 通过ID——  **#ID**来指定（要确保这个ID具有唯一性）

### CSS中的属性

* background-color：背景颜色

* color：颜色
* width：宽度控制

* margin：边界控制

* font-family：字体
  * sans-serif无衬线体	serif有衬线体
  * 如果字体有多个词（有空格）就要加双引号
  * monospace 等宽	

* font-size：字体大小

* front-weight：字重

* 以上有关字体的可统一通过font：+各种属性 来调整

  

* text-align：文本的水平对齐

* letter-spacing：字间距

* word-spacing：词间距

* line-hight：行高

  

* margin-top/margin-right/margin-bottom/margin-left：边距宽度（按严格的顺时针可以快速定义）

### CSS里的颜色

css用来调用color属性的六种不同方式

* 关键词：black
* 十六进制值：#ff0000
* RGB：rgb（255，0，0）
* HSL：hsl(0,100%,50%)（灰度值?)——（hue色相,saturation饱和度,lightness明度）
* RGBA：rgb(255,0,0,0.5)（最后一个值为α通道，用来控制其透明值，数值在0~1）
* HSLA：hsl(0,100%，50%，0.5)（同上）

<img src="C:\Users\29297\AppData\Roaming\Typora\typora-user-images\image-20201101211427674.png" alt="image-20201101211427674" style="zoom:80%;" />

### BOX模型

<img src="C:\Users\29297\AppData\Roaming\Typora\typora-user-images\image-20201102202524664.png" alt="image-20201102202524664" style="zoom: 50%;" />

* content：可以说是一张图或者上下顶边的文字
* border：边框（p/h1是0边框）
* padding：内边距——内容和边框的距离
* border：边框（其实只是很窄的一条线）
* margin：外边距

当两个盒子靠在一起的时候只会自动选择两者中margin较大的那一个作为边距（外边距塌陷）。

## JavaScript 

### JS基础

* 是解释型的一种编程语言,可以在网页上实现一些复杂的功能与交互
  * 不需要预先编译,是游览器(客户端)边运行边解释
  * 面向对象语言

* 三种添加JS的方法
  * 内部的JS:使用script的tag标签
  * 外部的JS:<script src="script.js"></script>通过js的link导入外部js
  * 内联的JS:直接在各个tag中的属性添加``<button onclick="createParagraph()"> Click me  </button>``

### JS语法

* JS没有整数和浮点数的区别,整数也算是一种浮点数(其实都是Number类型,在内存中用指数加尾数表示,所以0.1+0.2≠0.3)

### JS编程

* albert():类似于python的语法,放什么怎么放就展示什么
* console.log():在浏览器console控制台中进行操作
  * "word".length:求word的长度
  * "word".charAt(X):求该word中第X位的元素
  * "word".replace("X","Y"):把word中的X元素换成Y元素
  * "word".toupperCase:转大写
  * 用"空字符"＋**.** 运算符可以查看对字符串的一系列操作(都有操作说明)

* 布尔运算符在console控制台中都可以操作判断(**<>= &&||**)

#### JS变量

* var定义新建变量:var name="XX";(变量名为name)
* let定义新建变量:let a=1;(变量名为a)
* const声明常量(不可修改)

#### JS运算符

* 字符串也是可以用+来结合的
  * 运算过程从数字向字符串转换("3"+4+5=345)(也叫类型自动转换)
  * 但是是从左向右运算,所以有特殊情况 3+4+"5"=75

* ==和===的区别:三等号严格判等,不进行类型自动转换

#### JS控制结构

* 经典if  else逻辑判断控制
* while(条件成立){}
*  