# 软件编程案例06：温度传感器

## 简介 ##
---
- 温度传感器是指能感受温度并转换成可用输出信号的传感器。温度传感器是温度测量仪表的核心部分，品种繁多。
- 在这次的实验中，我们将学习模拟温度传感器，并将它的数值读出显示在micro:bit的显示屏上。

## 硬件连线图 ##
---
![](./images/Tk7Ddy9.png)

- 使用香蕉线按如上图连接电路，电池盒内放入2颗7号AAA电池。

## 电路原理图 ##
---
![](./images/8pV3WaA.png)

- micro:bit插槽的GND端和电池GND相连内部，形成电流回路。

## 主要元件介绍 ##
---
### 热敏电阻 ###
- 热敏电阻器是敏感元件的一类，按照温度系数不同分为正温度系数热敏电阻器（PTC）和负温度系数热敏电阻器（NTC）。热敏电阻器的典型特点是对温度敏感，不同的温度下表现出不同的电阻值。正温度系数热敏电阻器（PTC）在温度越高时电阻值越大，负温度系数热敏电阻器（NTC）在温度越高时电阻值越低，它们同属于半导体器件。
- 在实验箱板子上我们配备了1颗负温度系数热敏电阻器（NTC）。

![](./images/M3k99Lj.png)

*- 连线时注意正负极。*

## 软件编程设计
---
### 步骤 1

- 点击打开[微软makecode在线积木块编程https://makecode.microbit.org/#](https://makecode.microbit.org/#)。

- 点击New Project按钮，新建一个项目。

![](./images/t34k5Zb.png)

### 步骤 2

- 换算公式：

![](./images/sTfPnYc.png)

- micro:bit读取的为IO口的模拟读数，需要经过以上公式换算为温度值。


### 步骤 3

- 设置一个Temperature变量来存放换算过来温度值。
- 按照上述公式将P0口读取的模拟值换算为温度值。

![](./images/N91GU48.png)

- 显示温度值，间隔一秒钟。

![](./images/poCULlT.png)

### 程序

- 请参考程序连接：[https://makecode.microbit.org/_h8hUjXYFM0yH](https://makecode.microbit.org/_h8hUjXYFM0yH)

- 你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_h8hUjXYFM0yH" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---


## 结论
---
- 在micro:bit的点阵显示屏上实时显示当前温度。



## 思考
---
- 

## 常见问题
---


## 相关阅读  
---

