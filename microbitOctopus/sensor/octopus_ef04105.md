# RFID传感器

## 简介
RFID传感器利用无线射频方式对记录媒体（电子标签或射频卡）进行读写，从而达到识别目标和数据交换的目的。

![](./images/04105_01.png)

## 特性

三线端口设计，防止误插，易于使用。

## 技术规格


项目 | 参数 
:-: | :-: 
SKU|EF04105
接口|IIC
接口类型|IIC通信
工作电压|3.3V
额定电流|50mA
核心IC|PN5321A3

## 外形与定位尺寸

![](./images/04105_02.png)


## 快速上手

### 所需器材及连接示意图

如下图所示，将RFID传感器连接到sensor:bit的IIC端口。

![](./images/04105_03.png)

## makecode编程

### 添加扩展库
在MakeCode的代码抽屉中点击`扩展`。

![](./images/04105_04.png)

为了给RFID传感器编程，我们需要添加一个扩展库。在弹出页面，搜索`https://github.com/elecfreaks/pxt-OctopusX`，然后点击下载这个代码库。

![](./images/04105_05.png)

*注意：*如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。

### RFID写入数据

![](./images/05047_06.png)

请参考程序连接：[https://makecode.microbit.org/_19ePfj3idL1h](https://makecode.microbit.org/_19ePfj3idL1h)

你也可以通过以下网页修改程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_19ePfj3idL1h" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  

### 现象
当开机时，将电子标签放置在RFID下方，RFID将数据写入电子标签，然后读取电子标签数据并显示在micro:bit的点阵屏上。

### RFID读取数据

![](./images/05047_07.png)

请参考程序连接：[https://makecode.microbit.org/_fXU8hWYc9Lhu](https://makecode.microbit.org/_fXU8hWYc9Lhu)

你也可以通过以下网页修改程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_fXU8hWYc9Lhu" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  

### 现象
当开机时，将电子标签放置在RFID下方，RFID读取电子标签数据并显示在micro:bit的点阵屏上。
