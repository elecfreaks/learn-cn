# 电容式土壤湿度电子积木

## 简介
---

Octopus Analog Capacitive Soil Moisture Sensor是我们OCTOPUS系列的土壤湿度传感器电子积木，它的基本设计是根据OCTOPUS电子积木系列设定的，它的外形、PCB固定孔、电子积木的接口的设定是相同的。

采用电容感应原理来检测土壤湿度，避免了电阻式传感器极易被腐蚀的问题，极大地延长了它的工作寿命。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitSensor/sensor/images/04097_00.jpg)

## 特性 
---
- 不易腐蚀。
- 采用3V供电，可支持micro:bit。
- 接线方便。

## 参数
---
- 品名：电容式土壤湿度电子积木
- SKU：EF04097
- 工作电压：DC 3~5.5V
- 连接模式：G-GND，V-VCC，S-信号引脚
- 尺寸：19 x 76mm
- 净重：5.5g

## 外型与定位尺寸  
---
![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitSensor/sensor/images/04097_01.png)

## 快速上手  
---  
### 硬件连接  

将模块通过带扣杜邦线插入octopus:bit上的P1引脚，将micro:bit主板插入octopus:bit。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitSensor/sensor/images/04097_02.png)

### 软件编程  

打开makecode，模拟读取P1口，返回值为土壤湿度，显示在LED点阵显示屏上。
程序代码链接：[https://makecode.microbit.org/_4urWJCMeuh4L](https://makecode.microbit.org/_4urWJCMeuh4L)

你也能通过下列窗口直接下载代码
<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;">
 <iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" 
         src="https://makecode.microbit.org/#pub:_4urWJCMeuh4L" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin">
 </iframe>
</div>  

### 结果  

点阵显示屏显示当前土壤湿度值。

## 常见问题
