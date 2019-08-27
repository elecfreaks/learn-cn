# gun kit套件案例03：手枪换弹提示

## 目的
---

- 使用gun_kit手枪套件制作一把可以显示子弹数量的手枪

## 使用材料
---

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/gun_kit/images/gun_kit_case_03_01.png)

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

在`当开机时`中插入`设置扳机连接口`积木块，设置为`P8`口。初始化彩虹LED灯环，设置引脚为`P12`，`8`颗灯珠，使用`GRB`色彩，并设置变量`i`= 0。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/gun_kit/images/gun_kit_case_03_04.png)

### 步骤 3

如图所示，当发射键被按下时，使i=i-1，然后判断i是否大于或等于0，如果i是否大于或等于0，则将彩虹LED灯环上的第i颗灯珠熄灭，并发出声音,如果i小于0，则通过声音提示换弹。



![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/gun_kit/images/gun_kit_case_03_05.png)

### 步骤 4

如图所示，
当`A`键被按下时，将i设置为8，并将彩虹LED灯环上的灯珠全部点亮为蓝色。



![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/gun_kit/images/gun_kit_case_03_06.png)

### 程序

请参考程序连接：[https://makecode.microbit.org/_fgiWY2Cwc5Cw](https://makecode.microbit.org/_fgiWY2Cwc5Cw)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_fgiWY2Cwc5Cw]" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  

### 现象
---
- 按下`A`键后8颗LED点亮，每一次按下射击键则发出声音并按顺序熄灭一颗LED灯，当LED灯全部熄灭时则发出提示音，此时按下`A`键可重新装弹。


![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/gun_kit/images/gun_kit_case_03_07.gif)


## 思考
---

## 常见问题
---
## 相关阅读  
---
