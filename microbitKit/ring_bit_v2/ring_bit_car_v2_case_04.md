# 案例04 警察来了

## 目的
---
- 让Ring:bit智能车化身警车。

## 使用材料
---
- 1 x Ring:bit Car 套件

## 硬件连接图
---
- Ring:bit扩展版的P1口连接左轮舵机，P2口连接右轮舵机。
- P0口连接ring:bit Car专用扩展板。
![](./images/D5sFydb.jpg)

- 将专用扩展板上的拨片开关，拨到Rainbow LED。

![](./images/s3rVwxZ.jpg)

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

- 在`On start`积木块中插入设置左右轮舵机连接口积木块，端口号以实际舵机连接端口为准。
- 全速向前行驶。
- 设置连接到`P0`口的`2`颗Rainbow LED为`RGB`色彩。

![](./images/J7eFoDN.png)

### 步骤 3

- 在`forever`(永久循环)积木块中依次插入
- `show color red`(显示红色)积木块。
- `pause(ms) 100`(暂停100ms)积木块
- `show color blue`(显示红色)积木块。
- `pause(ms) 100`(暂停100ms)积木块

![](./images/CqsUljq.png)


### 程序

请参考程序连接：[https://makecode.microbit.org/_AvMC6j86A5ym](https://makecode.microbit.org/_AvMC6j86A5ym)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_AvMC6j86A5ym" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---


## 结论
---
- 小车闪亮红蓝警灯全速前进。

![](./images/E4XxlGK.jpg)

## 思考
---
- 让你的小车闪亮黄白急救警灯，如何编写代码？

## 常见问题
---


## 相关阅读  
---

