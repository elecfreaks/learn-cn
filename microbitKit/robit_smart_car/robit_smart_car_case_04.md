# robit智能小车案例04：自动车灯

## 目的
---
- 使用Robit主板上的光线传感器模块和LED模块制作智能车灯。

## 使用材料
---

- 1 x Robit智能小车主板
- 1 x Mbot Car

## 背景知识
### 光线传感器
---
[光传感器](https://baike.baidu.com/item/%E5%85%89%E4%BC%A0%E6%84%9F%E5%99%A8/2054816)通常是指能敏感由紫外光到红外光的光能量，并将光能量转换成电信号的器件,主要由光敏元件组成，主要分为环境光传感器、红外光传感器、太阳光传感器、紫外光传感器四类，主要应用在改变车身电子应用和智能照明系统等领域。

Robit主板上的光线传感器为<u>环境光传感器</u>，以数字大小的方式表示环境光的强弱。


## 硬件连接图
---
板载光线传感器，连接在micro:bit的P10口。

![](./images/OTB2gfJ.png)

板载两颗彩虹LED，连接在micro:bit的P12口。

![](./images/yOJCtFk.png)
## 软件
---
[微软makecode](https://makecode.microbit.org/#)

## 编程
---
### 步骤 1
在MakeCode的代码抽屉中点击Advanced，查看更多代码选项。

![](./images/LjMR5IU.png)

为了给Robit编程，我们需要添加一个代码库。在代码抽屉底部找到“Add Package”，并点击它。这时会弹出一个对话框。搜索“Robit"，然后点击下载这个代码库。

![](./images/ISZ6w26.png)

注意：如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。

### 步骤 2

创建一个永久循环，以模拟方式读取P10引脚，也就是光线传感器的引脚，读取光线强度值，赋值给item变量。

![](./images/HSAjMjm.png)

如果item变量，也就是光强度小于700，点亮LED灯为白色，并且延迟3000ms。

![](./images/FpjcKWz.png)

如果item大于700，LED灯熄灭。

![](./images/PWwcz3X.png)

**注意：** 下图为LED代码详解

![](./images/mPEbbU7.png)

### 程序
请参考程序连接：[https://makecode.microbit.org/_Dyu4j2A4F23c](https://makecode.microbit.org/_Dyu4j2A4F23c)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_Dyu4j2A4F23c" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

### 现象
当环境光很强，LED灯熄灭；当环境光很暗，LED点亮。

![](./images/s9qiUGU.jpg)

![](./images/27DbgCx.jpg)

## 思考
---

## 常见问题
---


## 相关阅读  
---

