# 案例05：多功能手电筒

## 目的
---
- 使用watch kit手表套件完成可穿戴便携式多功能手电筒。

## 使用材料
---

- 1 x Watch kit 手表套件


## 硬件连接图
---

如图所示，将灯环连接到power bit主板上。

![](./images/xLUYTkT.jpg)



## 软件
---
[微软makecode](https://makecode.microbit.org/#)

## 编程
---
### 步骤 1
- 在MakeCode的代码抽屉中点击Advanced，查看更多代码选项。

![](./images/LjMR5IU.png)

- 为了给灯环模块编程，我们需要添加一个代码库。在代码抽屉底部找到“Add Package”，并点击它。这时会弹出一个对话框。搜索“nexpixel"，然后点击下载这个代码库。

![](./images/0u6UbMV.png)

注意：如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。

### 步骤 2

- 上电开机时将功能标签`flag`设置为 0 。
- 当按钮 A 按下时，设置功能标签为 1 。
- 当按钮 B 按下时，设置功能标签为 2 。
- 当按钮A+B同时按下时，设置功能标签为 0 。

![](./images/n6EOHiO.png)

### 步骤 3

- 设置一个永久循环，循环判断功能标签。
- 当功能标签为 1 时，调用函数`light`(亮3颗灯)，当功能标签为 1 同时按钮 A 按下，调用函数`light_02`(全亮)。
- 当功能标签为 2 时，调用函数`police`(模拟警灯)。
- 当功能标签为 0 是，调用函数`true off`，关灯。


![](./images/shL403s.png)


### 步骤 4

- `light`功能函数体，8颗灯连接到P2口，点亮从第三颗往后3颗灯，显示颜色为白色。

![](./images/fUgwYDa.png)

- `light_02`功能函数体。点亮8颗灯。


![](./images/v0v7crG.png)

- `police`功能函数体，0到4显示蓝色延时0.1秒，4到8显示红色延迟0.1秒。

![](./images/8Wujurq.png)

- `true off`功能函数体，将8个灯都熄灭。

![](./images/MTjecwh.png)


### 程序
- 请参考程序连接：[https://makecode.microbit.org/_goJVKXdyqVRX](https://makecode.microbit.org/_goJVKXdyqVRX)

- 你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_goJVKXdyqVRX" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---


## 结论
---

按下A按钮亮灯，按住A按钮全亮，按下B按钮闪烁警灯，按下A+B关闭。

![](./images/Uiksjgk.gif)



## 思考
---


## 常见问题
---
问：为什么代码选择白色，看起来是黄色。

答：因为便携式主板电池供电不足，电流无法驱动。

## 相关阅读  
---

