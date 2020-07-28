# 魔法棒套件案例04：魔法棒充能

## 目的
---

- 使用魔法棒套件制作一根可以充能的魔法棒

## 使用材料
---



## 故事背景
---
小恩成功的用神奇的魔法让整个团队的气氛活跃了起来，但是在战斗、召集队友，驱散负能量之后，小恩的魔法棒耗尽魔力亮起了红灯。这时候大家才发现，在匆忙的撤退过程中没来得及带走补给，所以小恩决定用自身的魔力给魔法棒充能。

## 软件
---

[微软makecode](https://makecode.microbit.org/#)

## 编程
---

### 步骤 1
在MakeCode的代码抽屉中点击“高级”，查看更多代码选项。

![](./images/magicwand_case_01_02.png)

为了给魔法棒套件编程，我们需要添加一个扩展库。在代码抽屉底部找到“扩展”，并点击它。这时会弹出一个对话框，搜索”magicwand“(因为目前这个库还在审核中，在正式上架之前先通过这个链接搜索"https://github.com/elecfreaks/pxt-magicwand“)，然后点击下载这个代码库。

![](./images/magicwand_case_01_03.png)

*注意：*如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。
### 步骤 2
在模块选择区中选择变量并点击设置变量，在弹出窗口中输入'i'，点击确定。



![](./images/magicwand_case_03_04.png)


![](./images/magicwand_case_03_05.png)


### 步骤 3
在`当开机时`中，初始化流光溢彩灯，设置连接引脚`P8`，`8`颗LED灯，将变量'i'设为`-1`。

![](./images/magicwand_case_04_07.png)


### 步骤 4

如图所示，在`无限循环`中，判断在`P2`口的按钮是否被按下，当按钮被按下时，则循环执行，以1为幅度更改'i'，设置像素'i'颜色为蓝色，刷新显示并暂停500毫秒。当按钮没有被按下时，判断'i'的大小，当'i'小于7时，将变量'i'的值设为-1，设置灯环显示为红色。


![](./images/magicwand_case_04_08.png)

### 程序

请参考程序连接：[https://makecode.microbit.org/_7V63c6LsMAoj](https://makecode.microbit.org/_7V63c6LsMAoj)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_7V63c6LsMAoj]" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  

### 现象
---
- 开机后灯环显示红色，当按钮按下时则开始为魔法棒充能，灯环逐颗点亮为蓝色。如果在灯环全部LED灯变为蓝色前松开按钮，则充能失败，回到初始状态。如果灯环全部变为蓝色，则充能成功。




## 思考
---

## 常见问题
---
## 相关阅读  
---
