# 软件编程案例01：LED灯

## 简介 ##
---
LED灯的应用非常广泛。在日常生活中，我们看到的大部分信号灯都采用了LED灯座位主要光源。在本案例中，我们使用micro:bit控制1颗LED灯闪烁。

## 硬件连线图 ##
---
![](./images/jGkCj0K.png)、

- 使用香蕉线按如上图连接电路，电池盒内放入2颗7号AAA电池。

## 电路原理图 ##
---
![](./images/5DImBjP.png)

- micro:bit插槽的GND端和电池GND相连内部，形成电流回路。
- 当P0端口数字写入1，也就是高电平，电路接通，LED灯亮起。
- 当P0端口数字写入0，也就是低电平，电路断开，LED灯熄灭。

## 主要元件介绍 ##
---
### LED ###
- LED是Light Emitting Diode（发光二极管）的缩写。这是一种半导体二极管。它可以将电能转换成光能。当电流经过的时候，它就会发光。
- 在实验箱板子上我们配备了1颗红色的LED。左边黑色端口为负极，右边红色端口为正极。

![](./images/ks4hn2r.png)

*- 连线时注意正负极。*

### 电阻 ###
- 电阻是一种用于控制电流的元件。它可以限制所连接的电路的电流。电阻不分正负极
- 在实验箱中配备了3颗100 Ω电阻和1颗10KΩ电阻。

![](./images/fv1fyJm.png)

- 在LED灯的电路中串联一个100Ω电阻以限流，如果不限制电流的话，可能会造成LED的损坏。

## 软件编程设计
---
### 步骤 1

- 点击打开[微软makecode在线积木块编程https://makecode.microbit.org/#](https://makecode.microbit.org/#)。

- 点击New Project按钮，新建一个项目。

![](./images/t34k5Zb.png)

### 步骤 2

- 首先在forever积木块中插入，向P0口数字写入1 积木块，以点亮LED灯，然后暂停500ms；

![](./images/VOh783L.png)

- 再在后边插入，向P0口数字写入0 积木块，以关闭LED灯，然后暂停500ms；

![](./images/D08SzOj.png)

### 程序

- 请参考程序连接：[https://makecode.microbit.org/_Fa1Jpj38Di1Y](https://makecode.microbit.org/_Fa1Jpj38Di1Y)

- 你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_Fa1Jpj38Di1Y" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---


## 结论
---
- 打开开关，LED灯开始闪烁。

![](./images/KN0xKqX.gif)

## 思考
---
- 为什么要加500ms延迟。

## 常见问题
---


## 相关阅读  
---

