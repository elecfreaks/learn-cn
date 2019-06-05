# 课程_12 遥控小车

你有没有用micro:bit做过一个远程控制的项目呢？今天，让我们一起来做一个micro:bit遥控项目吧！这个项目需要2块micro:bit主板。你可以和你的一个小伙伴搭档，或者再拿一块micro:bit。 不要把小伙伴的micro:bit都拿走哦!


## 目标
---

- 学习远程控制micro:bit小车。
- 用一块备用的micro:bit做一个遥控器。


## 所需材料  
---

- 1 x BBC micro:bit
- 1 x USB线
- 1 x 电池盒
- 2 x AA电池
- 1 x micro:bit小车

**温馨提示: 如果你想要以上所有这些元器件，你可以购买我们的[micro:bit小小发明家套件](https://item.taobao.com/item.htm?spm=a230r.7195193.1997079397.9.z3IMPf&id=564707672256&abbucket=5)。** 


## 制作过程  
---

### 步骤1

在MakeCode里设置radio代码组。这可以确保你的发送器和接收器在同一个频道。
想一想遥控器上每个按键的功能。
通过使用所示积木块，每个按键按下，Radio就会发送一个不同的数字。
你可以在Radio代码选择区域下方找到这些积木块。
把这些代码下载到micro:bit, 你的遥控器就做好了。
现在遥控器上的每个按键都可以发送一个不同的指令了哦！

![](./images/GK13ZiA.png)


### 步骤2

在micro:bit小车的项目(或者是其他你想要遥控的项目) 中添加相同的radio代码组至 On Start积木块项下。
 
这能确保你的项目可以接收正确的指令哦!

![](./images/KsZS4Mg.png)


### 步骤3

还记得我们每按下一个遥控按键所发送的数字吗？我们将使用这些数字来引发动作。
在Radio代码选择区域中查找图中所示的radio received积木块。
用一个if-then积木块来检查你收到的数字，看它是不是你按下按键A所发送的数字。  
然后把micro:bit小车左转的代码放入到这个if-then积木块下方。
同时，我们需要添加一个指向左的LED指示来展示执行我们设定的动作。
将P0设置为0，让左边的舵机停止转动。

![](./images/9buZPoA.png)


### 步骤4

要让你的micro:bit小车向右转，你只需要按照上面的代码进行类似的设置就行了。向右转了之后，要让轮子停下来。你也可以选择在接收每个指令之后，让轮子不停地滚动。但是你会发现小车将不停地旋转。
将代码下载至你的micro:bit小车中。

![](./images/8jAmhRg.png)


如果你不想自己亲手编写代码，你可以通过下面这个链接下载程序的完整代码：

**发送：** [https://makecode.microbit.org/_gH73AW4Dy1rP](https://makecode.microbit.org/_gH73AW4Dy1rP)
**接收：** [https://makecode.microbit.org/_4am87cCWb0e9](https://makecode.microbit.org/_4am87cCWb0e9)

或者，你也可以从下面这个页面下载：  

**发送：**  

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_TKE3rA7CqL2w" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  


**接收：**  

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_4am87cCWb0e9" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  


### 太棒啦！

现在请将所有的代码下载到micro:bit，装上电池，准备让你的小车跑起来吧！试试看如果A、B同时按下，会发送哪些指令。或者尝试一下除了按键之外的不同输入方式，然后遥控你所有的micro:bit项目。太爽啦!不用离开座位，坐着就能掌控一切。


## 常见问题
---