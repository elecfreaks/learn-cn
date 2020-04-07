# 课程_02 按钮

![](./images/SVbSfPB.jpg)

## 简介
---
在上一个实验中，我们已经学习了如何让micro:bit控制2颗LED灯交替闪烁。这次我们将使用一个按钮来控制LED灯的闪烁。当我们按下按钮，2颗LED灯会交替闪烁；松开按钮，LED灯就会停止闪烁。 

## 元件清单
---
### 硬件：
- 1 x micro:bit
- 1 x USB线  
- 1 x micro:bit面包板扩展板
- 1 x 面包板83x55 mm
- 2 x LED  
- 2 x 100欧姆电阻  
- 1 x 瞬时按钮开关  
- 若干跳线

**温馨提示：如果你需要以上所有元件，你可以购买我们的[Elecfreaks小小科学家套件](https://item.taobao.com/item.htm?spm=a1z10.1-c-s.w4024-17803785896.2.18dc3f94XOgpWg&id=562837851877&scene=taobao_shop)。**

![](./images/W4tseua.jpg)

## 主要元件介绍
---
### 瞬时按钮开关

这是一个用来控制电子设备的普通元件。它大部分用于连接或者切断控制电路，从而实现电机或者其他电子设备的控制。
瞬时按钮开关通常是保持开启的。当它被按下的时候，电路就接通了；当它被弹起的时候，它就会跳回到未连接的状态。

![](./images/IO2KzaW.jpg)

瞬时按钮开关有4个引脚。这4个引脚可以被分为2组：引脚1短接引脚2，引脚3短接引脚4。

![](./images/OgWZfBQ.jpg)


## 实验步骤
---
### 硬件连接
根据下面的图片将你的元件连接起来：

- 1.将led灯的短引脚与GND连接

- 2.将led灯的长引脚通过电阻，与P0口与P1口连接

- 3.将瞬时开关与P2口连接

![](./images/qXKoSN4.jpg) 

连接完成后如图:

![](./images/uGLigLh.jpg)

### 软件

[微软Makecode在线编辑器:makecode.microbit.org](https://makecode.microbit.org/)



### 如图所示编写程序

![](./images/case_02_01.png)

### 代码详解
- 1.在 当开机时 积木块中将P2口电位拉高。

![](./images/case_02_02.png)

- 2.读取P2口的状态，判断按钮是否按下，当按钮被按下，将P0口写入数字信号0，关闭led，将P1口写入数字信号1，打开led，延迟500ms，将P0口写入数字信号1，打开led，将P1口写入数字信号0，关闭led，延迟500ms。

![](./images/case_02_03.png)

### 参考程序
请参考程序连接：[https://makecode.microbit.org/_T585WeYwVWtv](https://makecode.microbit.org/_T585WeYwVWtv)

你也可以通过以下网页直接下载程序，下载完成后即可开始运行程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_T585WeYwVWtv" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

## 实验结果
---
当你按下按钮，你可以看到2颗LED灯交替闪烁；松开按钮，这两颗LED灯就停止闪烁。如果不是这样的话，请返回之前的步骤，检查你的操作。

![](./images/7w5yp6z.gif)


## 思考
---
如果我们想按下按钮点亮红色的LED灯，松开按钮点亮绿色的LED等，那么我们该如何编程呢？
## 常见问题
--- 

## 更多信息，欢迎访问：
---
[micro:bit知识库地址](https://www.elecfreaks.com/learn-cn/)       
micro:bit官方推荐供应商：[恩孚科技淘宝店](https://shop69086944.taobao.com/?spm=a230r.7195193.1997079397.2.RSthR0)     
QQ技术交流群：570756726     

