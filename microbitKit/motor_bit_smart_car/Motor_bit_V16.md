# 两路电机驱动板（motor:bit）

## 简介
---
Motor:bit是一款基于Micro:bit的电机驱动板，它集成了TB6612电机驱动芯片，可用于驱动两路单通道最大电流为1.2A的直流电机，还集成了12路GVS-OCTOPUS系列电子积木接口、1路IIC通信接口，可用于扩展各种各样的传感器或者电子模块，其中P3-P7、P9-P10为Micro:bit直接驱动的3.3V电平IO接口；P13-P16、P19-P20(IIC接口)接口为支持3.3V/5V电平切换IO接口，通过切换板载的拨动开关可以驱动3.3V或者5V设备；另外，Motor:bit还集成了一个蜂鸣器，可用于播放简单的音乐，Motor:bit是一个极具DIY性质的Micro:bit的电机驱动板，你可用它来DIY一款属于你自己的智能小车，12路的扩展IO接口、IIC接口可以方便给你的设计搭载更多有趣的东西。

![](./images/6zRKrvw.jpg)

## 特性
---
- 支持2路直流电机
- 单通道最大1.2A驱动电流。
- 扩展14路IO口，以GVS接口形式引出，其中6路支持3V/5V电平切换。
- 板载1个无源蜂鸣器。

## 参数
---
项目|参数
:-:|:-:
品名|两路电机驱动板（motor:bit）
SKU|EF03406
版本号|V1.6
直流电源供电电压|DC6-12V
直流电机驱动|2路
每通道电机接口最大输出电流|1.2A
可扩展数字IO接口|12
可扩展模拟IO接口|3
IIC接口|支持
无源蜂鸣器|支持
尺寸|60.00mm X 47.50mm
净重|20g

## 外形与安装定位尺寸
---
![](./images/zXGYS2h.jpg)

## 引脚接口框图
---
![](./images/yiJJzHK.jpg)

## 主体功能模块介绍
---
### M1-M2电机接口

![](./images/29nn8kR.jpg)

M1-M2电机接口，M1、M2可以分别接入一路最大电流为1.2A的直流电机。

### 无源蜂鸣器

![](./images/eFXaJlg.jpg)

micro:bit主板的P0接口接入控制无源蜂鸣器，可以播放简单的声乐。

### 电源切换开关

![](./images/mq8NFg4.jpg)

电源开关，拨至ON-电源打开，拨至OFF-电源关断。

### 电源供电接口

![](./images/NDzflbB.jpg)

电源供电接口，可接入6-12V直流电源。

### VCC电平切换开关

![](./images/vpxh1nD.jpg)

VCC电平切换开关，开关拨至5V则VCC提供5V电源，开关拨至3V3则VCC提供3.3V电源，电平切换开关对P13、P14、P15、P16、P19、P20这6个IO口有效。

### G-VCC-S标准GVS电子积木接口

![](./images/4cqVab2.jpg)

G-VCC-S标准GVS电子积木接口，4路（P13-P16）GPIO和1路IIC通信接口（P19-P20），可以根据VCC的电平变化，接入3.3V/5V电平的设备。

### G-3V3-S标准GVS电子积木接口

![](./images/xjDkR8E.jpg)

G-3V3-S标准GVS电子积木接口，可以直接接入8路工作在3.3V电源的设备，其中P3、P4、P10可用于模拟信号输入接口。

### micro:bit主板金手指接口

![](./images/CemM8y5.jpg)

用于插入micro:bit主板。

## 快速上手
---
### 硬件连接  
将两路TT马达如图所示连接至motor:bit

![](./images/5ayGCgd.png)

### 软件编程  
打开[makecode](https://makecode.microbit.org/)，搜索关键词`motorbit`添加motorbit package。

![](./images/CDV9ODY.png)

编写程序让两个TT马达交替旋转。

![](./images/2klOChu.png)

完整程序链接：[https://makecode.microbit.org/_LsPT31WPH1JD](https://makecode.microbit.org/_LsPT31WPH1JD)

你也能在下列网页直接下载程序：
<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_LsPT31WPH1JD" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>


## 常见问题
---
**问：为什么电机转起来的时候，蜂鸣器响声异常？**  
答：micro:bit只能同时输出一个频率的PWM信号，电机的PWM信号频率与蜂鸣器的频率不一致，所以电机与蜂鸣器无法同时正常工作。这个是micro:bit主板特性决定的，不是电机驱动板的问题。

