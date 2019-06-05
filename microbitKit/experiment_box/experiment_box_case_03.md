# 软件编程案例03：RGB LED灯

## 简介 ##
---
三色LED是LED灯的一种。它能够发出红、绿、蓝三种不同颜色的光线。在本次实验中，我们将让RGB LED在红、绿、蓝三种颜色之间切换。

## 硬件连线图 ##
---
![](./images/Gca57tq.png)

- 使用香蕉线按如上图连接电路，电池盒内放入2颗7号AAA电池。

## 电路原理图 ##
---
![](./images/wnBLHqP.png)

micro:bit插槽的GND端和电池GND相连内部，形成电流回路。

## 主要元件介绍 ##
---
### RGB LED ###
- RGB LED是LED的一种，把红色LED、绿色LED、蓝色LED集合成一个元件，分为R通道，Ｇ通道和B通道，也就是RGB。我们都知道，光的三原色分别为红色、绿色、蓝色，利用这三种颜色进行组合，能够合成出万物所有的颜色。同样，利用RGB LED进行不同亮度的组合，能够形成无数种颜色。
- RGB LED分为两种类型，分别为共阴极与共阳极：共阴极的RGB LED公共端接GND；共阳极的RGB LED公共端接VCC。
- 实验箱板载一颗共阴极的RGB LED。

![](./images/KF4IVxu.jpg)

- *连线时注意正负极。*

## 软件编程设计
---
### 步骤 1

- 点击打开[微软makecode在线积木块编程https://makecode.microbit.org/#](https://makecode.microbit.org/#)。

- 点击New Project按钮，新建一个项目。

![](./images/t34k5Zb.png)

### 步骤 2

- 在当on button A pressed积木块中依次插入，P0口数字写入1，P1口数字写入0，P2口数字写入0积木块。
- 向RGB的R通道写入1，G和B通道写入0。
- RGB LED亮红灯。

![](./images/sB2lvoi.png)

- 同理写绿灯和蓝灯的代码。

![](./images/Rl1jlrI.png)

![](./images/JsaMcnR.png)


### 程序

- 请参考程序连接：[https://makecode.microbit.org/_bm1g8RaVuPkb](https://makecode.microbit.org/_bm1g8RaVuPkb)

- 你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_bm1g8RaVuPkb" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---


## 结论
---
- 按下A按钮，亮红灯，按下B按钮，亮绿灯，按下C按钮，亮蓝灯。


## 思考
---
- 红色加蓝色是什么颜色，表现出来。

## 常见问题
---


## 相关阅读  
---

