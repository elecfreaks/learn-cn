# 多功能扩展板:悟空（Wukong）

## 简介
- - - - -

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitExtensionModule/images/wukong_00.jpg)

悟空 是一款基于micro:bit的高集成度多功能扩展板，它的大小与micro:bit相近，功能十分丰富，集成了蜂鸣器、舵机驱动、电机驱动等。
自带400mAh锂电池包，板载电源管理系统，支持快速充电，充满仅需20分钟，满负载运行时间可达到40分钟以上。
扩展板底座为乐高标准 7 X 5 方形积木块，完美接入乐高积木。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitExtensionModule/images/wukong_01.jpg)

## 特性 
- - - - -

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
|产品编号|EF08207|SKU|-|
| 尺 寸 |40.00 X 58.12 X 24.53 mm|高度包含乐高底座，不包含主板|手工测量，以实物为准|
| 重 量 |41.6g|包含底座，包含锂电池包|手工测量，以实物为准|
| 电源系统 |单击电源开关开机，双击关机|4颗LED灯指示电量，电路支持快充|也可通过板载USB口供电|
| 供电电池 |400mAh聚合物锂电池|快充20分钟，满载工作40分钟以上|安全防爆|
| 工作电压 |3.7v~5v|锂电池供电3.7v，USB口直供5v|-|
| 工作温度 |-20℃~60℃|充电温度0℃~40℃|-|
| 电机驱动 |2路 (M1，M2)|板载电机驱动电路驱动 |-|
| 舵机驱动 |8路舵机接口 (S0~S7)|板载舵机驱动电路驱动|-|
| IO口引出 |P0、P1、P2、P8、P12、P13、P14、P15、IIC|支持拖动3V和5V器件|GVS端子|
| Rainbow LED |LED0、LED1、LED2、LED3|扩展Neopixel库使用|连接到micro:bit引脚P16|
| 蜂鸣器 |无源蜂鸣器，板载功能开关|使用music库驱动|连接到micro:bit引脚P0|
| 氛围灯 |反面边缘8颗LED灯，编程控制|常亮，闪亮，呼吸灯效果|开机时会闪亮一次，为正常现象
| 乐高底座 |标准7 x 5 长方形底座|电池包镶嵌底座中央|-|


## 外型与定位尺寸
- - - - -

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitExtensionModule/images/wukong_02.png)


## 主要模块介绍  
- - - - -

### 开关，usb供电口及电量指示灯

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitExtensionModule/images/wukong_07.jpg)

### micro:bit主板插销

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitExtensionModule/images/wukong_15.jpg)

### 电机驱动接口  

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitExtensionModule/images/wukong_03.jpg)

### 舵机驱动接口

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitExtensionModule/images/wukong_04.jpg)

### 8路标准GVS接口及5v接口

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitExtensionModule/images/wukong_05.jpg)

### I2C排母接口

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitExtensionModule/images/wukong_06.jpg)

### 4颗Rainbow LED

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitExtensionModule/images/wukong_08.jpg)

### 蜂鸣器(背面)及蜂鸣器功能开关

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitExtensionModule/images/wukong_09.jpg)
![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitExtensionModule/images/wukong_10.jpg)

### 8颗氛围灯(背面)

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitExtensionModule/images/wukong_11.jpg)

### 锂电池接口(背面)

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitExtensionModule/images/wukong_12.jpg)

### 乐高固定螺丝孔M3(背面)

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitExtensionModule/images/wukong_13.jpg)


## 快速上手  
- - - - -

### 硬件连接

- 将micro:bit主板插入主板插销座，主板带LOGO一面，朝向蜂鸣器开关一侧。
- 单击一次电源开关打开电源。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitExtensionModule/images/wukong_20.jpg)

### 软件编程平台

- [微软makecode积木块式在线编程:makecode.microbit.org](makecode.microbit.org)

### 添加专属积木块库

- 点击高级`Advanced`，在下拉菜单中点击扩展`Extensions`，进入添加积木块菜单。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/smart_cutebot/images/cutebot-pk-1.png)

- 在搜索框中搜索`wukong`，点击图片中`wukong`，添加扩展包。
- 添加完成。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/smart_cutebot/images/wukong_14.png)

## 相关文档
- - - - -
