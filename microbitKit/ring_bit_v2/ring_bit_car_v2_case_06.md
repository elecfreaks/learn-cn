# 案例06 远程控制

## 目的
---
- 使用另一块micro:bit远程遥控Ring:bit智能车。

## 使用材料
---
- 1 x Ring:bit Car 套件
- 1 x micro:bit主板

## 背景知识 ##
### 什么是无线电 
---
- 无线电无线电技术是通过无线电波传播信号的技术，其原理在于，导体中电流强弱的改变会产生无线电波。利用这一现象，通过调制可将信息加载于无线电波之上。当电波通过空间传播到达收信端，电波引起的电磁场变化又会在导体中产生电流。通过解调将讯息从电流变化中提取出来，就达到了资讯传递的目的。


## 硬件连接图
---
- Ring:bit扩展版的P1口连接左轮舵机，P2口连接右轮舵机。
![](./images/jBVHea8.png)

## 软件平台
---
[微软makecode](https://makecode.microbit.org/#)在线积木块编程[https://makecode.microbit.org/#](https://makecode.microbit.org/#)

## 编程
---
### 步骤 1
- 在MakeCode的代码抽屉中点击Advanced，查看更多代码选项。

![](./images/2qCyzQ7.png)

- 为了给Ring:bit套件编程，我们需要添加一个代码库。在代码抽屉底部找到“Add Package”，并点击它。这时会弹出一个对话框。搜索“ringbit"，然后点击下载这个代码库。

![](./images/1Wq2Mov.jpg)

注意：如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。

### 遥控器端程序
请参考程序连接：[https://makecode.microbit.org/_46FfwWDJwiyy](https://makecode.microbit.org/_46FfwWDJwiyy)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_46FfwWDJwiyy" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

### Ring:bit 小车端程序 ###
请参考程序连接：[https://makecode.microbit.org/_4aWeti12K4HR](https://makecode.microbit.org/_4aWeti12K4HR)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_4aWeti12K4HR" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---


## 结论
---
- 按按钮A，小车左转，按按钮B小车右转，按钮A、B同时按下，小车前进，摇晃micro:bit主板，小车后退。


## 思考
---
- 如何远程遥控小车行驶速度，如何编程？

## 常见问题
---


## 相关阅读  
---

