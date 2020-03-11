# 课程_14 环境光

![](./images/NkZTTdv.jpg)  

## 简介
---
在光敏传感器这个实验里，我们外接一个光敏传感器来感知外界光线，实际上，在micro:bit内部，也集成了一个光敏感应装置，本次实验，我们就用内部集成的光敏感应装置。当外界环境光比较暗时，点亮灯环。 

## 元件清单
---
### 硬件：
- 1 x micro:bit
- 1 x USB线
- 1 x micro:bit面包板扩展板
- 1 x 面包板83 x 55 mm
- 1 x LED七彩灯环（8颗灯珠) 
- 若干跳线

**温馨提示：如果你需要以上所有元件，你可以购买我们的[Elecfreaks小小科学家套件](https://item.taobao.com/item.htm?spm=a1z10.1-c-s.w4024-17803785896.2.18dc3f94XOgpWg&id=562837851877&scene=taobao_shop)。**

![](./images/W4tseua.jpg)

## 主要元件介绍
---
你可能好奇为什么micro:bit没有任何光传感器却能够感光。让我们一起来看看micro:bit官网上关于micro:bit屏幕的一段话：

micro:bit屏幕是由一个5x5的LED点阵构成。它作为一个3x9的矩阵连接到了micro:bit上。运行软件高速反复更新这个矩阵，正因为如此，它是位于用户视野范围内，并且不会检测到任何闪光。通过将一些LED驱动引脚反复切换成输入，并对电压衰减时间进行采样，这个LED矩阵也被应用于感应环境光，这和周围的环境光等级大致成正比。

![](./images/1JzFZG3.jpg) 

真是太不可思议啦！除了它的发光能力，micro:bit居然可以感光！因为LED通常被作为发光器来使用，所以我们很容易忘记它是基本的光电二极管，而且也是光检测器。如果并入LED驱动电路中，那么它的功能就能够被很好地展现，而无须任何额外的硬件。

## 实验步骤
---
### 硬件连接
根据下面的图片将你的元件连接起来：

- 将灯环的信号线与扩展板的P0口连接起来

![](./images/fKgQRoW.jpg)

连接完成后如图:

![](./images/Hacl6BL.jpg)

### 软件

[微软Makecode在线编辑器:makecode.microbit.org](https://makecode.microbit.org/)

![](./images/JHZUvh2.png)

### 添加Package
- 在MakeCode的代码抽屉中点击Advanced，查看更多代码选项。

![](./images/smtcNoB.png)

点击“Extensions”，在弹出的对话框中搜索“neopixel"，下载neopixel代码库。

![](./images/umQwUC2.png)

### 如图所示编写程序

![](./images/AZCjDfR.png)

### 代码详解
- 1.将扩展板P0口设置为灯环信号输出口，将色彩模式设置为RGB模式。

![](./images/ZlZCHyZ.png)

- 2.当micro:bit接收到的光照强度低于10，控制灯环发出七彩的光芒。

![](./images/XoTAOIf.png)

### 参考程序
请参考程序连接：[https://makecode.microbit.org/_70bWD0iuK6AT](https://makecode.microbit.org/_70bWD0iuK6AT)

你也可以通过以下网页直接下载程序，下载完成后即可开始运行程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_70bWD0iuK6AT" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

## 实验结果
---
在暗处，灯环点亮；在亮处，灯环熄灭。

![](./images/F9B9ySD.gif)


## 思考
---
当灯环亮起彩虹色后，让彩虹转动起来。该如何设计电路与编程？

## 常见问题
---
    
## 更多信息，欢迎访问：
---
[micro:bit知识库地址](https://www.elecfreaks.com/learn-cn/)    
micro:bit官方推荐供应商：[恩孚科技淘宝店](https://shop69086944.taobao.com/?spm=a230r.7195193.1997079397.2.RSthR0)  
QQ技术交流群：570756726   



