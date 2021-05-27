

# 课程_01 LED

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/Starter_Kit/images/case_01_01.jpg)

## 简介
---
LED灯的应用非常广泛。在日常生活中，我们看到的大部分信号灯都采用了LED灯作为它的主要光源。在今天的实验中，我们将要用micro:bit使2颗LED灯交替闪烁。 

## 元件清单
---
### 硬件：
- 1 x micro:bit
- 1 x USB线  
- 1 x micro:bit面包板扩展板
- 1 x 面包板83x55mm 
- 2 x LED  
- 2 x 100欧姆电阻  
- 若干跳线

**温馨提示：如果你需要以上所有元件，你可以购买我们的[Elecfreaks小小科学家套件](https://item.taobao.com/item.htm?ft=t&id=597096675822)。**

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/Starter_Kit/images/case_01_02.jpg)

## 主要元件介绍
---
### micro:bit面包板扩展板
micro:bit面包板扩展板可以在面包板上扩展出micro:bit的所有引脚，方便我们在面包板上制作简单的电路。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/Starter_Kit/images/case_01_03.jpg)
 
下面这张图片显示了如何将面包板扩展板插入到面包板上。面包板扩展板可以适用于各种规格的面包板。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/Starter_Kit/images/case_01_04.jpg)

### LED
LED是Light Emitting Diode（发光二极管）的缩写。这是一种半导体二极管。它可以将电能转换成光能。当电流经过的时候，它就会发光。
 
![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/Starter_Kit/images/case_01_05.jpg)

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/Starter_Kit/images/case_01_06.jpg)
 
如果你仔细看看LED，你就会发现它的两个特点。一个是它的引脚的长度不一致，另一个是LED的一侧是扁平的，而不是圆柱形。这些特征可以告诉你哪个引脚是阳极（正极），哪个引脚是阴极（负极）。长一些的引脚连接正极供电（3.3v),带有扁平一侧的引脚连接接地。

### 电阻
电阻是一种用于控制电流的元件。它可以限制所连接的电路的电流。在我们的实验中，我们使用了100欧姆的电阻。如果不限制电流的话，就会损坏LED灯。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/Starter_Kit/images/case_01_07.jpg)

想通过色环来识别电阻的阻值吗？你可以阅读这篇文章：
[How to Identify Color Circle Resistance Value](https://www.elecfreaks.com/9158.html).

## 实验步骤
---
### 硬件连接
根据下面的图片将你的元件连接起来：

- 1.将led灯的短引脚与GND连接

- 2.将led灯的长引脚通过电阻，与P0口与P1口连接
![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/Starter_Kit/images/case_01_08.jpg)

连接完成后如图:

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/Starter_Kit/images/case_01_09.jpg)

### 软件

[微软Makecode在线编辑器:makecode.microbit.org](https://makecode.microbit.org/)



### 如图所示编写程序

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/Starter_Kit/images/case_01_11.png)

### 代码详解
- 1.将P0口写入数字信号0，关闭led，将P1口写入数字信号1，打开led，延迟500ms。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/Starter_Kit/images/case_01_12.png)

- 2.将P0口写入数字信号1，打开led，将P1口写入数字信号0，关闭led，延迟500ms。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/Starter_Kit/images/case_01_13.png)

### 参考程序
请参考程序连接：[https://makecode.microbit.org/_LybdqfauX3TR](https://makecode.microbit.org/_LybdqfauX3TR)

你也可以通过以下网页直接下载程序，下载完成后即可开始运行程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_LybdqfauX3TR" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

## 实验结果
---
你可以看到两颗LED灯交替闪烁。如果不是这样的话，请返回之前的步骤，检查你的操作。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/Starter_Kit/images/case_01_14.gif)


## 思考
---
如果我们想控制4颗LED灯，让它们依次被点亮，那么我们该如何设计电路和编程呢？

## 常见问题
---

## 更多信息，欢迎访问：
---
[micro:bit知识库地址](https://www.elecfreaks.com/learn-cn/)    
micro:bit官方推荐供应商：[恩孚科技淘宝店](https://shop69086944.taobao.com/?spm=a230r.7195193.1997079397.2.RSthR0)  
QQ技术交流群：570756726   



