---
title: 前端面试题
categories:
    - 学习
tags:
    - JavaScript
    - HTML
    - CSS
    - http
    - 前端
toc: true
comments: true
---
### HTML面试题<br><br>

1.XHTML和HTML有什么区别
> - HTML是一种基本的WEB网页设计语言，XHTML是一个基于XML的置标语言
>最主要的不同：
>- XHTML 元素必须被正确地嵌套。
>- XHTML 元素必须被关闭。
>- 标签名必须用小写字母。
>- XHTML 文档必须拥有根元素。

<!-- more -->

2.前端页面有哪三层构成，分别是什么?作用是什么?
> - 结构层 Html 表示层 CSS 行为层 js;
3.你做的页面在哪些流览器测试过?这些浏览器的内核分别是什么?
>- Ie(Ie内核) 火狐（Gecko） 谷歌（webkit,Blink） opera(Presto),Safari(wbkit)

4.什么是语义化的HTML?
>- 直观的认识标签 对于搜索引擎的抓取有好处，用正确的标签做正确的事情！
  >-  html语义化就是让页面的内容结构化，便于对浏览器、搜索引擎解析；
  > 在没有样式CCS情况下也以一种文档格式显示，并且是容易阅读的。搜索引擎的爬虫依赖于标记来确定上下文和各个关键字的权重，利于 SEO。
   >- 使阅读源代码的人对网站更容易将网站分块，便于阅读维护理解。

5.HTML5 为什么只需要写 !DOCTYPE HTML？
> - HTML5 不基于 SGML，因此不需要对DTD进行引用，但是需要doctype来规范浏览器的行为（让浏览器按照它们应该的方式来运行）；而HTML4.01基于SGML,所以需要对DTD进行引用，才能告知浏览器文档所使用的文档类型。

6.Doctype作用？标准模式与兼容模式各有什么区别?
>- !DOCTYPE声明位于位于HTML文档中的第一行，处于html 标签之前。告知浏览器的解析器用什么文档标准解析这个文档。DOCTYPE不存在或格式不正确会导致文档以兼容模式呈现。
> - 标准模式的排版 和JS运作模式都是以该浏览器支持的最高标准运行。在兼容模式中，页面以宽松的向后兼容的方式显示,模拟老式浏览器的行为以防止站点无法工作。

7.html5有哪些新特性、移除了那些元素？如何处理HTML5新标签的浏览器兼容问题？如何区分 HTML 和
HTML5？
> - HTML5 现在已经不是 SGML 的子集，主要是关于图像，位置，存储，多任务等功能的增加。
> - 绘画 canvas
>- 用于媒介回放的 video 和 audio 元素
>- 本地离线存储 localStorage 长期存储数据，浏览器关闭后数据不丢失；
>- sessionStorage 的数据在浏览器关闭后自动删除
> - 语意化更好的内容元素，比如 article、footer、header、nav、section
>- 表单控件，calendar、date、time、email、url、search
>- 新的技术webworker, websockt, Geolocation
> 移除的元素
>- 纯表现的元素：basefont，big，center，font, s，strike，tt，u；
>- 对可用性产生负面影响的元素：frame，frameset，noframes；
> 支持HTML5新标签：
> - IE8/IE7/IE6支持通过document.createElement方法产生的标签，
>- 可以利用这一特性让这些浏览器支持HTML5新标签，
>- 浏览器支持新标签后，还需要添加标签默认的样式：

8.请描述一下 cookies，sessionStorage 和 localStorage 的区别？
>  - cookie在浏览器和服务器间来回传递。 sessionStorage和localStorage不会
>  - sessionStorage和localStorage的存储空间更大；
>  - sessionStorage和localStorage有更多丰富易用的接口；
>  - sessionStorage和localStorage各自独立的存储空间；

9.如何实现浏览器内多个标签页之间的通信?
> - 调用localstorge、cookies等本地存储方式

### CSS面试题<br><br>
 1.简要说一下CSS的元素分类
>- 块级元素：div,p,h1,form,ul,li;
>- 行内元素 :  span>,a,label,input,img,strong,em;

 2.CSS隐藏元素的几种方法（至少说出三种）
>  - Opacity:元素本身依然占据它自己的位置并对网页的布局起作用。它也将响应用户交互;
>  - Visibility:与 opacity 唯一不同的是它不会响应任何用户交互。此外，元素在读屏软件中也会被隐藏;
>  - Display:display 设为 none 任何对该元素直接打用户交互操作都不可能生效。此外，读屏软件也不会读到元素的内容。这种方式产生的效果就像元素完全不存在;
>  - Position:不会影响布局，能让元素保持可以操作;
>  - Clip-path:clip-path 属性还没有在 IE 或者 Edge 下被完全支持。如果要在你的 clip-path 中使用外部的 SVG 文件，浏览器支持度还要低;

 3.CSS清除浮动的几种方法（至少两种）
> - 使用带clear属性的空元素
> - 使用CSS的overflow属性；
> - 使用CSS的:after伪元素；
> - 使用邻接元素处理；

 4.CSS居中（包括水平居中和垂直居中）
>### 内联元素居中方案
>**水平居中设置：**
>1.行内元素
> - 设置 text-align:center；

>2.Flex布局
 >- 设置display:flex;justify-content:center;(灵活运用,支持Chroime，Firefox，IE9+)
 >
 >**垂直居中设置：**
 >1.父元素高度确定的单行文本（内联元素）
 > - 设置 height = line-height；

 >2.父元素高度确定的多行文本（内联元素）
  >- a:插入 table （插入方法和水平居中一样），然后设置 vertical-align:middle；
  >- b:先设置 display:table-cell 再设置 vertical-align:middle；
>### 块级元素居中方案
>**水平居中设置：**
  >1.定宽块状元素
  > - 设置 左右 margin 值为 auto；

 > 2.不定宽块状元素
 >  - a:在元素外加入 table 标签（完整的，包括 table、tbody、tr、td），该元素写在 td 内，然后设置 margin 的值为 auto；
 >  - b:给该元素设置 displa:inine 方法；
 >  - c:父元素设置 position:relative 和 left:50%，子元素设置 position:relative 和 left:50%；
 >  
 > **垂直居中设置：**
 >   - 使用position:absolute（fixed）,设置left、top、margin-left、margin-top的属性;
 >   - 利用position:fixed（absolute）属性，margin:auto这个必须不要忘记了;
 >   - 利用display:table-cell属性使内容垂直居中;
 >   - 使用css3的新属性transform:translate(x,y)属性;
 >   - 使用:before元素;

 5.写出几种IE6 BUG的解决方法
 >- 双边距BUG float引起的 使用display
 >- 3像素问题 使用float引起的 使用dislpay:inline -3px
 >- 超链接hover 点击后失效 使用正确的书写顺序 link visited hover active
 >- Ie z-index问题 给父级添加position:relative
 >- Png 透明 使用js代码 改
 >- Min-height 最小高度 ！Important 解决’
 >- select 在ie6下遮盖 使用iframe嵌套
 >- 为什么没有办法定义1px左右的宽度容器（IE6默认的行高造成的，使用over:hidden,zoom:0.08 line-height:1px）

 6.对于SASS或是Less的了解程度？喜欢那个？
> - 语法介绍

 7.Bootstrap了解程度
> - 特点，排版，插件的使用;

 8.页面导入样式时，使用link和@import有什么区别？
> - link属于XHTML标签，除了加载CSS外，还能用于定义RSS, 定义rel连接属性等作用；而@import是CSS提供的，只能用于加载CSS;
> - 页面被加载的时，link会同时被加载，而@import引用的CSS会等到页面被加载完再加载;
> - import是CSS2.1 提出的，只在IE5以上才能被识别，而link是XHTML标签，无兼容问题;

 9.介绍一下CSS的盒子模型？
 > - 有两种， IE 盒子模型、标准 W3C 盒子模型；IE的content部分包含了 border 和 pading;
 >- 盒模型： 内容(content)、填充(padding)、边界(margin)、 边框(border).

 10.CSS 选择符有哪些？哪些属性可以继承？优先级算法如何计算？ CSS3新增伪类有那些？
 > - id选择器（ # myid）
 > - 类选择器（.myclassname）
 > - 标签选择器（div, h1, p）
 > - 相邻选择器（h1 + p）
 > - 子选择器（ul > li）
 > - 后代选择器（li a）
 > - 通配符选择器（ * ）
 > - 属性选择器（a[rel = "external"]）
 > - 伪类选择器（a: hover, li: nth - child）
>- 可继承的样式： font-size font-family color, UL LI DL DD DT;
> - 不可继承的样式：border padding margin width height ;
> - 优先级就近原则，同权重情况下样式定义最近者为准;
> - 优先级为:
      !important >  id > class > tag
      important 比 内联优先级高

 11.CSS3有哪些新特性？
 > - CSS3实现圆角（border-radius:8px），阴影（box-shadow:10px），
  >   对文字加特效（text-shadow、），线性渐变（gradient），旋转（transform）
 > - transform:rotate(9deg) scale(0.85,0.90) translate(0px,-30px) skew(-9deg,0deg);//旋转,缩放,定位,倾斜
   >  增加了更多的CSS选择器  多背景 rgba

## JavaScript面试题

 1.javascript的typeof返回哪些数据类型
> - Ｏbject number function boolean underfind;

 2.例举3种强制类型转换和2种隐式类型转换?
> - 强制（parseInt,parseFloat,number）隐式（== – ===）；

 3.数组方法pop() push() unshift() shift()
> - Push()尾部添加 pop()尾部删除
> - Unshift()头部添加 shift()头部删除

 4.ajax请求的时候get 和post方式的区别?
> - 一个在url后面 一个放在虚拟载体里面
>有大小限制
>- 安全问题
>应用不同 一个是论坛等只需要请求的，一个是类似修改密码的;

 5.call和apply的区别
> - Object.call(this,obj1,obj2,obj3)
>- Object.apply(this,arguments)

 6.ajax请求时，如何解释json数据
> - 使用eval parse,鉴于安全性考虑 使用parse更靠谱;

 7.事件委托是什么
> - 让利用事件冒泡的原理，让自己的所触发的事件，让他的父元素代替执行！

 8.闭包是什么，有什么特性，对页面有什么影响?简要介绍你理解的闭包
> - 闭包就是能够读取其他函数内部变量的函数。

 9.添加 删除 替换 插入到某个接点的方法
>obj.appendChidl()
>obj.innersetBefore
>obj.replaceChild
>obj.removeChild

 10.说一下什么是javascript的同源策略？
> - 一段脚本只能读取来自于同一来源的窗口和文档的属性，这里的同一来源指的是主机名、协议和端口号的组合

 11.编写一个b继承a的方法;
```
function A(name){
    this.name = name;
    this.sayHello = function(){alert(this.name+” say Hello!”);};
}
function B(name,id){
    this.temp = A;
    this.temp(name);        //相当于new A();
    delete this.temp;       
     this.id = id;   
    this.checkId = function(ID){alert(this.id==ID)};
}
```

 12.如何阻止事件冒泡和默认事件
 ```
function stopBubble(e)
{
    if (e && e.stopPropagation)
        e.stopPropagation()
    else
        window.event.cancelBubble=true
}
return false
```

 13.下面程序执行后弹出什么样的结果?

```
function fn() {
    this.a = 0;
    this.b = function() {
        alert(this.a)
    }
}
fn.prototype = {
    b: function() {
        this.a = 20;
        alert(this.a);
    },
    c: function() {
        this.a = 30;
        alert(this.a);
    }
}
var myfn = new fn();
myfn.b();
myfn.c();
```

 14.谈谈This对象的理解。
>this是js的一个关键字，随着函数使用场合不同，this的值会发生变化。
>   但是有一个总原则，那就是this指的是调用函数的那个对象。
>   this一般情况下：是全局对象Global。 作为方法调用，那么this就是指这个对象



 15.下面程序的结果
```
function fun(n,o) {
  console.log(o)
  return {
    fun:function(m){
      return fun(m,n);
    }
  };
}
var a = fun(0);  a.fun(1);  a.fun(2);  a.fun(3);
var b = fun(0).fun(1).fun(2).fun(3);
var c = fun(0).fun(1);  c.fun(2);  c.fun(3);
```
>//答案：
>//a: undefined,0,0,0
>//b: undefined,0,1,2
>//c: undefined,0,1,1

 16.下面程序的输出结果
```
var name = 'World!';
(function () {
    if (typeof name === 'undefined') {
        var name = 'Jack';
        console.log('Goodbye ' + name);
    } else {
        console.log('Hello ' + name);
    }
})();
```

 17.了解Node么？Node的使用场景都有哪些？
> - 高并发、聊天、实时消息推送

 18.介绍下你最常用的一款框架
 >  - jquery,rn,angular等;

 19.对于前端自动化构建工具有了解吗？简单介绍一下
>- Gulp,Grunt等；

 20.介绍一下你了解的后端语言以及掌握程度

### 其它
<br>
 1.对Node的优点和缺点提出了自己的看法？
> (优点）
>      因为Node是基于事件驱动和无阻塞的，所以非常适合处理并发请求，
>      因此构建在Node上的代理服务器相比其他技术实现（如Ruby）的服务器表现要好得多。
>     此外，与Node代理服务器交互的客户端代码是由javascript语言编写的，
 >     因此客户端和服务器端都用同一种语言编写，这是非常美妙的事情。
 > （缺点）
 >      Node是一个相对新的开源项目，所以不太稳定，它总是一直在变，
 >     而且缺少足够多的第三方库支持。看起来，就像是Ruby/Rails当年的样子。

 2.你有哪些性能优化的方法？
 > （1） 减少http请求次数：CSS Sprites, JS、CSS源码压缩、图片大小控制合适；网页Gzip，CDN托管，data缓存 ，图片服务器。
 >  （2）前端模板 JS+数据，减少由于HTML标签导致的带宽浪费，前端用变量保存AJAX请求结果，每次操作本地变量，不用请求，减少请求次数
 > （3） 用innerHTML代替DOM操作，减少DOM操作次数，优化javascript性能。
 > （4） 当需要设置的样式很多时设置className而不是直接操作style。
 > （5） 少用全局变量、缓存DOM节点查找的结果。减少IO读取操作。
 > （6） 避免使用CSS Expression（css表达式)又称Dynamic properties(动态属性)。
 > （7） 图片预加载，将样式表放在顶部，将脚本放在底部  加上时间戳。
 > （8） 避免在页面的主体布局中使用table，table要等其中的内容完全下载之后才会显示出来，显示div+css布局慢。对普通的网站有一个统一的思路，就是尽量向前端优化、减少数据库操作、减少磁盘IO。向前端优化指的是，在不影响功能和体验的情况下，能在浏览器执行的不要在服务端执行，能在缓存服务器上直接返回的不要到应用服务器，程序能直接取得的结果不要到外部取得，本机内能取得的数据不要到远程取，内存能取到的不要到磁盘取，缓存中有的不要去数据库查询。减少数据库操作指减少更新次数、缓存结果减少查询次数、将数据库执行的操作尽可能的让你的程序完成（例如join查询），减少磁盘IO指尽量不使用文件系统作为缓存、减少读写文件次数等。程序优化永远要优化慢的部分，换语言是无法“优化”的。
>    
3.http状态码有那些？分别代表是什么意思？
> 100-199 用于指定客户端应相应的某些动作。
> 200-299 用于表示请求成功。
> 300-399 用于已经移动的文件并且常被包含在定位头信息中指定新的地址信息。
> 400-499 用于指出客户端的错误。400    1、语义有误，当前请求无法被服务器理解。401    当前请求需要用户验证 403    服务器已经理解请求，但是拒绝执行它。
> 500-599 用于支持服务器错误。 503 – 服务不可用
4.一个页面从输入 URL 到页面加载显示完成，这个过程中都发生了什么？（流程说的越详细越好）

 > - 查找浏览器缓存
 > -  DNS解析、查找该域名对应的IP地址、重定向（301）、发出第二个GET请求
 > - 进行HTTP协议会话
 > - 客户端发送报头(请求报头)
 > - 文档开始下载
 > - 文档树建立，根据标记请求所需指定MIME类型的文件
 > - 文件显示
 > - 浏览器这边做的工作大致分为以下几步：
 > - 加载：根据请求的URL进行域名解析，向服务器发起请求，接收文件（HTML、JS、CSS、图象等）。
 > - 解析：对加载到的资源（HTML、JS、CSS等）进行语法解析，建议相应的内部数据结构（比如HTML的DOM树，JS的（对象）属性表，CSS的样式规则等等）


 5.你常用的开发工具是什么，为什么？
 > - Sublime,Atom,Nodepad++;


 6.说说最近最流行的一些东西吧？常去哪些网站？
 > -  Node.js、MVVM、React-native,Angular,Weex等
 > - CSDN,Segmentfault,博客园,掘金,Stackoverflow等


 7.介绍下你的项目（如果有的话）？并说一下在做这个项目中运用的技术以及遇到的难题是如何解决的
