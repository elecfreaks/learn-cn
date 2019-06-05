# 3线宽压超声波电子积木

## 简介
---
Sonar:bit是一个3线宽压超声波模块，它可以工作电压为3.0V-5V，3.3v或5V的单片机系统均能使用；它只需要3根线（G、V、S）就可以工作，比常规的4线超声波模块节省一个IO口。Sonar:bit量程为4cm~400cm，测量数据稳定准确，误差仅为±1cm。可应用于短距离测量、智能小车、机器人、Micro:bit、Arduino配套教学等场合。

![](./images/pdBREKf.jpg)

## 特性
---
- 输入电压为3V~5V，micro:bit与arduino均能直接驱动。
- 标准的3线GVS接口，仅占用一个IO口。


## 参数
---

![](./images/vm9SX0e.png)


## 外形与安装定位尺寸
---
![](./images/h4HcvxO.jpg)

## 引脚接口框图
---
![](./images/7E5ECzN.jpg)

## 主体功能模块介绍
---
### 超声波发射探头

![](./images/T1xDsne.jpg)

超声波发射探头用于发射超声波信号。

### 超声波接收探头

![](./images/JxNrz8Q.jpg)

超声波接收探头用于接收超声波信号。

### 主控芯片MCU

![](./images/2CjnvfP.jpg)

超声波模块核心控制芯片。

### 发射信号驱动芯片

![](./images/iOW0IN3.jpg)

发射信号驱动芯片用于提供驱动超声波发射探头的发射超声波信号。

### 接收信号处理芯片

![](./images/VxEZ5KQ.jpg)

接收信号处理芯片用于对超声波回波信号进行接收与处理，并将处理好的信号反馈给主控芯片。

### G-V-S信号控制接口

![](./images/N9yc6Jm.jpg)

G-V-S信号控制接口，用于外部设备控制超声波模块的工作。

## 快速上手
---
### 硬件连接  

将Sonar:bit连接到sensor:bit的P2端口，Micro:bit连接到电脑。 
连接好后如图所示：

![](./images/fvYx5lR.jpg)

![](./images/wCftg3Y.jpg)

### 软件编程  
打开[makecode](https://makecode.microbit.org/)在线编辑器。

编写程序，让从P2口返回的数据赋值给distance变量，将变量数字输出到点阵显示屏上：

![](./images/sbRh3HL.png)

程序代码链接：[https://makecode.microbit.org/_b7JL2Yd3q3Km](https://makecode.microbit.org/_b7JL2Yd3q3Km)

你也能通过下列窗口直接下载代码：

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_b7JL2Yd3q3Km" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>

### 结果

点阵显示屏实时显示超声波模块与物体之间的距离，单位为cm。


## 文档
---
[WIKI](https://github.com/elecfreaks/learn-cn)

## 常见问题
---
