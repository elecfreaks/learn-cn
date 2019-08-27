# gun kit套件案例01：打蜘蛛

## 目的
---

- 使用gun_kit手枪套件制作一把可以将蜘蛛打翻的手枪

## 使用材料
---

## 背景知识
---

## 软件
---

[微软makecode](https://makecode.microbit.org/#)

## 编程
---

### 步骤 1
 在MakeCode的代码抽屉中点击“高级”，查看更多代码选项。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/gun_kit/images/gun_kit_case_01_02.png)

为了给gun_kit手枪套件编程，我们需要添加一个扩展库。在代码抽屉底部找到“扩展”，并点击它。这时会弹出一个对话框，搜索”Toy Gun Kit”(因为目前这个库还在审核中，在正式上架之前先通过这个链接搜索"github.com/elecfreaks/pxt-microbit-toy-gun“)，然后点击下载这个代码库。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/gun_kit/images/gun_kit_case_01_03.png)

*注意：*如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。

### 步骤 2

在`当开机时`中依次插入`设置红外发射连接接口`积木块，设置为`P1`口。`设置扳机连接口`积木块，设置为`P8`口。`设置子弹类型`积木块，并选择参数`手枪子弹`。



![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/gun_kit/images/gun_kit_case_01_04.png)


### 步骤 3

如图所示，在`无限循环`中插入`如果为...则...`积木块，`扳机按下`积木块，`开火`积木块。



![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/gun_kit/images/gun_kit_case_01_05.png)

### 程序

请参考程序连接：[https://makecode.microbit.org/_cwJ97i2z1RaA](https://makecode.microbit.org/_cwJ97i2z1RaA)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_cwJ97i2z1RaA]" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  

### 现象

按下射击键则发射子弹，当子弹击中快速移动中的蜘蛛时，蜘蛛被打翻并停止动作。

## 思考
---
如何在射击时发出声音。

## 常见问题
---
## 相关阅读  
---
