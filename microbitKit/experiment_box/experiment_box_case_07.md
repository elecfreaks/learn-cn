# 软件编程案例07：蜂鸣器

## 简介 ##
---
- 蜂鸣器是一种一体化结构的电子讯响器，广泛应用于计算机、打印机、复印机、报警器、电子玩具、汽车电子设备、电话机、定时器等电子产品中作发声器件。本次实验，我们用micro:bit驱动蜂鸣器，让它发出不同的声音的高频与低频间来回循环，就像警报声一样。

## 硬件连线图 ##
---
![](./images/4EceRG6.png)

- 使用香蕉线按如上图连接电路，电池盒内放入2颗7号AAA电池。

## 电路原理图 ##
---
![](./images/kl4b2QE.png)

- micro:bit插槽的GND端和电池GND相连内部，形成电流回路。
- micro:bit的P0口输出一个方波，经过三极管放大后驱动蜂鸣器。

## 主要元件介绍 ##
---
### 蜂鸣器 ###
- 蜂鸣器是一种发声器件，它由振动装置和谐振装置组成。按照控制方式分类，可把蜂鸣器又分为有源型与无源型。
- 有源型蜂鸣器的工作发声原理是：蜂鸣器内部集成振荡系统与放大取样电路，当有直流电源通过蜂鸣器时会使谐振装置产生声音信号，有源型蜂鸣器的工作发声原理图如下：

![](./images/spNnKiB.jpg)

- 无源型蜂鸣器的工作发声原理是：方波信号输入谐振装置转换为声音信号输出，无源型蜂鸣器的工作发声原理图如下：

![](./images/kNHyjjl.jpg)

- 在实验箱板载了一颗无源蜂鸣器。

![](./images/xyNlKjk.jpg)

### Mos管 ###

- 三极管是一种控制电流的半导体器件，其作用是把微弱信号放大成幅度值较大的电信号。如果直接把micro:bit产生的PWM信号输入至蜂鸣器，蜂鸣器只会发出微弱的声音，这是因为IO口的驱动电流通常都是非常微弱的，不足以直接驱动蜂鸣器这类器件。这时候，我们就需要用到三极管将PWM信号的电流放大，从而让蜂鸣器能发出正常的声响。 
- 实验箱板载了一颗mos管。

![](./images/NnmYwRp.jpg)

*- 连线时注意正负极。*

## 软件编程设计
---
### 步骤 1

- 点击打开[微软makecode在线积木块编程https://makecode.microbit.org/#](https://makecode.microbit.org/#)。

- 点击New Project按钮，新建一个项目。

![](./images/t34k5Zb.png)

### 步骤 2

![](./images/vyb4j8a.png)

- 按顺序依次插入播放音调和延迟积木块，播放CEGE音调。

### 程序

- 请参考程序连接：[https://makecode.microbit.org/_VdrFjUVzHgA1](https://makecode.microbit.org/_VdrFjUVzHgA1)

- 你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_VdrFjUVzHgA1" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---


## 结论
---
- 发出不同的声音的高频与低频间来回循环，就像警报声一样。

## 思考
---
- 

## 常见问题
---


## 相关阅读  
---

