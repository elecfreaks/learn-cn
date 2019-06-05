# 电压检测电子积木

## 简介
---
分压器可以检测高达50V的电源电压。分压器模块基于电阻器（1K和15K精密电阻器）

 ![](./images/fl6I2w5.jpg)

## 特性
---
- 分压器原理。电压检测模块允许输入电压降低16倍。由于micro:bit模拟输入电压为 3.3V，因此电压检测模块的输入电压不能大于3.3Vx16 = 52.8V。由于micoro:bit的10位ADC，这意味着采样分辨率为0.003225V（3.3V / 1023）。因此模块的最小输入电压为0.00489Vx3.3=0.01064V。
- tips:所有octopus积木块都支持scrach编程。  

## 技术规格
---
项目 | 参数 
:-: | :-: 
SKU|EF04039
类型|模拟
输入电压（DC）|最大50V，最小0.01064V
检测范围|检测电源电压高达50V

## 外形与定位尺寸
---
 ![](./images/doEjdcR.png)

## 快速上手
---
### 所需器材及连接示意图
如下图所示，连接扩展板的P1口。

***以sensor:bit为例***

 ![](./images/fcHzFyT.png)

### 添加Package

### 如图所示编写程序

 ![](./images/6DO11mU.png)

### 参考程序
请参考程序连接：[https://makecode.microbit.org/_AXD2gM3J36Jz](https://makecode.microbit.org/_AXD2gM3J36Jz)

你也可以通过以下网页直接下载程序，下载完成后即可开始运行程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_AXD2gM3J36Jz" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

### 结果
- micro:bit led灯上显示接收到的电压信息。
## 相关案例
---

## 技术文档
---
