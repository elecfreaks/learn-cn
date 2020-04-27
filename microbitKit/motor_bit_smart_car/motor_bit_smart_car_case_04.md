# 案例04 自动避障

## 目的
---

- 使用motor:bit智能车载套件完成超声波避障功能。

## 使用材料
---

- 1 x motor:bit 智能车载套件

## 背景知识
---
### 什么是超声波
- [超声波](https://zh.wikipedia.org/wiki/%E8%B6%85%E8%81%B2%E6%B3%A2)是一种频率高于20000赫兹的声波，它的方向性好，穿透能力强，易于获得较集中的声能，在水中传播距离远，可用于测距、测速、清洗、焊接、碎石、杀菌消毒等。超声波因其频率下限大于人的听觉上限而得名。
### 超声波测距原理
- 超声波发射器向某一方向发射超声波，在发射时刻的同时开始计时，超声波在空气中传播，途中碰到障碍物就立即返回来，超声波接收器收到反射波就立即停止计时。根据接收器接到超声波时的时间计算距离，与雷达测距原理相似。
- ![](./images/vSFTiuw.jpg)

## 硬件连接图
---

如图所示，将超声波模块连接到P10引脚。

![](./images/t4vFZ0y.jpg)

![](./images/kzPngGo.jpg)

## 软件
---
[微软makecode](https://makecode.microbit.org/#)在线积木块编程[https://makecode.microbit.org/#](https://makecode.microbit.org/#)

## 编程
---
### 步骤 1
在MakeCode的代码抽屉中点击高级，查看更多代码选项。

![](./images/motor_bit_case_01.png)

为了给motorbit主板编程，我们需要添加一个代码库。在代码抽屉底部找到“扩展”，并点击它。这时会弹出一个对话框。搜索“motorbit"，然后点击下载这个代码库。

![](./images/motor_bit_case_02.png)

注意：如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。

### 步骤 2
程序初始化时，定义了一个away变量，用来表示检测到障碍物的距离，并将它置为0。

设置左轮右轮速度均为100。

![](./images/motor_bit_case_04_03.png)

### 步骤3

创建一个无限循环循环，实时的读取超声波模块返回的数据，并且赋值给away。

![](./images/motor_bit_case_04_04.png)

#### 防撞停车

当检测距离(away)距离小于8cm时，停车，暂停300ms后，设置左右轮速度为负数实现倒车，延时600ms。

![](./images/motor_bit_case_04_05.png)

#### 转向避障

当检测距离(away)距离小于15cm时，生成一个0到100的随机数。

当随机数小于50的时候右轮赋负值，右轮倒转完成右转。

当随机数大于50的时候左轮赋负值，左轮倒转完成左转。

![](./images/motor_bit_case_04_06.png)

如果检测距离(away)大于15cm，设置左右轮速度为100前进。

![](./images/motor_bit_case_04_07.png)

### 程序
请参考程序连接：[https://makecode.microbit.org/_hkKRJFFa6WLu](https://makecode.microbit.org/_hkKRJFFa6WLu)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_hkKRJFFa6WLu" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---


## 结论
---
- 车辆上电以100的速度向前直行，当距离障碍小于8cm且不等于0cm时候，车辆停止运动，0.3s后开始倒车。
- 当距离障碍小于15cm时，随机左转或者右转，以避开障碍物。
- 检测到其他情况是，以100的速度继续前进。

## 思考
---

## 常见问题
---


## 相关阅读  
---

