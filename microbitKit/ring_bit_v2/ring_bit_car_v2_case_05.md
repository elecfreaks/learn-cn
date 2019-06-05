# 案例05 疯狂舞蹈

## 目的
---
- 让Ring:bit智能车随心起舞。

## 使用材料
---
- 1 x Ring:bit Car 套件

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

- 在`On start`积木块中插入设置左右轮舵机连接口积木块。
- 端口号以实际舵机连接端口为准。
![](./images/igG5TVD.png)

### 步骤 3
- 在`forever`(永久循环)积木块中插入。
- 设置一个`left`变量和一个`right`变量。
- 随机生成一个数字赋值给`left`变量和`right`变量。

![](./images/2PPYJ0T.png)

### 步骤 4

- 再插入设置左右轮速度为左右变量的积木块。
- 暂停1秒。

![](./images/HSujBjF.png)


### 程序

请参考程序连接：[https://makecode.microbit.org/_PXXfa8FF5MWs](https://makecode.microbit.org/_PXXfa8FF5MWs)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_PXXfa8FF5MWs" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---


## 结论
---
- 上电之后，小车开始随机前后左右不同速度行驶。

![](./images/j6kX56N.jpg)

## 思考
---
- 将小车随机行驶的速度控制在很低的速度，如何编程？

## 常见问题
---


## 相关阅读  
---

