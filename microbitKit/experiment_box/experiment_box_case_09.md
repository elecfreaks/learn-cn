# 软件编程案例09：自锁按钮

## 简介 ##
---
- 自锁开关，是一种常见的按钮开关。当我们初次按下开关按钮时，开关电路连接并保持这种状态，即自锁。再次按下开关按钮时，开关断开，同时开关按钮弹出来。在这次实验中，我们将使用自锁开关来控制LED的点亮与熄灭。

## 硬件连线图 ##
---
![](./images/2hsQnmL.png)

- 使用香蕉线按如上图连接电路，电池盒内放入2颗7号AAA电池。

## 电路原理图 ##
---
![](./images/VT0SVKN.png)

- micro:bit插槽的GND端和电池GND相连内部，形成电流回路。

## 主要元件介绍 ##
---
### 自锁开关 ###
- 自锁开关一般是指开关自带机械锁定功能，按下去，松手后按钮是不会完全跳起来的，处于锁定状态，需要再按一次，才解锁完全跳起来。它就叫自锁开关。早期的直接完全断电的电视机、显示器就是使用的这种类型的开关。
- 在实验箱板载了一颗带红色键帽的自锁按钮。

![](./images/3iIZPHP.png)

*- 连线时注意正负极。*

## 软件编程设计
---
### 步骤 1

- 点击打开[微软makecode在线积木块编程https://makecode.microbit.org/#](https://makecode.microbit.org/#)。

- 点击New Project按钮，新建一个项目。

![](./images/t34k5Zb.png)

### 步骤 2

- 在on start积木块中插入设置引脚P0以触发边缘事件，之后插入拉引脚P0为上，默认高电平并且可以检测电平变化的边沿。

![](./images/aIzHYGY.png)

- 每次按下按钮的时候，P0口的电压就会改变一次.0V到3.3V的时候，我们称之为“上升沿”(RISE)。当3.3V切换到0V时，我们称之为“下降沿”(FALL)。

![](./images/kcnveNe.jpg)

### 步骤 3

- 设置一个事件，监测P0电压的上升和下降。当上升沿来临时，向P2口数字写入1，以点亮LED灯。

![](./images/c6aX7T8.png)

### 步骤 4

- 当下降沿来临时，向P2口数字写入0，以熄灭LED灯。

![](./images/c6aX7T8.png)

### 程序

- 请参考程序连接：[https://makecode.microbit.org/_33tJqiCC8DL0](https://makecode.microbit.org/_33tJqiCC8DL0)

- 你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_33tJqiCC8DL0" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---


## 结论
---
- 按下自锁开关，LED点亮；再按一次，LED熄灭。

## 思考
---
- 如何用自锁开关来控制micro:bit点阵显示屏，如何编写代码。

## 常见问题
---


## 相关阅读  
---

