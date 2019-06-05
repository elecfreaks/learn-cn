# robit智能小车案例01：超声波测距

## 目的
---

- 了解什么是超声波，如何用超声波测距。
- 使用Robit智能小车来测距。


## 使用材料
---

- 1 x Robit智能小车


## 背景知识
---

### 什么是超声波

[超声波](https://zh.wikipedia.org/wiki/%E8%B6%85%E8%81%B2%E6%B3%A2)是一种频率高于20000赫兹的声波，它的方向性好，穿透能力强，易于获得较集中的声能，在水中传播距离远，可用于测距、测速、清洗、焊接、碎石、杀菌消毒等。超声波因其频率下限大于人的听觉上限而得名。

### 超声波测距原理

超声波发射器向某一方向发射超声波，在发射时刻的同时开始计时，超声波在空气中传播，途中碰到障碍物就立即返回来，超声波接收器收到反射波就立即停止计时。根据接收器接到超声波时的时间计算距离，与雷达测距原理相似。

![](./images/vSFTiuw.jpg)

### 超声波模块 ###

- [Sonar:bit](https://www.elecfreaks.com/estore/sonar-bit-for-micro-bit-ultrasonic-sensor-distance-measuring-3v-5v.html)是一个3线宽压超声波模块，它可以工作电压为3.0V-5V，3.3v或5V的单片机系统均能使用；它只需要3根线（G、V、S）就可以工作，比常规的4线超声波模块节省一个IO口。Sonar:bit量程为4cm~400cm，测量数据稳定准确，误差仅为±1cm。可应用于短距离测量、智能小车、机器人等场合。

![](./images/wZIpIu7.jpg)![](./images/7QseHWh.jpg)


## 硬件连接图
---

如图所示，将超声波模块与Robit主板P1口使用3pin杜邦线连接。


![](./images/xb7vuYW.jpg)

![](./images/Hz4ZGz3.jpg)


## 软件
---

[微软makecode](https://makecode.microbit.org/#)

## 编程
---

### 步骤 1
- 在MakeCode的代码抽屉中点击Advanced，查看更多代码选项。

![](./images/2qCyzQ7.png)

- 为了给robit智能小车编程，我们需要添加一个扩展库。在代码抽屉底部找到“Extension”，并点击它。这时会弹出一个对话框。搜索“robit"，然后点击下载这个代码库。

![](./images/CyQSlJk.png)

注意：如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。

### 步骤 2

在`Basic`中拖出一个`forever`积木块，在其中插入`show number`积木块。

在`Sonarbit`中拖出`Ulirasonic distance`积木块，选择`cm`和`P1`。这条语句作用为连接超声波模块到`P1`口返回数据为`cm`。

![](./images/EhBi4Sm.png)

### 程序

请参考程序连接：[https://makecode.microbit.org/_DdTdurbyrVvH](https://makecode.microbit.org/_DdTdurbyrVvH)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_DdTdurbyrVvH" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  

**注意：** 该超声波模块检测的最大距离大约为400cm。

### 现象

超声波模块会实时返回距离，并且显示在Micro:bit的5X5点阵上，距离单位为厘米CM。

![](./images/pKxQMu8.jpg)


## 思考
---
超声波测距显示距离为0有几种情况？


## 常见问题
---


## 相关阅读  
---

 
