# 案例01 全速行驶

## 目的
---
- 让Ring:bit智能车完成最基本的前进后退。

## 使用材料
---
- [Ring:bit Car 套件（淘宝购买链接）](https://item.taobao.com/item.htm?ft=t&id=564916883947)


## 硬件连接图
---
- Ring:bit扩展版的P1口连接左轮舵机，P2口连接右轮舵机。

![](./images/jBVHea8.png)

## 软件平台
---
[微软 makecode](https://makecode.microbit.org/#)

## 编程
---
### 步骤 1
- 在MakeCode的代码抽屉中点击Advanced，查看更多代码选项。

![](./images/2qCyzQ7.png)

- 为了给Ring:bit套件编程，我们需要添加一个代码库。在代码抽屉底部找到“Add Package”，并点击它。这时会弹出一个对话框。搜索“ringbit"，然后点击下载这个代码库。

![](./images/1Wq2Mov.jpg)

注意：如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。

### 步骤 2

- 在`On start`(开始)积木块中插入设置左右轮舵机连接口积木块。
- 端口号以实际舵机连接端口为准。

![](./images/ring_bit_car_v2_case_01_01.png)

### 步骤 3

- 在`on button A pressed`(当按钮A按下时)积木块中插入`go straight at full speed`(全速前进)积木块。


![](./images/ring_bit_car_v2_case_01_02.png)


### 步骤 4

- 在`on button B pressed`(当按钮B按下时)积木块中插入`reverse at full speed`(全速倒退)积木块。


![](./images/ring_bit_car_v2_case_01_03.png)

### 程序

请参考程序连接：[https://makecode.microbit.org/_WC016LTP5a9s](https://makecode.microbit.org/_WC016LTP5a9s)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_WC016LTP5a9s" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---


## 结论
---
- 当按钮A按下时，小车全速前进。
- 当按钮B按下时，小车全速后退。
![](./images/wwV0YDe.jpg)

## 思考
---
当你按下按钮A，让小车停下，如何编写代码？

## 常见问题
---


## 相关阅读  
---

