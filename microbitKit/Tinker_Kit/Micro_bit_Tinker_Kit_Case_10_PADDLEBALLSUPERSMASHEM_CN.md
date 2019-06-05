# 课程_10 乒乓球游戏

![](./images/ngNx9A3.jpg)  

一起来学习用Javascript在5x5的micro:bit屏幕上编写一个简单有趣的小游戏吧！这个游戏可能和其他的小游戏有些类似，但是它更加图形化，游戏化。


## 项目简介  
---

在这个项目中，我们将要制作一个小游戏。这个游戏主要是把小球弹到一堵墙上。如果你失手了，游戏就结束了。对于那些想寻求挑战的人来说，这是个不错的游戏哦！因为随着游戏级别的上升，游戏的难度也会加大。


## 所需材料：  
---

- 1 x BBC micro:bit
- 1 x USB线

**温馨提示: 如果你想要以上所有这些元器件，你可以购买我们的[micro:bit小小发明家套件](https://item.taobao.com/item.htm?spm=a230r.7195193.1997079397.9.z3IMPf&id=564707672256&abbucket=5)。**

![](./images/quhpGUa.jpg)


## 目标：  
---

1.了解micro:bit;
2.学习编写一个小游戏。


## 制作过程
---

### 步骤1 – 元器件连接  

首先，将micro:bit连接至电脑。

![](./images/c90TTlY.jpg)


### 步骤2 – 编程前的准备  

为了使用我们准备好的套件，我们需要添加一个代码库。在代码选择区域点击“Advanced”查看更多代码选项，并在底部寻找“Add Package”。

![](./images/fYL6XPR.jpg)

这时将会弹出一个对话框。在对话框中搜索“tinker kit”，然后点击下载这个代码库。

![](./images/CTucu8p.png)

注意：如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。


### 步骤3 – 编程  

![](./images/FowItUF.png)

首先，让我们一起来定义变量吧！我们需要很多变量来储存小球的位置、速度和方向，球拍的长度和位置，以及最后的得分情况。

![](./images/y2eJKOG.png)

其次，我们需要编写函数控制球拍。xb 代表了球拍左边第一个像素点的位置，yb代表了球拍的长度。函数left和函数right控制了xb和球拍的运动，而函数board可以使球拍显示在micro:bit屏幕上。

![](./images/zlPtelo.png)

接下来，我们需要编写函数控制小球的运动。在开始的时候，小球每秒移动一次。但是随着你的游戏级别的上升，小球运动的间隔越来越短。这是多么刺激呀！

![](./images/xlwFo1f.png)

现在，我们需要编写函数控制小球和周围物体的互动。当小球弹到一边的时候，它的水平运动改变了，但是它的垂直运动却保持不变。当小球弹到顶部的时候，它可以朝任何方向反弹，游戏变得更加有趣。

![](./images/uuUwCvm.png)

最重要的是，我们需要查看小球是否击中了球拍。如果没有击中，你就输了，micro:bit就会显示得分。如果击中了，小球也会朝任意方向反弹回来，游戏的难度会增加。

![](./images/KeNkSBL.png)

最后，我们需要用一个for循环让小球保持运动。同时，我们用函数onButtonPressed()来使球拍运动。

如果你不想自己动手编程，你可以直接下载下面的完整代码:  

[https://makecode.microbit.org/63331-03858-42547-81536](https://makecode.microbit.org/63331-03858-42547-81536)

或者，你也可以从下面这个页面下载：

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:63331-03858-42547-81536" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  


### 步骤4 - 使用  

![](./images/FAgJjFo.jpg)

将micro:bit连接电脑，运行程序。 真是太简单啦！

![](./images/HbWnEbK.jpg)

如果你的得分超过12分，你将获得一个笑脸。相反，如果你的得分低于12分，你就会获得一个哭脸。


### 步骤5 - 成功！  

太棒啦！现在你已经在micro:bit5x5的屏幕上编写了一个打乒乓球的游戏哦！你肯定非常自豪吧！


## 常见问题
---