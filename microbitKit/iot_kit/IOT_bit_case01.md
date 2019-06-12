# iot套件案例01：空气质量监测站

## 目的
---

- 制作一个空气质量监测站。

## 使用材料
---

- 1 x [IOT:kit(物联网环境科学套件):https://www.elecfreaks.com/store](https://www.elecfreaks.com/store/micro-bit-smart-science-iot-kit-with-micro-bit.html)

## 背景知识
---
### 什么是物联网
- [物联网](https://zh.wikipedia.org/wiki/%E8%B6%85%E8%81%B2%E6%B3%A2)是一个由相互关联的计算设备、机械和数字机器、物体、动物或人组成的系统，这些计算机设备、机械和数字机器、物体、动物或人具有唯一标识符（uids），并且能够在网络上传输数据，而不需要人与人或人与计算机之间的交互。
简单概括可为：把所有物品通过信息传感设备与互联网连接起来，进行信息交换，即物物相息，以实现智能化识别和管理。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_01_01.png)

## 硬件连接图
---

如图所示，将灰尘传感器模块的`LED IN`连接到`P9`口，`OUT`连接到`P10`口。

OLED屏幕连接`IIC`接口。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_01_02.png)

## 软件
---

[微软makecode](https://makecode.microbit.org/#)

## 编程
---

### 步骤 1
- 在MakeCode的代码抽屉中点击Advanced，查看更多代码选项。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/iot_bit_11.jpg)

- 为了给IoT物联网环境科学套件编程，我们需要添加一个扩展库。在代码抽屉底部找到“Extension”，并点击它。这时会弹出一个对话框。搜索“IOT"，然后点击下载这个代码库。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/iot_bit_12.jpg)

*注意：*如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。
### 步骤 2

在`on start`中插入`initialize OLED`积木块，参数填入`64*128`。

初始化OLED屏幕为`64`像素*`128`像素。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_01_03.png)

### 步骤 2

在`forever`中依次插入`clear OLED display`积木块，`show string`积木块，`show number`积木块。

显示字符`Dust(ug/m3):`，显示dust灰尘模块返回值。

暂停`60s`，一分钟显示一次。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_01_04.png)

### 程序

请参考程序连接：[https://makecode.microbit.org/_7EPDui88d7v3](https://makecode.microbit.org/_7EPDui88d7v3)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_7EPDui88d7v3" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  

### 现象
---
每隔一分钟会显示一次当前空气中的灰尘数。

## 思考
---
如何在空气质量很差的时候发出报警。

## 常见问题
---
## 相关阅读  
---
