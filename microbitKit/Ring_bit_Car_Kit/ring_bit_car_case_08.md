# 案例08 加速度计远程控制

## 目的
---
- 使用另一块micro:bit的加速度计远程控制小车。

## 使用材料
---
- 1 x Ring:bit Car 套件
- 2 x micro:bit主板

## 背景知识 ##
### 什么是无线电 ###
---
- 无线电无线电技术是通过无线电波传播信号的技术，其原理在于，导体中电流强弱的改变会产生无线电波。利用这一现象，通过调制可将信息加载于无线电波之上。当电波通过空间传播到达收信端，电波引起的电磁场变化又会在导体中产生电流。通过解调将讯息从电流变化中提取出来，就达到了资讯传递的目的。

### 什么是加速度计 ###
---
- 加速度传感器是一种能够测量加速度的传感器。通常由质量块、阻尼器、弹性元件、敏感元件和适调电路等部分组成。传感器在加速过程中，通过对质量块所受惯性力的测量，利用牛顿第二定律获得加速度值。根据传感器敏感元件的不同，常见的加速度传感器包括电容式、电感式、应变式、压阻式、压电式等。

 *新版和旧版micro:bit加速度计芯片有所区别。新版micro:bit将电子罗盘和加速度计合并为一个芯片，使用方法不变。*

 ![](./images/2n6TbVZ.png)  ![](./images/F0frwo6.jpg)

## 硬件连接图
---
- Ring:bit扩展版的P1口连接左轮舵机（即图中右下角的P1,3.3v，GND），P2口连接右轮舵机（即图中左上角的P2，3.3V，GND），将选择开关拨到P2的位置。
![](./images/MT6Y00d.png)

## 软件平台
---
[微软makecode](https://makecode.microbit.org/#)在线积木块编程[https://makecode.microbit.org/#](https://makecode.microbit.org/#)

## 编程
---
### 步骤 1
- 在MakeCode的代码抽屉中点击Advanced，查看更多代码选项。

![](./images/2qCyzQ7.png)

- 为了给Ring:bit套件编程，我们需要添加一个代码库。在代码抽屉底部找到“Add Package”，并点击它。这时会弹出一个对话框。搜索“ringbit"，然后点击下载这个代码库。

![](./images/1Wq2Mov.jpg)

注意：如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。

### 步骤 2 ###

- 陀螺仪控制算法较为复杂，详解请点击文章：加速度计算法

- 你也可以直接使用以下程序

### 遥控器端程序
请参考程序连接：[https://makecode.microbit.org/_AT4PoHKdVi6L](https://makecode.microbit.org/_AT4PoHKdVi6L)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_AT4PoHKdVi6L" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

### Ring:bit 小车端程序 ###
请参考程序连接：[https://makecode.microbit.org/_aRxV2TAXeYgH](https://makecode.microbit.org/_aRxV2TAXeYgH)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_aRxV2TAXeYgH" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---


## 结论
---
- Ring:bit小车随着陀螺仪的方向行驶，陀螺仪倾斜角度控制行车速度。
![](./images/5fPKpKC.gif)

## 思考
---
- 

## 常见问题
---


## 相关阅读  
---

