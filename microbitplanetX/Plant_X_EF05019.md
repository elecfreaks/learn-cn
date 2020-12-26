# 双路巡线模块

## 简介
两路巡线模块集成了两组反射式红外对管，可通过它来制作小车智能巡线项目。

![](./images/05019_01.png)

## 特性
---
- RJ11端口设计，防止误插，易于使用。
## 技术规格
---

项目 | 参数 
:-: | :-: 
SKU|EF05019
接口|RJ11
接口类型|数字输出
工作电压|3.3V
有效距离|2~12mm
黑线|输出低电平
白线|输出高电平





## 外形与定位尺寸
---


![](./images/05019_02.png)


## 快速上手
---

### 所需器材及连接示意图
---

- 如下图所示，将双路巡线模块连接到哪吒扩展板的J1端口。


![](./images/05019_03.png)

## makecode编程
---

### 步骤 1
在MakeCode的代码抽屉中点击“高级”，查看更多代码选项。

![](./images/05001_04.png)

为了给双路巡线模块编程，我们需要添加一个扩展库。在代码抽屉底部找到“扩展”，并点击它。这时会弹出一个对话框，搜索”PlanetX“，然后点击下载这个代码库。

![](./images/05001_05.png)

*注意：*如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。
### 步骤 2
### 如图所示编写程序

![](./images/05019_06.png)


### 参考程序
请参考程序连接：[https://makecode.microbit.org/_8fT96MWdg9Ux](https://makecode.microbit.org/_8fT96MWdg9Ux)

你也可以通过以下网页直接下载程序，下载完成后即可开始运行程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_8fT96MWdg9Ux" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

### 结果
- 根据双路巡线模块检测到的不同状态，micro:bit上的LED矩阵会显示不同的图标。

## python编程
---


### 步骤 1
为了方便的使用python对行星系列传感进行编程，我们可以使用已经编写好的库[PlanetX_MicroPython]，只需要调用函数并修改参数即可实现对应的功能。

下载压缩包并解压[PlanetX_MicroPython](https://github.com/lionyhw/PlanetX_MicroPython/archive/master.zip)

推荐使用官方平台：[Python editor](https://python.microbit.org/v/2.0)进行编程

![](./images/05001_07.png)

为了给双路巡线模块编程，我们需要添加enum.py和tracking.py两个文件。点击Load/Save，然后点击Show Files（1）下拉菜单，再点击Add file在本地找到下载并解压完成的PlanetX_MicroPython文件夹，从中选择enum.py和tracking.py两个文件添加进来。

![](./images/05001_08.png)
![](./images/05001_09.png)
![](./images/05019_10.png)

### 步骤 2
### 参考程序
```
from microbit import *
from enum import *
from tracking import *

tracking = TRACKING(J1)
while True:
    if tracking.get_state() == 11:
        display.show(Image.YES)
    elif tracking.get_state() == 10:
        display.show(Image.SAD)
    elif tracking.get_state() == 00:
        display.show(Image.NO)
    elif tracking.get_state() == 01:
        display.show(Image.HAPPY)
```


### 结果
- 根据双路巡线模块检测到的不同状态，micro:bit上的LED矩阵会显示不同的图标。
## 相关案例
---

## 技术文档
---
