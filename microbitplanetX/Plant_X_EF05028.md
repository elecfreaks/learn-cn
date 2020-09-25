# PM2.5传感器

## 简介
PM2.5传感器是一款可以检测环境PM2.5浓度的传感器模块，它的工作原理是基于ZH03激光粉尘传感器模组，通过这个模组对空气中的粉尘颗粒物进行检测。

![](./images/05028_01.png)

## 特性
---
- RJ11端口设计，防止误插，易于使用。
## 技术规格
---

项目 | 参数 
:-: | :-: 
SKU|EF05028
接口|RJ11
接口类型|数字输出
工作电压|3.3V






## 外形与定位尺寸
---


![](./images/05028_02.png)


## 快速上手
---

### 所需器材及连接示意图
---

- 如下图所示，将PM2.5传感器连接到哪吒扩展板的J1端口，OLED显示屏连接到哪吒扩展板的IIC端口。


![](./images/05028_03.png)

## makecode编程
---

### 步骤 1
在MakeCode的代码抽屉中点击“高级”，查看更多代码选项。

![](./images/05001_04.png)

为了给PM2.5传感器编程，我们需要添加一个扩展库。在代码抽屉底部找到“扩展”，并点击它。这时会弹出一个对话框，搜索”PlanetX“，然后点击下载这个代码库。

![](./images/05001_05.png)

*注意：*如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。
### 步骤 2
### 如图所示编写程序

![](./images/05028_06.png)


### 参考程序
请参考程序连接：[https://makecode.microbit.org/_itg0eE91PTz7](https://makecode.microbit.org/_itg0eE91PTz7)

你也可以通过以下网页直接下载程序，下载完成后即可开始运行程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_itg0eE91PTz7" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

### 结果
- 通过OLED显示屏显示当前PM2.5的返回值。

## python编程
---


### 步骤 1
下载压缩包并解压[PlanetX_MicroPython](https://github.com/lionyhw/PlanetX_MicroPython/archive/master.zip)
打开[Python editor](https://python.microbit.org/v/2.0)

![](./images/05001_07.png)

为了给PM2.5传感器编程，我们需要添加pm25.py和enum.py两个文件。点击Load/Save，然后点击Show Files（1）下拉菜单，再点击Add file在本地找到下载并解压完成的PlanetX_MicroPython文件夹，从中选择pm25.py和enum.py文件添加进来。

![](./images/05001_08.png)
![](./images/05001_09.png)
![](./images/05028_10.png)

### 步骤 2
### 参考程序
```
from microbit import *
from enum import *
from pm25 import *

pm2_5 = PM25(J1)
while True:
    display.scroll(pm2_5.get_pm25())
    sleep(1000)

```


### 结果
- 通过micro:bit的LED矩阵显示当前PM2.5传感器的返回值。
## 相关案例
---

## 技术文档
---
