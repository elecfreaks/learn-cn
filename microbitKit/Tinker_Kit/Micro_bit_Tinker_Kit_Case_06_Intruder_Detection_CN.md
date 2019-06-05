# 课程_06 入侵检测

## 入侵检测系统  


在这个项目中，我们将创造一个入侵检测系统。当有人开门的时候，它就会发出警报，而房屋的状态也会显示在OLED屏幕上。

## 所需材料：  
---

- 1 x BBC micro:bit
- 1 x USB线
- 1 x 扩展板
- 1 x 碰撞传感器
- 1 x OLED
- 1 x 蜂鸣器
- 2 x 母对母的跳线

**温馨提示: 如果你想要以上所有这些元器件，你可以购买我们的[micro:bit小小发明家套件](https://item.taobao.com/item.htm?spm=a230r.7195193.1997079397.9.z3IMPf&id=564707672256&abbucket=5)。**


## 目标：  
---

- 了解碰撞传感器、OLED和蜂鸣器。
- 用OLED进行创作。
- 用碰撞传感器进行创作。


## 制作过程  
---

### 步骤 1 – 元器件连接  

将micro:bit插入扩展板，并用USB线连接micro:bit。

![](./images/cvJnbqE.jpg)

然后，用跳线将蜂鸣器连接到扩展板上的引脚P0。如下图所示，插入OLED。你可以将它插入到扩展板上3排排针孔的任意一排。

![](./images/3benydL.jpg)

将碰撞传感器连接到扩展板上的引脚P1。确保线的颜色和扩展板上引脚的颜色一致。

![](./images/YvQkd81.jpg)


### 步骤 2 – 编程前的准备  

![](./images/qPgEmnW.jpg)

我们将添加一个代码库来方便使用我们套件中的元器件。在代码抽屉中点击Advanced，查看更多代码选项，并在代码抽屉底部找到Add Package。

![](./images/IWhPZeP.png)

这将会弹出一个对话框。在对话框中搜索“tinker kit”， 然后点击下载这个代码库。

![](./images/b0vriWO.png)

注意：如果你收到提示说一些代码库因为不兼容的问题将被删除，你可以选择根据提示操作，或者在项目文件的菜单中选择新建一个新项目。


### 步骤 3 – 编程  

![](./images/OKjXb0c.jpg)

点击代码抽屉中的Tinkercademy, 找到与我们元器件相应的积木块。

![](./images/UwHfSVv.jpg)

你应该在开始的时候初始化OLED。64和128分别代表了OLED的高度和宽度。

![](./images/GIhLCLU.jpg)

因为这里只有两个条件，所以我们只需要一个“else-if”语句。
当碰撞传感器被触发，蜂鸣器响起，OLED屏幕上将会显示“Intruder Detected”（检测到入侵）。否则，蜂鸣器不会响起，OLED屏幕上显示“The house is safe”（房屋处于安全状态）。

如果你不想自己亲手编写代码，你可以从下面这个链接直接下载程序的完整代码：

[https://makecode.microbit.org/_A0zFxqMPMXbo](https://makecode.microbit.org/_A0zFxqMPMXbo)

或者，你也可以从下面这个页面下载：

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_A0zFxqMPMXbo" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>


### 步骤 4 – 成功!  

太棒啦！你已经创造出了一个入侵检测器哦！


## 常见问题
---