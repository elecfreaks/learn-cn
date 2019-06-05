# 5V传感器扩展板（octopus:bit）

## 简介  
---

ELECFREAKS Octopus:bit是一款micro:bit的扩展板。它扩展出了micro:bit的GPIO口、串口、IIC接口、SPI接口。它最大的特点是可对部分GPIO口的工作电压进行电平转换，使micro:bit能适配5V的传感器。

![](./images/wcgxnG0.png)


## 包装清单  
---

1 x ELECFREAKS Octopus:bit  


## 硬件  
---

### 特点  

- 输入电压3.3V（通过micro:bit边缘连接器供电）  
- 扩展了从P0至P16的PGIO口。  
- 每个I/O口下方都有VCC与GND的排针，并且用不同的颜色区分开来，用你可以很方便的连接你的扩展模块，该针脚的排布与章鱼系列完全兼容。  
- 具备升压模块，P8、P9、P11~P16的工作电平可通过电平转换开关在3.3V与5V之间切换。  
- 引出了串口、I2C接口与SPI接口，其中，I2C接口可以接3路I2C设备，SPI接口可以接两路SPI设备。  
- 两块扩展板之间可直接对接进行串口通信。  


## 应用  
---

适用于所有需要使用micro:bit GPIO的场景，如编程教育、制作智能设备等。  


## 引脚接口框图  
---

![](./images/wCWdoag.jpg)


## 部分引脚接口详细介绍
---

### 标准GVS接口

![](./images/gk3dN4E.png)

标准GVS接口，其中黄色部分（P0~P7， P10）工作电压为3.3V，蓝色部分（P8, P9, P11~P16）工作电压可通过电平转换开关在3.3V与5V之间切换。
每个I/O口下方都有VCC与GND的排针，并且用不同的颜色区分开来，用你可以很方便的连接你的扩展模块，该针脚的排布与章鱼系列完全兼容。

### 电平转换开关

![](./images/JoxT6k2.png)

该开关可对蓝色部分IO口（P8, P9, P11~P16）的工作电平进行3.3V/5V切换。

该开关的作用范围如下图所示： 
![](./images/GHPffMl.png)

### 串口

![](./images/8aVYsja.png)

串口的工作电压可通过电平转换开关进行3.3V/5V切换。
TX连接在P8，RX连接在P12，左边排针的部分为输入输出双向串口，右边排母为单向输出串口
**注意** 要使用该串口，请先按照如下程序初始化串口：

![](./images/1gnuYd5.png)

## 外形与安装定位尺寸
---

![](./images/ZYrWREG.jpg)


## 软件
---

## 示例1 播放音乐
---

### 硬件连接

将无源蜂鸣器模块连接至PO口。

![](./images/Zc6ChwR.jpg)

### 示例代码  

![](./images/0MBprkk.png)

代码连接：[https://makecode.microbit.org/_fAmC3WERHdR2](https://makecode.microbit.org/_fAmC3WERHdR2)  

下载完程序后，蜂鸣器将循环播放生日快乐歌。




