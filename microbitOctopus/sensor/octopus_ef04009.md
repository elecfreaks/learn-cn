# 红外接收传感器

## 简介
这是一种简单的红外接收传感器，主要通过HS0038红外二极管接收红外信号。HS0038对红外信号特别敏感，接收红外信号非常迅速。可用于红外遥控，红外发射器工作。
![](./images/04009_01.png)
## 特性
---
- 三线端口设计，防止误插，易于使用。
## 技术规格
---

项目 | 参数 
:-: | :-: 
SKU|EF04009
引脚定义|S-Sigal V-VCC G-GND
工作电压|3V
产品尺寸|38.9 x 23.5 mm


尺寸：

## 外形与定位尺寸
---


![](./images/04009_02.png)


## 快速上手
---

### 所需器材及连接示意图
---

- 如下图所示，将红外接收传感器连接到扩展板的P1端口。

***以sensor：bit为例***



![](./images/04009_03.png)

## 编程
---

### 步骤 1
在MakeCode的代码抽屉中点击“高级”，查看更多代码选项。

![](./images/04009_04.png)

为了给红外接收传感器编程，我们需要添加一个扩展库。在代码抽屉底部找到“扩展”，并点击它。这时会弹出一个对话框，搜索”ir-receiver“，然后点击下载这个代码库。

![](./images/04009_05.png)

*注意：*如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。
### 步骤 2
### 如图所示编写程序

![](./images/04009_06.png)


### 参考程序
请参考程序连接：[https://makecode.microbit.org/_FUzeJvaord75](https://makecode.microbit.org/_FUzeJvaord75)

你也可以通过以下网页直接下载程序，下载完成后即可开始运行程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_FUzeJvaord75" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

### 结果
- 按下遥控器的开关按钮，则显示笑脸，按下遥控器的四个方向键，则micro:bit主板上则显示对应的箭头图标。
## 相关案例
---

## 技术文档
---
