# iot套件案例03：环境质量监测站

## 目的
---

- 制作一个环境质量监测站。


## 使用材料
---

- 1 x [IOT:kit(物联网环境科学套件)]()


## 背景知识
---

### 什么是环境检测

- [环境检测：]()环境监测是利用GIS技术对环境监测网络进行设计,环境监测收集的信息又能通过GIS适时储存和显示，并对所选评价区域进行详细的场地监测和分析。


## 硬件连接图
---

如图所示，将光线传感器模块连接到`P1`口。

BME280模块连接到`IIC`接口`SCL-P19` `SDA-P20`。

OLED屏幕连接`IIC`接口。 

![](./images/lXpPGTA.png)


## 软件
---

[微软makecode](https://makecode.microbit.org/#)

## 编程
---

### 步骤 1
- 在MakeCode的代码抽屉中点击Advanced，查看更多代码选项。

![](./images/2qCyzQ7.png)

- 为了给IOT物联网环境科学套件编程，我们需要添加一个扩展库。在代码抽屉底部找到“Extension”，并点击它。这时会弹出一个对话框。搜索“IOT"，然后点击下载这个代码库。

![](./images/xfsOffX.png)

注意：如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。

### 步骤 2

在`on start`中插入`initialize OLED`积木块，参数填入`64*128`。

初始化OLED屏幕为`64`像素*`128`像素。

![](./images/RmoYl5S.png)

### 步骤 2

在`forever`中依次插入`show string`积木块，`show number`积木块。

显示当前光线值，温度以及湿度值。

插入`insert newline`积木块，另起一行。

![](./images/r34zWZ5.png)

### 程序

请参考程序连接：[https://makecode.microbit.org/_gXa1mXargW1V](https://makecode.microbit.org/_gXa1mXargW1V)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_gXa1mXargW1V" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  


### 现象
---

每分钟显示当前环境的光线值、温度值、湿度值。

## 思考
---

如何统计一天内的数据。

## 常见问题
---

## 相关阅读  
---
