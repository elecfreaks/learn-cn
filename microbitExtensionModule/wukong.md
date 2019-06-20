# 多功能扩展板:悟空（Wukong）

## 简介
---

悟空 是一款基于micro:bit的高集成度多功能扩展板，它的大小与micro:bit相近，功能十分丰富，集成了蜂鸣器、舵机驱动、电机驱动等。
自带400mAh锂电池包，板载电源管理系统，支持快速充电，充满仅需20分钟，满负载运行时间可达到40分钟以上。
扩展板底座为乐高标准 7 X 5 方形积木块，完美接入乐高积木块。


## 特性 
---

- 外形小巧，高集成度
- 标准乐高积木接口
- 以GVS端子形式扩展出大部分IO口
- 单独引出IIC接口，能直接插入OLED、BME280等IIC器件。
- 集成蜂鸣器和蜂鸣器开关。
- 集成电机驱动电路。
- 集成舵机驱动电路。
- 支持5V传感器工作。
- 自带锂电池包，集成电池管理系统，四颗LED灯指示电量。
- 电源电路支持快充。


## 参数
- - - - -

| 参数 | 详情 | 说明 | 备注 |
|:-:|:-:|:-:|:-:|
| 尺 寸 |40.00 X 58.12 X 24.53 mm|高度包含乐高底座，不包含主板|手工测量会有误差，以实物为准|
| 重 量 |41.6g|包含底座，包含锂电池包|手工测量会有误差，以实物为准|
| 供电系统 |400mAh软包锂电池，支持快充|快充20分钟，满载工作40分钟以上|也可通过板载USB口供电|
| 电机驱动 |2路 (M1，M2)|板载电机驱动电路驱动 |-|
| 舵机驱动 |8路舵机接口 (S0~S7)|板载舵机驱动电路驱动|-|
| IO口引出 |P0、P1、P2、P8、P12、P13、P14、P15、IIC|支持拖动3V和5V器件|-|
| Rainbow LED |LED0、LED1、LED2、LED3|扩展Neopixel库使用|连接到micro:bit引脚P16|
| 蜂鸣器 |有源蜂鸣器，板载功能开关|使用music库驱动|连接到micro:bit引脚P0|
|尺 寸||
|尺 寸||
|尺 寸||
|尺 寸||
|尺 寸||
|尺 寸||
|尺 寸||
|尺 寸||
|尺 寸||

### 外型与定位尺寸  
![](./images/gB0wNrj.png)

## 引脚接口框图
![](./images/GyigPRt.png)

## 主要功能模块介绍  
---  

### 耳机插座  
![](./images/0iA1JlU.png)

耳机通过P0口控制，插入耳机时，蜂鸣器自动断开。

### 蜂鸣器  
![](./images/TyBn9U6.png)

蜂鸣器通过P0口控制，插入耳机时，蜂鸣器自动断开。

### 16路标准GVS接口  
![](./images/lu64mbc.png)

这是16路GVS标准接口，可扩展3v的电子积木模块。

### I2C接口
![](./images/AzBhRRS.png)

这是一组I2C接口排母接口，可直接接入OLED模块。

![](./images/VEl3AeH.png)

这是一组I2C接口排针接口。

## 快速上手  
---  

### 硬件连接  

将micro:bit主板插入sensor:bit主板。
![](./images/WLLJgP2.jpg)

### 软件编程  

打开makecode，编写程序让蜂鸣器播放音乐。
程序代码链接：[https://makecode.microbit.org/_3At2iE5Ue3XK](https://makecode.microbit.org/_3At2iE5Ue3XK)

你也能通过下列窗口直接下载代码
<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_3At2iE5Ue3XK" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>

### 结果  

按下按钮A时，蜂鸣器播放音乐，插上耳机时可以通过耳机听到音乐，同时蜂鸣器会停止播放音乐。

## 常见问题
