# 软件编程案例02：按钮

## 简介 ##
---
在上一个实验中，我们已经学习了如何让micro:bit控制LED灯永久闪烁。

这次我们将使用一个按钮来控制LED灯的闪烁。当我们按下按钮，LED灯会闪烁；松开按钮，LED灯就会停止闪烁。

## 硬件连线图 ##
---
![](./images/fLSfez6.png)

- 使用香蕉线按如上图连接电路，电池盒内放入2颗7号AAA电池。

## 电路原理图 ##
---
![](./images/NSpS8c0.png)

- micro:bit插槽的GND端和电池GND相连内部，形成电流回路。
- 当按钮按下时电路接通，micro:bit的P2端口连接到GND，P2口电平被拉低。

## 主要元件介绍 ##
---
### 按钮开关 ###
- 这是一个用来控制电子设备的普通元件。它大部分用于连接或者切断控制电路，从而实现电机或者其他电子设备的控制。 
- 瞬时按钮开关通常是保持开启的。当它被按下的时候，电路接通；当它弹起的时候，电路会切换回断路的状态。
- 在实验箱板子上我们配备了1个带有蓝色键帽的按钮开关。

![](./images/HgatY6t.png)

## 软件编程设计
---
### 步骤 1

- 点击打开[微软makecode在线积木块编程https://makecode.microbit.org/#](https://makecode.microbit.org/#)。

- 点击New Project按钮，新建一个项目。

![](./images/t34k5Zb.png)

### 步骤 2

- 首先在on start积木块中插入，将P2端口拉高，使其默认值为1，也就是默认高电平。

![](./images/VuZAOrz.png)

### 步骤 3 

- 数字读取P2口的值，并且判断其是否等于0。（当按钮按下时电路接通，P2口接GND变为低电平，数字读取时值为0。）

![](./images/0EHwnci.png)

### 步骤 4

- 如果P2口数值为0，则向P2口写入0，延时500ms，再写入1，延时500ms。LED灯闪烁。

![](./images/z9Yqpi3.png)

### 程序

- 请参考程序连接：[https://makecode.microbit.org/_5UriK0fC7LWr](https://makecode.microbit.org/_5UriK0fC7LWr)

- 你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_5UriK0fC7LWr" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---


## 结论
---
- 按下按钮开关，LED灯开始闪烁。
- 松开按钮开关，LED灯常亮。


## 思考
---
- 为什么要加500ms延迟。


## 常见问题
---


## 相关阅读  
---

