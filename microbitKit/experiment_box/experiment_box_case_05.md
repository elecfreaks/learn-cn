# 软件编程案例05：光敏传感器

## 简介 ##
---
- 光敏二极管，是一种能够将光根据使用方式，利用光照强弱来改变电路中的电流。本次实验，我们通过光敏二极管来控制micro:bit 5x5LED屏幕的亮度。

## 硬件连线图 ##
---
![](./images/YlThssw.png)

- 使用香蕉线按如上图连接电路，电池盒内放入2颗7号AAA电池。

## 电路原理图 ##
---
![](./images/Baf6k1C.png)

- micro:bit插槽的GND端和电池GND相连内部，形成电流回路。

## 主要元件介绍 ##
---
### 光敏二极管 ###
- 光敏二极管，又叫光电二极管（英语：photodiode ）是一种能够将光根据使用方式，转换成电流或者电压信号的光探测器。管芯常使用一个具有光敏特征的PN结，对光的变化非常敏感，具有单向导电性，而且光强不同的时候会改变电学特性，因此，可以利用光照强弱来改变电路中的电流。
- 在实验箱板子上我们配备了1颗光敏二极管。左边黑色端口为负极，右边红色端口为正极。

![](./images/E1kmQUI.jpg)

*- 连线时注意正负极。*

## 软件编程设计
---
### 步骤 1

- 点击打开[微软makecode在线积木块编程https://makecode.microbit.org/#](https://makecode.microbit.org/#)。

- 点击New Project按钮，新建一个项目。

![](./images/t34k5Zb.png)

### 步骤 2

- 在forever积木块中插入判断模拟读取P0口的值是否大于100积木。
- 当值大于100时（光线足够亮）。
- 清空屏幕。

![](./images/Ll1nPCC.png)

### 步骤 3

- 当值不大于100时（光线很暗）。
- micro:bit 5X5 点阵显示屏显示一颗心。

![](./images/5WMWzWe.png)

### 程序

- 请参考程序连接：[https://makecode.microbit.org/_1f0Kjdgk7dVc](https://makecode.microbit.org/_1f0Kjdgk7dVc)

- 你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_1f0Kjdgk7dVc" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---


## 结论
---
- 亮光不显示，光线变暗显示一颗心。


## 思考
---


## 常见问题
---


## 相关阅读  
---

