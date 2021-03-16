# 加速度计算法

- Ring:bit小车加速度计陀螺仪算法。

## 使用材料
---

- 1 x Micro:bit
- 1 x Ring:bit Car二代

## 背景知识
---

- [Micro:bit](http://microbit.org/)是一个小型的可编程计算机，由英国广播电视公司（BBC）推出，专为青少年编程教育，设计旨在使学习与教学变得轻松有趣。

- ELECFREAKS Ring:bit二代智能车是一款小型DIY智能车，由BBC micro:bit和ELECFREAKS Ring:bit组成。Ring:bit扩展了micro:bit的三个GPIO口，可以连接轻松的连接各种传感器和组件。一个基础的Ring:bit智能车可以很容易的编程去驱动，还可以搭配遥控器甚至创建一个彩虹灯塔。只要增加一个扩展模块，你的Ring:bit智能车就可以做更多事情，例如巡线，跟随，避障，绘图和更多玩法。

- [无线电无线电技术](https://baike.baidu.com/item/%E6%97%A0%E7%BA%BF%E7%94%B5/3979?fr=aladdin)是通过无线电波传播信号的技术，其原理在于，导体中电流强弱的改变会产生无线电波。利用这一现象，通过调制可将信息加载于无线电波之上。当电波通过空间传播到达收信端，电波引起的电磁场变化又会在导体中产生电流。通过解调将讯息从电流变化中提取出来，就达到了资讯传递的目的。

- [加速度传感器](https://baike.baidu.com/item/%E5%8A%A0%E9%80%9F%E5%BA%A6%E4%BC%A0%E6%84%9F%E5%99%A8/8719004)是一种能够测量加速度的传感器。通常由质量块、阻尼器、弹性元件、敏感元件和适调电路等部分组成。传感器在加速过程中，通过对质量块所受惯性力的测量，利用牛顿第二定律获得加速度值。根据传感器敏感元件的不同，常见的加速度传感器包括电容式、电感式、应变式、压阻式、压电式等。

 *新版和旧版micro:bit加速度计芯片有所区别。新版micro:bit将电子罗盘和加速度计合并为一个芯片，使用方法不变。*

 ![](./images/2n6TbVZ.png)  ![](./images/F0frwo6.jpg)


## 软件准备
---

[微软makecode](https://makecode.microbit.org/#)在线积木块编程[https://makecode.microbit.org/#](https://makecode.microbit.org/#)

 ![](./images/cp88kPs.png)

## 程序
---
### 步骤 1：添加代码包
- 在MakeCode的代码抽屉中点击Advanced，查看更多代码选项。

![](./images/2qCyzQ7.png)

- 为了给Ring:bit套件编程，我们需要添加一个代码库。在代码抽屉底部找到“Add Package”，并点击它。这时会弹出一个对话框。搜索“ringbit"，然后点击下载这个代码库。

![](./images/1Wq2Mov.jpg)

注意：如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。

### 步骤 2：算法原理

- 加速度计分为X轴和Y轴两个方向，在俯视图上，将micro:bit和Ring:bit Car放在同一个三维坐标轴中就很好理解。
![](./images/4jVn6rG.jpg)

 以控制端micro:bit的方向来同步控制Ring:bit小车的行驶方向及速度。

![](./images/NGnp5Ya.jpg)

- 向右前方行驶，X轴和Y轴数据均为正数，左轮速度应大于右轮速度，依次完成左转。
- 同理左前方，左后方，右后方均如此分析。
- 得出结论为：左轮数据为Y轴数据加上X轴数据，右轮数据位Y轴数据减去X轴数据。

![](./images/8oOCEWj.png)

### 步骤 3：代码解释(控制端) ###
---

![](./images/xxvSu1T.png)

- 在开机的时候设置无线电组别为`90`,需要和接收端(小车)设置为一致。
- 循环发送数据X，值为X轴加速度值。加速度值范围为`-1024~+1024`，而小车转速为`-100~+100`，故需要除以`10`以符合范围。
- 循环发送数据Y，值为Y轴加速度值，同理除以`10`。

### 步骤 4：代码解释(小车端)
---

![](./images/JsLkJ1t.png)

- 开机的时候，设置小车左右轮连接为P1和P2(以小车实际连接端口为准)，显示一个图标，设置无线电组别为90(与发送端一致)，用来设置XValue和yValue两个变量存储X轴数据和Y轴数据。

![](./images/A5gqKjZ.png)

- 当接收到无线电数据时，判断如果为X值，将数据存入`xValue`，如果为y值，将数据存入`yValue`。

![](./images/a3uTwmH.png)

- 将上边得出的公式带入，算出左右轮速度值，将左右轮速度设置为相应值。


## 参考程序 ##
### 遥控器端程序
请参考程序连接：[https://makecode.microbit.org/_AT4PoHKdVi6L](https://makecode.microbit.org/_AT4PoHKdVi6L)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_AT4PoHKdVi6L" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

### Ring:bit 小车端程序 ###
请参考程序连接：[https://makecode.microbit.org/_e5t6XPHoTiHy](https://makecode.microbit.org/_e5t6XPHoTiHy)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_e5t6XPHoTiHy" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---


## 结论
---
- Ring:bit小车随着陀螺仪的方向行驶，陀螺仪倾斜角度控制行车速度。
