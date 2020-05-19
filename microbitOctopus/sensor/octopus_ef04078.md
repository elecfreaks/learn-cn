# 手势识别电子积木

## 简介
---
OCTOPUS手势传感器是PAJ7620U2，它将手势识别功能与通用I2C接口集成到一个芯片中。 它可以识别9个手势，包括向上移动、向下移动、向左移动、向右移动等，只需轻轻一挥你的手即可轻轻滑动等等。

 ![](./images/AVBdYeR.jpg)

## 特性
---

- 三线端口设计，防止误插，易于使用。

## 技术规格
---

项目 | 参数 
:-: | :-: 
SKU|EF04078
检测位|内置接近检测
手势|9基本手势(上/下/右/左/前进/后退/顺时针/逆时针/波计数）
检测范围|5-10cm
环境光免疫力|100k
电源|5V
工作温度|-20℃~70℃
尺寸|23.48mm×31.28mm

## 外形与定位尺寸
---

 ![](./images/FW7bmzW.png)

## 快速上手
---
### 所需器材及连接示意图


***以sensor:bit为例***

![](./images/ef04078_08.jpg)

### 添加Package
在MakeCode的代码抽屉中点击Advanced，查看更多代码选项。

![](./images/smtcNoB.png)

点击“Extensions”，在弹出的对话框中搜索“https://github.com/elecfreaks/pxt-gesture”，下载手势识别传感器代码库。
![](./images/ef04078_05.png)

### 如图所示编写程序

![](./images/ef04078_06.png)

### 参考程序
请参考程序连接：[https://makecode.microbit.org/_Dry9Rm7xpi2A](https://makecode.microbit.org/_Dry9Rm7xpi2A)

你也可以通过以下网页直接下载程序，下载完成后即可开始运行程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_Dry9Rm7xpi2A" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

### 结果
- 随着手势动作的不一样，micro:bit点阵屏上显示出不同方向的箭头。



![](./images/ef04078_07.gif)

## 相关案例
---

## 技术文档
---
