# 案例02 画一个形状

## 目的
---
- 让Ring:bit智能车按一个角度旋转。

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

- 在On start积木块中插入设置左右轮舵机连接口积木块。
- 端口号以实际舵机连接端口为准。
![](./images/igG5TVD.png)

### 步骤 3

- 在`forever`(永久循环)积木块中依次插入：
- `go straight at full speed`(全速前进)积木块
- `pause`(暂停)积木块
- `turn right at full speed`(全速向右转)积木块
- `pause`(暂停)积木块

![](./images/FRnGCpw.png)


### 程序

请参考程序连接：[https://makecode.microbit.org/_5md9ofDyRigh](https://makecode.microbit.org/_5md9ofDyRigh)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:__5md9ofDyRigh" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---


## 结论
---
- 小车向前走，然后向右旋转一个角度，继续向前走。


![](./images/srKhgfm.jpg)

## 思考
---
- 让你的小车舞蹈起来，如何编程？

## 常见问题
---


## 相关阅读  
---

