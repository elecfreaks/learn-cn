# 130带扇叶电机电子积木

## 简介
---
OCTOPUS Motor Brick是一种简单的电子积木式风扇电机驱动模块

 ![](./images/vu7ViBU.jpg)

## 特性
---
- 三线端口设计，防止误插，易于使用。

## 技术规格
---

项目 | 参数 
:-: | :-: 
SKU|EF04059
电源|3.3V-5V
N-MOS| IRLML2502TRPBF具有高电流驱动能力
低功率风扇电机|工作电流120mA
工作温度|-25~85℃
尺寸|39.33mm×31.28mm

## 外形与定位尺寸
---

 ![](./images/bFU1faL.jpg)

## 快速上手
---
### 所需器材及连接示意图

- 使用130带扇叶电机电子积木时，需要使用电池盒进行供电
- 如图连接扩展板的P16口

***以octupus：bit为例***

 ![](./images/ZBTdQp1.png)


### 如图所示编写程序
按A键向P16口写入1，按B键向P16口写入0

 ![](./images/04059_01.png)

### 参考程序
请参考程序连接：[https://makecode.microbit.org/_fUURco9Rj8mH](https://makecode.microbit.org/_fUURco9Rj8mH)

你也可以通过以下网页直接下载程序，下载完成后即可开始运行程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_fUURco9Rj8mH" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

### 结果

- 当按下A键时电机旋转，当按下B键时电机停止旋转。

## Python 编程

### 步骤 1
下载压缩包并解压[Octopus_MicroPython-master](https://github.com/lionyhw/Octopus_MicroPython/archive/master.zip)
打开[Python editor](https://python.microbit.org/v/2.0)

![](./images/05001_07.png)

为了给130带扇叶电机模块编程，我们需要添加fans.py。点击Load/Save，然后点击Show Files（1）下拉菜单，再点击Add file在本地找到下载并解压完成的Octopus_MicroPython-master文件夹，从中选择fans.py添加进来。

![](./images/05001_08.png)
![](./images/05001_09.png)
![](./images/04059_10.png)

### 步骤 2
### 参考程序
```
from microbit import *
from fans import *

f = FANS(pin1)
while True:

    f.set_fans(1, 100)
    sleep(3000)
    f.set_fans(0, 0)
    sleep(2000)
```


### 结果
- 风扇转动三秒，停止两秒。

## 相关案例
---

## 技术文档
---
## 常见问题
---
1.在硬件连接以及程序正确的情况下，发现电机无法转动。
- 出现这类问题通常是因为供电不足，工作电压应为3.3V~5V,工作电流应为120mA.
- 如果使用带USB供电的扩展板，则使用USB进行供电。
- 如果使用micro:bit进行供电，则可以使用micro:bit上的USB接口以及电池接口同时进行供电
- 如果使用扩展板，请勿同时使用扩展板的供电接口和micro:bit的供电接口。
2.发现接入电机后，不进行编程电机也会转动。
- 在接入电机时，需注意避开micro:bit的共用引脚

micro:bit版本 |LED共用引脚 | 按键共用引脚
:-: | :-: | :-: 
micro:bit V2|P3\P4\P6\P7\P10|P5\P11
micro:bit V1|P3\P4\P6\P7\P9\P10|P5\P11
