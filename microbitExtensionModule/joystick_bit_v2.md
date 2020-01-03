# Joystick:bit V2

## 简介
---
Joystick:bit V2是一款基于micro:bit 的游戏手柄。它包含可控制4个方向的手柄和4个未定义的按钮。同时也搭配了蜂鸣器和振动马达，增强了游戏体验。它外观小巧，手感舒适，可远程遥控。

![](./images/joystick_v2_01.jpg)

## 包装清单
---

1 x [Joystick:bit v2](http://www.elecfreaks.com/estore/elecfreaks-joystick-bit-for-micro-bit.html)


## 特点
---
- 编程语言：Javascript / Makecode / Microsoft Touch Develop / Python.

- 板载蜂鸣器。

- 震动反馈带来极致游戏体验。

- 可使用makecode扩展包，简单易用。

- 拔出micro:bit 后自动断电。

- 可为micro:bit 到处7个IO接口。

## 外形与尺寸定位

---

![](./images/joystick_v2_02.png)


## 功能性模块介绍
---

### 手柄

![](./images/joystick_v2_03.png)

 X & Y分别连接至micro:bit 主板的P1,P2接口。

### 蜂鸣器

![](./images/joystick_v2_04.png)

无源蜂鸣器连接至micro:bit 的P0 接口。

### 振动马达

![](./images/joystick_v2_05.png)

振动马达连接至P16接口。

### 按钮

![](./images/joystick_v2_06.png)

 C、D、E、F 按钮相应的连接至micro:bit 的P12、P13、P14、P15 接口。

### 7个GVS 接口

![](./images/joystick_v2_07.png)

它包含7个GVS扩展端口，可以焊接引脚来扩展更多的功能。

## 开始搭建
---
### 安装

装入2节 3A 电池并插入micro:bit 主板。

添加“joystick:bit” 扩展包。

进入makecode并且创建一个新项目，点击扩展。 

![](./images/joystick_v2_08.png)

搜索“ joystickbit” 并添加对应的扩展包。

![](./images/joystick_v2_09.png)
![](./images/joystick_v2_10.png)

## 编程
---

开始编程，一旦按下你的游戏手柄上的按钮，它就会产生振动反馈和显示按钮标志。

![](./images/joystick_v2_11.png)

程序链接: [https://makecode.microbit.org/_AD3P71UrTCA1](https://makecode.microbit.org/_AD3P71UrTCA1)

或通过以下界面直接下载:
<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_AD3P71UrTCA1" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>


当下载完成后，打开电源开关，系统提示音响起。

按下C，D,  E 或F按钮，手柄都会振动一次。

## 更多信息
---

若想获取更多信息，请查看：http://www.elecfreaks.com
