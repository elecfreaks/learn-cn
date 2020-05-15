# 魔法棒套件案例01：遭遇险情

## 目的
---

- 使用魔法棒套件制作一根可以将蜘蛛打翻的魔法棒

## 使用材料
---

## 故事背景
---
在一个幽暗静谧的峡谷中突然传来了一阵窸窸窣窣的脚步声，第一次离开魔法学院进行试炼的小恩和他的队友小心翼翼的探索前进。突然前面的草丛露出了一双红色的眼睛，小恩的队伍遭遇了一只虫族哨兵，让我们快速的制作一根魔法棒来释放魔法，驱逐虫族吧。

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

在`当开机时`中插入`设置魔法等级`积木块，设置为`初级`，并设置红外发射连接口为'P1'。

![](./images/magicwand_case_01_04.png)


### 步骤 3

如图所示，在`在'P2'的按钮被按下时`中插入`释放一次魔法`积木块。



![](./images/magicwand_case_01_05.png)


### 程序

请参考程序连接：[https://makecode.microbit.org/_E0Y7rg53hK46](https://makecode.microbit.org/_E0Y7rg53hK46)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_E0Y7rg53hK46]" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  

### 现象

按下按钮则发射魔法，当魔法击中快速移动中的蜘蛛时，蜘蛛被打翻并停止动作。

## 思考
---
如何在使用魔法时发出声音。

## 常见问题
---
## 相关阅读  
---
