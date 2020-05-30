# 手势识别传感器

## 简介
手势识别传感器可以识别9个手势，包括向上移动、向下移动、向左移动、向右移动等，可用于非接触式控制场景如非接触式鼠标，智能家居，汽车点击设备控制，机器人交互等

![](./images/05020_01.png)

## 特性
---
- RJ11端口设计，防止误插，易于使用。
## 技术规格
---

项目 | 参数 
:-: | :-: 
SKU|EF05020
接口|RJ11
接口类型|IIC
工作电压|3.3V
核心IC|PAJ7620U2
手势类型|基本手势(上、下、右、左、前进、后退、顺时针、逆时针等)



尺寸：

## 外形与定位尺寸
---


![](./images/05020_02.png)


## 快速上手
---

### 所需器材及连接示意图
---

- 如下图所示，将手势识别传感器连接到哪吒扩展板的IIC端口。


![](./images/05020_03.png)

## 编程
---

### 步骤 1
在MakeCode的代码抽屉中点击“高级”，查看更多代码选项。

![](./images/05001_04.png)

为了给手势识别传感器编程，我们需要添加一个扩展库。在代码抽屉底部找到“扩展”，并点击它。这时会弹出一个对话框，搜索”https://github.com/elecfreaks/pxt-PlanetX“，然后点击下载这个代码库。

![](./images/05001_05.png)

*注意：*如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。
### 步骤 2
### 如图所示编写程序

![](./images/05020_06.png)


### 参考程序
请参考程序连接：[https://makecode.microbit.org/_gqVLAwesWAcU](https://makecode.microbit.org/_gqVLAwesWAcU)

你也可以通过以下网页直接下载程序，下载完成后即可开始运行程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_gqVLAwesWAcU" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

### 结果
- 根据手势识别传感器检测到的动作，在micro:bit上显示相应的图标。
## 相关案例
---

## 技术文档
---
