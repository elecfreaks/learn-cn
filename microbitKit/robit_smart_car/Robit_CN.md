# mBot扩展板(Robit)

## 简介
---

Robit是一款基于micro:bit的智能小车主板，它能完全兼容mBot的车架与传感器，除了继承了mBot上简单方便的RJ25接线端口、电机接口和传感器之外，我们还扩展4路直流电机接口、2路步进电机接口（步进电机接口与直流电机接口复用），8路PWM信号输出接口，可以驱动舵机等PWM信号驱动的设备，板载10路G-5V-S数字信号OCTOPUS电子积木接口，4路G-5V-S模拟信号OCTOPUS电子积木接口。Robit除了可以实现所有mBot的基本功能，还能扩展更多的传感器、电机、舵机、步进电机等。

![](./images/ybkfOnk.jpg)


## 特性
---

- 完全兼容mBot的车架与传感器。
- 支持4路直流电机驱动，2路步进电机驱动。
- 8路PWM信号输出接口。
- 扩展出10路G-5V-S数字信号OCTOPUS电子积木接口。
- 扩展出4路G-5V-S模拟信号OCTOPUS电子积木接口。
- 集成蜂鸣器、光敏传感器、彩虹LED、红外发射、红外接收等常用功能。

## 参数
---
项目 | 参数 
:-: | :-: 
直流电源供电输入电压|DC 3.7-6V
锂电池供电输入电压|DC 3.7-4.2V
USB充电电流|500mA
可扩展模拟IO口数量|4
可扩展的数字IO口数量|10
舵机接口数量|8
直流电机驱动|4路
步进电机驱动|2路
可编程LED灯珠数|2颗
无源蜂鸣器|支持
光敏传感器|支持
红外接收|支持
红外发射|支持
尺寸|90mm X 74mm
净重|46g


### 外形与安装定位尺寸

![](./images/DHJWwCU.png)

## 引脚接口框图
---

![](./images/4ZNLceA.png)

## 主要功能模块介绍
---

### RJ25接口

![](./images/AiRvd9b.png)

robit有4组RJ25接口，每个RJ25接口包含6个出点，分别对应了电源、两个IO口与IIC接口，兼容mBot部分传感器。  
J1的6个触点分别对应micro:bit的SCL(P19)、SDA(P20)、GND、5V、P13、P14。  
J2的6个触点分别对应micro:bit的SCL(P19)、SDA(P20)、GND、5V、P15、P16。  
J3的6个触点分别对应micro:bit的SCL(P19)、SDA(P20)、GND、5V、P1、P2，支持5V的模拟输入传感器。  
J4的6个触点分别对应micro:bit的SCL(P19)、SDA(P20)、GND、5V、P3、P4，支持5V的模拟输入传感器。  

### GVS标准电子积木接口

![](./images/EX5gFN0.png)

micro:bit的IO口除了引出至RJ25接口外，还以GVS的形式引出，支持5V的器件，其中P1、P2、P3、P4支持5V的模拟输入传感器。

### GVS标准舵机接口

![](./images/q60J0FD.png)

S0~S7，最多可同时接入8路舵机。该接口从PCA9685芯片引出，通过micro:bit的IIC接口扩展而来，不占用普通I/O口。

### 直流电机接口

![](./images/foGr3ds.png)

M1~M4，最多可同时接入4路直流电机。电机通过PCA9685芯片进行PWM控制，该芯片使用micro:bit的IIC接口，不占用普通I/O口。

### 步进电机接口

![](./images/SgFEXhW.png)

STEP1与STEP2，最多可同时接入两路28BYJ-48-5V步进电机。

### 蜂鸣器

![](./images/OJuywhz.png)

板载蜂鸣器，连接在micro:bit的P0口。

### 光线传感器
  
![](./images/GxtT0KK.png)  

板载光线传感器，连接在micro:bit的P10口。  

### 红外发射管  

![](./images/iMOf8lZ.png)  

板载红外发射管，连接在micro:bit的P6口。  

### 红外接收管

![](./images/uw7fE9k.png)  

板载红外接收管，连接在micro:bit的P8口。 

### 彩虹LED

![](./images/aANe5pE.png)

板载两颗彩虹LED，连接在micro:bit的P12。

### DC电源接口  

![](./images/5hUXn0Y.png)  

DC电源接口，可支持3.7V~4.2V直流电源，通常接入4节AAA电池盒。  

### 锂电池接口  

![](./images/CX1F1jI.png)  

锂电池接口，可支持3.7V~4.2V锂电池。  

### 锂电池电量指示灯  

![](./images/86v4GeD.png)  

锂电池电量指示灯，为闪烁状态，满电为4格电，闪烁一次表示1格电，满电为连续闪烁4次。  

### USB充电接口  

![](./images/9xSHrjg.png)  

该USB接口仅用于为锂电池充电，不支持数据传输，充电电流为500mA。  

## 快速上手  
---
### 硬件连接  
将robit固定在mbot小车上；  
将左轮电机接入M1口，将右轮电机接入M2口；  
连接好后如图所示：  
![](./images/sVvkB7S.jpg)  

### 软件编程  
打开[makecode](https://makecode.microbit.org/)，搜索关键词`robit`添加robit package。

![](./images/C0LxMkP.png)

编写程序，让robit小车先前进3秒，再后退3秒，往返运行，详细代码如下：

![](./images/8WwA6Bp.png)

程序代码链接：[https://makecode.microbit.org/_aXVAyx3dm585](https://makecode.microbit.org/_aXVAyx3dm585)

你也能通过下列窗口直接下载代码：

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_aXVAyx3dm585" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>

### 结果
robit小车先前进3秒，再后退3秒，往返运行。

## 常见问题
---
