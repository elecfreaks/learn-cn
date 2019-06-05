# 案例07 灯光寻路

## 目的
---

- 让Ring:bit智能车完成自动寻找光源的功能。

## 使用材料
---

- 1 x Ring:bit Car 套件


## 硬件连接图
---
- Ring:bit扩展版的P1口连接左轮舵机（即图中右下角的P1,3.3v，GND），P2口连接右轮舵机（即图中左上角的P2，3.3V，GND），将选择开关拨到P2的位置。
![](./images/MT6Y00d.png)

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
---
- 从Basic中拖出一个`on start`积木块，初始化ring:bit扩展板的P1，P2口分别对应小车左右轮胎。

![](./images/RFccHpJ.png)

### 步骤 3
---
- 从input函数库中，拖入获取光线强度的函数`light level`，当强度大于设定的界定值，小车径直朝光源处行驶。
- 当不强度值不足的时候，小车在原地旋转，寻找光源。
![](./images/i1lAR3X.png)




### 程序

请参考程序连接：[https://makecode.microbit.org/_K3J3EhLamU80](https://makecode.microbit.org/_K3J3EhLamU80)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_K3J3EhLamU80" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

## 结论
---

- 小车原地旋转寻找光源，当光源出现，小车径直向光源驶去。

![](./images/e1PY6hc.gif)

## 思考
---

- 家庭火源不注意防卫就会造成可怕的后果，制作一个能自动逃离火源的自卫小车？

## 常见问题
---


## 相关阅读  
---

