# iot:bit物联网扩展版

## 简介
---

- Iot:bit是一款micro:bit物联网科学实验扩展版，支持3pin接口的传感器，执行机构和蜂鸣器，板载了RTC时钟模块，即使主板断电，也会精准计时。

- IoT:bit是一款基于micro:bit的物联网micro:bit扩展板，它使用ESP8266为WIFI扩展模块，使用串口与micro:bit通信，同时扩展了micro:bit上所有可用的IO口，以GVS形式引出，通过它能扩展各种3V的电子积木模块，如LED灯、光敏、舵机等。并且板载了蜂鸣器能够播放外音。板载RTC时钟，断电也可以继续计时。使用makecode编程扩展专属代码库，可以方便接入thingspeak，快速搭建物联网智能设备。

 ![](./images/NGKCsKq.jpg)

### 特性
---

- 集成了ESP12F WiFi、RTC、无源蜂鸣模块。
- 以GVS端子形式扩展出大部分IO口。
- 丝印注明板载主要元件。
- 单独引出IIC接口，能直接插入OLED、BME280等IIC器件。
- 集成蜂鸣器和耳机接口。
- 兼容乐高：4个标准间距的乐高固定孔。

## 硬件外观及参数
---

### 外形与安装定位尺寸
---

- 产品尺寸：71mm x 63mm x 23mm
- PCB板厚：1.5mm
- 开孔直径：2.4mm

 ![](./images/5CDXW5R.png)

### 参数
---

 |项目|参数|备注|
 |:-:|:-:|:-:|
 |直流供电电源|USB-5V|-|
 |最大工作电流|800mA|-|
 |工作温度|-25~80℃|-|
 |WIFI模块|ESP8266|ESP12F|
 |蜂鸣器|无源蜂鸣器|-|
 |RTC时钟|DS1307 RTC|-|
 |RTC时钟电池|CR1220 纽扣电池|需自行配备|
 |引脚引出|非全|-|
 |串口引出|串口可对IO口进行映射|软件编程实现|
 |I2C口引出|19、20引脚|只能作为I2C功能引脚使用|
 |SPI口引出|14、15引脚|可做普通IO使用|
 |尺寸|71.00mm X 63.00mm|不含包装|
 |净重|30.00g|不含包装|

### 引脚接口框图
---

![](./images/3Pb4vCV.png)

### 主体模块介绍
---

 ![](./images/bkO3DMr.png)

## 软件支持
---

- 编程方式：Makecode/Micropython/JavaScript/

### Makecode积木块
---

- Microsoft出品micro:bit官方推荐使用编程方式。

- https://makecode.microbit.org

 ![](./images/LczawXh.png)

### JavaScript代码编程
---

- 在`makecode`界面中点击`JavaScript`可以进行`JavaScript`编程。

- https://makecode.microbit.org

 ![](./images/X7zJlwA.png)

### MicroPython代码编程
---

- 进阶编程方式`MicroPython`官方推荐使用`MU`软件

- https://codewith.mu/

 ![](./images/CJytOdT.png)


## 快速上手  
---
### 硬件安装及连接

- 首先安装CR1220纽扣电池为RTC时钟模块供电,

 ![](./images/EkM7aP2.gif)

- 然后把Microbit插到Iot:bit上，注意插接方向

 ![](./images/kFW4hB9.gif)

- 最后使用独立USB电源为扩展板供电，打开板载电源开关。 

 ![](./images/DXB3mBI.gif)

### 软件编程  
---
#### 软件编程平台 ###
---

- makecode积木块在线编程：https://makecode.microbit.org


#### 添加代码库 ###
---

- 在MakeCode的代码抽屉中点击Advanced，查看更多代码选项。

 ![](./images/j31P9Bx.jpg)

- 为了给IoT物联网环境科学套件编程，我们需要添加一个扩展库。在代码抽屉底部找到“Extension”，并点击它。这时会弹出一个对话框。搜索“IOT"，然后点击下载这个代码库。

 ![](./images/AaZxCEb.jpg)

**注意：**如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。


#### 如何驱动蜂鸣器 ###
---

- IoT:bit板载一颗蜂鸣器，位置如图上所示，连接到micro:bit主板的P0口，可以直接用makecode积木块中`music`编程播放音乐。

 ![](./images/zBNYZsy.png) ![](./images/lNibSJk.png)

- 在input函数库中选择当按钮A按下时。编写一小段音乐。

 ![](./images/cPG4w9y.png)

- 程序代码链接：[https://makecode.microbit.org/_4j6PCeV087AW](https://makecode.microbit.org/_4j6PCeV087AW)


#### 如何使用RTC时钟 ###
---

- IoT:bit板载DS1307RTC时钟模块，位置如上图所示，RTC时钟需要一颗CR1220纽扣电池持续供电，这样当IOT:bit断电时，RTC时钟模块也持续工作保证时间正确。

 ![](./images/Y76pQRh.jpg) ![](./images/ivqmwe3.png)

---

- 按下按钮A，将时间设置为设定时间。开机时开始RTC时钟模块功能，循环在点阵显示屏上显示分钟。

- 将电源关闭一分钟后再打开电源，点阵显示屏会显示增加１分钟后的分钟数。

 ![](./images/t9fOHMT.png)

- 程序代码链接：[https://makecode.microbit.org/_e9d3vW96bPe2](https://makecode.microbit.org/_e9d3vW96bPe2)

#### 如何使用物联网功能功能 ###
---

- IoT:bit最重要的功能为WIFI功能，板载`ESP-12F`WIFI模块，可以连接WIFI，发送数据，使用串口与micro:bit主板通信，板载默认连接引脚`RX-P8`，`TX-P12`。物联网使用
- 使用thingspeak平台作为物联网云端，可以编写代码一键上传数据。thingspeak平台使用指南

 ![](./images/CbzmpB1.jpg) ![](./images/fLnI2rl.png)

- 当开机时初始化ESP8266默认连接到P8和P12端口。
- 然后连接自己的WiFi，写入账号和密码。
- 在永久循环中，连接thinkspeak平台，设置要发送的数据，然后发送数据，暂停一会。

 ![](./images/03PNnhW.png)

- 程序代码链接：[https://makecode.microbit.org/_JAXAmmHq4FhW](https://makecode.microbit.org/_JAXAmmHq4FhW)

#### 其他传感器支持库 ###
---

- IoT:bit同样支持elecfreaks出品的各种传感器，为了方便使用，扩展包里新增了Octopus积木块。

 ![](./images/hQwlIOW.png)

### 下载代码 ###
---
- 首先将micro:bit单独连接USB线，另一端连接到电脑。（如果插在扩展板上可能会导致micro:bit连接不正常或者损坏）

![](./images/DfE3smq.jpg)

- 将下载好的文件，点击鼠标右键发送到micro:bit盘，或者复制黏贴micro:bit盘。

![](./images/lIRbv15.jpg)

![](./images/JsGZrPa.png)

- 即可观察程序结果。

![](./images/YEGtIO7.jpg)

### 文档
---


### 常见问题
---
