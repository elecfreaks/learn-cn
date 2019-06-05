# 课程_10 电机

![](./images/8KZyoCy.jpg)

## 简介
---
电机是依据电磁感应定律实现电能转换为动能的一种装置。在这次的实验中，我们将用一个开关来控制电机的启动与停止。

## 元件清单
---
### 硬件：
- 1 x micro:bit
- 1 x USB线
- 1 x micro:bit面包板扩展板
- 1 x 面包板83 x 55 mm
- 1 x 5V 迷你电机
- 1 x TIP 120 NPN 三极管
- 1 x 1N4007 二极管
- 1 x 100 欧姆电阻
- 2 x 鳄鱼夹线
- 若干跳线
**温馨提示：如果你需要以上所有元件，你可以购买我们的[Elecfreaks小小科学家套件](https://item.taobao.com/item.htm?spm=a1z10.1-c-s.w4024-17803785896.2.18dc3f94XOgpWg&id=562837851877&scene=taobao_shop)。**

![](./images/W4tseua.jpg)

## 主要元件介绍
---
### 电机

电机是依据电磁感应定律实现电能转换为动能的一种装置。电机的分类非常多，在本案例里，我们用到的是直流电机。当在电机两端加上直流电压时，电机会旋转，电压越高，旋转的速度越快。

![](./images/JesPIk4.jpg)

### 二极管

二极管是一种具有两个电极的原件，一端为阳极，一端为阴极，它只允许电流从阳极向阴极方向移动，可以把它想象成电子版的止逆阀。
对于普通的二极管，可以通过管体表面颜色来区分正负极，有白线的一端为负极。

![](./images/b1g3bBJ.jpg)

### 鳄鱼夹线

鳄鱼夹线与跳线的作用一样。有些器件不方便用跳线连接，可以考虑用鳄鱼夹来连线。

![](./images/EfkdKmY.jpg)

本次实验，我们就是用鳄鱼夹线来连接我们的电机。

![](./images/Oj1aUaf.jpg)


## 实验步骤
---
### 硬件连接
根据下面的图片将你的元件连接起来：


![](./images/2MZA7bj.jpg)

micro:bit的IO口的驱动电流非常微弱的，不足以直接驱动电机。这时候，我们就需要用到三极管将IO信号的电流放大，用三极管放大IO口信号电流的电路图与上一课驱动蜂鸣器的电路图非常类似，唯一的区别是在电机两端加上了一个二极管。该二极管在此电路中叫做续流二极管。

电机里面有线圈，线圈在通过电流时，会在其两端产生感应电动势。当电流消失时，其感应电动势会对电路中的元件产生反向电压，有可能会损坏器件，续流二极管在电路中反向并联在线圈的两端，当电感线圈断电时其两端的电动势并不立即消失，此时残余电动势通过二极管释放。这是一种经典保护设计。

三极管将IO信号的电流放大的局部电路图如下： 

![](./images/e4YL3hx.jpg)

连接完成后如图:

![](./images/RwH4uNp.jpg) 

### 软件

[微软Makecode在线编辑器:makecode.microbit.org](https://makecode.microbit.org/)

![](./images/JHZUvh2.png)

### 如图所示编写程序

![](./images/imGjxBm.png)

### 代码详解
- 1.将P0口写入数字信号1，将P1端口上拉至高电平，这样才能正常识别按钮信号

![](./images/Qqjk2WB.png)

- 2.当按钮被按下，设置P0为1，放开时，设置为数字信号量0

![](./images/lFdOZxr.png)

### 参考程序
请参考程序连接：[https://makecode.microbit.org/_CAUDezEJrVtc](https://makecode.microbit.org/_CAUDezEJrVtc)

你也可以通过以下网页直接下载程序，下载完成后即可开始运行程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_CAUDezEJrVtc" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

## 实验结果
---
按下按钮时，电机开始旋转，再按一次，电机停止旋转。
注意：micro:bit的电源电压比较低，只有3V，按下按钮时，电机有可能不能启动，遇到这种情况，请用手拨动一下电机的扇叶，电机方能正常旋转。

![](./images/UeWUgLi.gif)


## 思考
---
如果要用电位器对电机进行速度控制，该如何设计电路与编程？

## 常见问题
---

## 更多信息，欢迎访问：
---
[micro:bit知识库地址](https://www.elecfreaks.com/learn-cn/)    
micro:bit官方推荐供应商：[恩孚科技淘宝店](https://shop69086944.taobao.com/?spm=a230r.7195193.1997079397.2.RSthR0)  
QQ技术交流群：570756726   



