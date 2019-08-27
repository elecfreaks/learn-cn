# gun kit套件案例01：打蜘蛛

## 目的
---

- 使用gun_kit手枪套件制作一把可以控制飞碟飞行的枪。

## 使用材料
---

- 1 x [GUN:kit(手枪套件):https://www.elecfreaks.com/store](https://www.elecfreaks.com/store/micro-bit-smart-science-iot-kit-with-micro-bit.html)

## 背景知识
---
## 硬件连接图
---


## 软件
---

[微软makecode](https://makecode.microbit.org/#)

## 编程
---

### 步骤 1
[x] 在MakeCode的代码抽屉中点击Advanced，查看更多代码选项。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/gun_kit/images/case_03_02.png)

为了给gun_kit手枪套件编程，我们需要添加一个扩展库。在代码抽屉底部找到"Extension"，并点击它。这时会弹出一个对话框。搜索"github.com/elecfreaks/pxt-microbit-toy-gun"，然后点击下载这个代码库。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/gun_kit/images/case_01_03.png)

***注意：如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。
### 步骤 2
在`on start`中依次插入`set openFire button`积木块，设置为`P8`口,
`set IR send`积木块，设置为`P1`口
`set bullet type`积木块，并选择参数`Pistol Cartridge`。
![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/gun_kit/images/case_01_04.png)


### 步骤 3

如图所示，在`forever`中插入`if...then`积木块，`openFire button is pressed`积木块，`openFire`积木块。


![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/gun_kit/images/case_01_05.png)

### 程序

请参考程序连接：[https://makecode.microbit.org/_hY9Lb31iL2oL](https://makecode.microbit.org/_hY9Lb31iL2oL)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_hY9Lb31iL2oL]" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  

### 现象

按下射击键则发射子弹，当子弹击中快速移动中的蜘蛛时，蜘蛛被打翻并停止动作。

## 思考
---
如何在射击时发出声音。

## 常见问题
---
## 相关阅读  
---
