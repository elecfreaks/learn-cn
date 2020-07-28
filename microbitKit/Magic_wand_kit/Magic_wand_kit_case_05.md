# 魔法棒套件案例05：法力提醒

## 目的
---

- 使用魔法棒套件制作一根可以显示剩余法力值的魔法棒

## 使用材料
---



## 故事背景
---
魔法棒充能完毕，这是小恩仅剩的魔力储备，也是队伍里最后的魔法能量了。小恩决定给魔法棒设置一个魔力值消耗提示，提醒自己节省能量。

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
在`当开机时`中，初始化流光溢彩灯，设置连接引脚`P8`，`8`颗LED灯，将变量'i'设为`7`，设置灯环显示蓝色。

![](./images/magicwand_case_05_07.png)


### 步骤 4

如图所示，当`P2`按钮被按下时，将灯环的第i+1颗灯设置为红色，然后刷新显示，然后以-1为幅度更改i。

![](./images/magicwand_case_05_08.png)

### 程序

请参考程序连接：[https://makecode.microbit.org/_2AJ1jJgjbXjJ](https://makecode.microbit.org/_2AJ1jJgjbXjJ)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_2AJ1jJgjbXjJ]" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  

### 现象
---
- 开机后灯环显示蓝色，当按钮被按下则将最后一颗亮蓝色LED灯变为红色。




## 思考
---

## 常见问题
---
## 相关阅读  
---
