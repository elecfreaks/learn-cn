# 魔法棒套件案例02：召集队员

## 目的
---

- 使用魔法棒套件制作一根可以控制信号飞碟的魔法棒
## 使用材料
---



## 故事背景
---
虽然成功的驱逐了虫族哨兵，但是由于战斗的动静惊动了虫巢，虫群涌动。小恩和他的队友只能在虫群发动攻击前仓促撤离。虽然已经成功的撤退到安全地带，但在慌乱中小恩和他的队友失散了。让我们帮助小恩制作一个法杖，快速的发出信号召集队友吧。

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

在`当开机时`中，插入`设置红外发射连接口`积木块，设置为`P1`。

![](./images/magicwand_case_02_04.png)


### 步骤 3

如图所示，当`向右倾斜`时，如果连接在`P2`端口的按钮被按下，则`设置魔法等级为初级`，然后`释放一次魔法`；当`向左倾斜`时，如果连接在`P2`端口的按钮被按下，则`设置魔法等级为高级`，然后`释放一次魔法`。

![](./images/magicwand_case_02_05.png)
### 程序

请参考程序连接：[https://makecode.microbit.org/_5ufbHfhXkcHz](https://makecode.microbit.org/_5ufbHfhXkcHz)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_5ufbHfhXkcHz]" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  

### 现象
---
- 当魔法棒向右倾斜时，按下按钮则飞碟起飞。
- 当魔法棒向左倾斜时，按下按钮则飞碟降落。

## 思考
---


## 常见问题
---
## 相关阅读  
---
