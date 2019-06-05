# 软件编程案例08：舵机

## 简介 ##
---
- 舵机是一种位置（角度）伺服的驱动器，适用于那些需要角度不断变化并可以保持的控制系统。在这次的实验中，我们将用micro:bit控制舵机在行程范围内循环转动。

## 硬件连线图 ##
---
![](./images/QpsN3Rk.png)

- 使用香蕉线按如上图连接电路，电池盒内放入2颗7号AAA电池。

## 电路原理图 ##
---
![](./images/yXHJ6zm.png)

- micro:bit插槽的GND端和电池GND相连内部，形成电流回路。

## 主要元件介绍 ##
---
### 舵机 ###
- 舵机由直流电机、减速齿轮组、电位器和控制电路组成的一套自动控制系统。通过发送脉冲信号，指定输出轴旋转角度。舵机一般而言都有最大旋转角度（比如180度）。
- 一般而言，舵机的基准信号都是周期为20ms，宽度为1.5ms。这个基准信号定义的位置为中间位置。舵机有最大转动角度，中间位置的定义就是从这个位置到最大角度与最小角度的量完全一样。最重要的一点是，不同舵机的最大转动角度可能不相同，但是其中间位置的脉冲宽度是一定的，那就是1.5ms。
- 在实验箱板载了一颗180°舵机。
![](./images/uqmkhZ6.png)

注意：micro:bit官方已经将舵机的控制代码封装成积木块，用Makecode编程时，无需考虑脉冲宽度之类的复杂信息。

*- 连线时注意正负极。*

## 软件编程设计
---
### 步骤 1

- 点击打开[微软makecode在线积木块编程https://makecode.microbit.org/#](https://makecode.microbit.org/#)。

- 点击New Project按钮，新建一个项目。

![](./images/t34k5Zb.png)

### 步骤 2

- 在forever积木块中插入，将伺服电机P1口设置为0°。
- 暂停2秒。

![](./images/rMTDGWP.png)

- 再在其后插入将伺服电机P1口设置为180°。
- 暂停2秒。

![](./images/rKePFnv.png)

### 程序

- 请参考程序连接：[https://makecode.microbit.org/_fudJaMCRhE1r](https://makecode.microbit.org/_fudJaMCRhE1r)

- 你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_fudJaMCRhE1r" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---


## 结论
---
- 舵机在0至180度之间来回旋转。

## 思考
---
- 如果我们想用温度传感器和舵机做一个指针温度计，那么我们该如何设计电路与编程？

## 常见问题
---


## 相关阅读  
---

