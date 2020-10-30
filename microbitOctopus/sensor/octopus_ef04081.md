# 噪音传感器电子积木

## 简介
---
声音传感器对声音强度特别敏感，可用于检测环境声级，更大的噪声会有更大的输出正弦波振幅。

 ![](./images/hP4azP5.png)

## 特性
---
- 三线端口设计，防止误插，易于使用。

## 技术规格
---

项目 | 参数 
:-: | :-: 
SKU|EF04081
输出电压|3.3V-5V
正弦波|大声的噪声带来更大的输出正弦波振幅
## 外形与定位尺寸
 ![](./images/uPRIFLt.png)

## 快速上手
---

### 所需器材及连接示意图

- 如图连接扩展板的P1口

***以sensor：bit为例***

 ![](./images/I9xA8Ms.png)

### 添加Package

### 如图所示编写程序
1.添加led显示模块

2.显示读取到的声音信息



![](./images/04081_01.png)



### 参考程序

请参考程序连接：[https://makecode.microbit.org/_c9P1uiUkC7JE](https://makecode.microbit.org/_c9P1uiUkC7JE)

你也可以通过以下网页直接下载程序，下载完成后即可开始运行程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_c9P1uiUkC7JE" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

### 结果
- micro：bit的点阵屏上显示分贝信息。

## python编程
---


### 步骤 1
下载压缩包并解压[Octopus_MicroPython-master](https://github.com/lionyhw/Octopus_MicroPython/archive/master.zip)
打开[Python editor](https://python.microbit.org/v/2.0)

![](./images/05001_07.png)

为了给噪音传感器编程，我们需要添加noise.py。点击Load/Save，然后点击Show Files（1）下拉菜单，再点击Add file在本地找到下载并解压完成的Octopus_MicroPython-master文件夹，从中选择noise.py添加进来。

![](./images/05001_08.png)
![](./images/05001_09.png)
![](./images/04081_10.png)

### 步骤 2
### 参考程序
```
from microbit import *
from noise import *

s = NOISE(pin1)
while True:
    x = s.get_noise()
    display.scroll(x)
```


### 结果
- 在micro:bit的LED矩阵上显示当前噪音传感器返回的读数。



## 相关案例
---

## 技术文档
---
