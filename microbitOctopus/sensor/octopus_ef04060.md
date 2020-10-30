# MQ3气体传感器电子积木

## 简介
MQ-3气体传感器所使用的气敏材料是在清洁空气中电导率较低的二氧化锡(SnO2)。当传感器所处环境中存在酒精蒸汽时，传感器的电导率随空气中酒精气体浓度的增加而增大。


![](./images/04060_01.png)






## 特性
---
- 三线端口设计，防止误插，易于使用。
## 技术规格
---

项目 | 参数 
:-: | :-: 
SKU|EF04060
接口类型|模拟
引脚定义|S-Sigal V-VCC G-GND
工作电压|3V
产品尺寸|38x27mm


尺寸：

## 外形与定位尺寸
---



![](./images/04060_02.png)



## 快速上手
---

### 所需器材及连接示意图
---

- 如下图所示，将MQ3气体传感器连接到扩展板的P1端口。

***以iot：bit为例***



![](./images/04060_03.png)


*注意：*由于器件耗电量过大，所以必须使用扩展板的USB接口供电，目前支持USB接口供电的扩展板有iot:bit和悟空扩展板。

### 如图所示编写程序



![](./images/04060_04.png)


### 参考程序
请参考程序连接：[https://makecode.microbit.org/_KJVXj9Co2UXU](https://makecode.microbit.org/_KJVXj9Co2UXU)

你也可以通过以下网页直接下载程序，下载完成后即可开始运行程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_KJVXj9Co2UXU" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

### 结果
- 硬件连接后需要预热三分钟，等读数相对稳定后再将传感器探头靠近酒精气体进行检测。
- 随着环境酒精气体浓度的改变，micro:bit的led显示器上显示的数值随之升高而变大。


## python编程
---


### 步骤 1
下载压缩包并解压[Octopus_MicroPython-master](https://github.com/lionyhw/Octopus_MicroPython/archive/master.zip)
打开[Python editor](https://python.microbit.org/v/2.0)

![](./images/05001_07.png)

为了给MQ3气体传感器编程，我们需要添加ethanol.py。点击Load/Save，然后点击Show Files（1）下拉菜单，再点击Add file在本地找到下载并解压完成的Octopus_MicroPython-master文件夹，从中选择ethanol.py添加进来。

![](./images/05001_08.png)
![](./images/05001_09.png)
![](./images/04060_10.png)

### 步骤 2
### 参考程序
```
from microbit import *
from ethanol import *

ethanol = ETHANOL(pin1)
while True:
    display.scroll(ethanol.get_ethanol())
```


### 结果
- micro:bit的LED矩阵显示当前MQ3气体传感器的返回值。

## 相关案例
---

## 技术文档
---
