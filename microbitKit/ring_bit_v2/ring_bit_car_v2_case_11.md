# 案例11 游戏手柄控制小车行驶



## 目的
---

- 通过手柄控制Ring:bit.小车行驶 




## 使用材料
---

Ring:bit套件 × 1

游戏手柄 × 1










## 软件
---

[MicroSoft makecode](https://makecode.microbit.org/#)

## 编程

---

### 步骤 1

在MakeCode的代码抽屉中点击“高级”，查看更多代码选项。



![](./images/2qCyzQ7.png)




### 步骤 2    小车编程


为了给Ring:bit套件编程，我们需要添加一个扩展库。在代码抽屉底部找到“扩展”，并点击它。这时会弹出一个对话框，搜索”Ringbit”，然后点击下载这个代码库。




![](./images/1Wq2Mov.jpg)




*注意：*如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。



在当开机时(开始)积木块中设置无线电组别为1，一定要和遥控端设置为同一组别，否则无法匹配。

然后在当接收到数据积木块中插入两次判断语句，分别判断无线电接收值name是否为x或者y；

当无线电收到的name值为x时，为加速度计X轴数据，将value值保存到xValue变量；

当无线电收到的name值为y时，为加速度计Y轴数据，将value值保存到yValue变量；

在无限循环积木块中，设置左轮速度为yValue+xValue，右轮速度为yValue-xValue。



![](./image/Ringbit_Bricks_Pack_case_cn_07_05.png)

### 程序

请参考程序连接： [https://makecode.microbit.org/_1vAgLo3Ky5Rm](https://makecode.microbit.org/_1vAgLo3Ky5Rm)


你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_1vAgLo3Ky5Rm]" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  



### 步骤 3    游戏手柄编程

为了给游戏手柄编程，我们需要添加一个扩展库。在代码抽屉底部找到“扩展”，并点击它。这时会弹出一个对话框，搜索”joystickbit”，然后点击下载这个代码库。




![](./image/Ringbit_Bricks_Pack_case_cn_07_06.png)




*注意：*如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。

在当开机时积木块中设置无线电组别为1；

X轴和Y轴的数值范围为0~1023，当摇杆位置在中心的时候，它的理论值为512，故需要将0~1023map映射到-100~100这个范围之内。

在无限循环积木块中设置变量x它的值为X轴的读值映射到-100~100这个范围的值。

在无限循环积木块中设置变量y它的值为y轴的读值映射到100~-100这个范围的值。

通过无线发送值将变量x和变量y发送出去。



![](./image/Ringbit_Bricks_Pack_case_cn_07_07.png)




### 程序

请参考程序连接：[https://makecode.microbit.org/_Ct3UpWKx3eb0](https://makecode.microbit.org/_Ct3UpWKx3eb0)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_Ct3UpWKx3eb0]" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
### Result
---
用手柄摇杆可以控制小车前进后退转弯速度等。


## Exploration
---

## FAQ
---
## Relevant File
---
