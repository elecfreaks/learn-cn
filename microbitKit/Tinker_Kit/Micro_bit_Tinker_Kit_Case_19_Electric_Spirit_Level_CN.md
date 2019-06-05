# 课程_19 电子水平仪

今天，我们要用micro:bit来制作一个水平仪。这个水平仪可以展示物体的倾斜状况。制作过程非常简单哦！

## 制作目标  
---

- 学习用micro:bit内置的加速度传感器来获取倾斜状况。
- 学习如何使用micro:bit板子上5*5LED点阵。

## 所需材料  
---

- 1 x BBC micro:bit
- 1 x USB线
- 2 x AA 电池

**温馨提示: 如果你想要以上所有这些元器件，你可以购买我们的[micro:bit小小发明家套件](https://item.taobao.com/item.htm?spm=a230r.7195193.1997079397.9.z3IMPf&id=564707672256&abbucket=5)。**


## 准备工作  
---

- 用USB线把你的micro:bit连接到电脑上。
- 点击 makecode.microbit.org进入Javascript编辑器。


## 步骤0：代码流程图  
---

在开始写代码之前，我们需要明确我们想用程序来实现什么效果，要让每个部件运行起来，我们需要怎么排列它们的顺序。

为了制作这个水平仪，我们将在循环里面设置的代码步骤分别是：

从加速度传感器上读取倾斜。
把物体的倾斜用micro:bit主板上的LED点阵显示出来。
检查之前的循环中倾斜的变化。
创建不同倾斜方向的LED坐标数组。
将LED坐标绘制到micro:bit主板上的LED点阵上。

此外，我们需要添加的一些其他功能包括：

1.校准。初始化倾斜位置。
2.返回默认的倾斜校准。

## 制作过程  
---

### 步骤1：定义变量  

首先，我们需要定义图中所示的变量。这些变量分别是：

tiltList: 用来存储在0-4的值之间的倾斜范围的数组，倾斜的顺序依次是向左、向右、向前、向后。
tiltBoundary: 在0（不倾斜）和1（微斜）之间首次倾斜的边界。
prevState: 以tiltList的格式存储上一个循环的micro:bit倾斜数值的数组，用于检测迭代之间的倾斜变化。 
ledPlotList: 以（x,y）的格式绘制LED坐标数组。为了定义一个数组，我们使用了number[][]数据类型来代表type: number的一个嵌套的变量数组。

### 步骤2：:把倾斜数值转换为水平  

因为5x5LED点阵只能显示有限的信息，实际的倾斜值将不会被显示出来。
然而，函数tiltExtent()用参数num代表加速度传感器的倾斜值，并把这些倾斜值 (num) 转换成0-4的倾斜水平。  
0 代表在所给的方向中没有倾斜，4代表大倾斜，而-1则是代表出错后的返回。
在这里，tiltBoundary和tiltSensitivity都用作倾斜水平之间的边界值。

### 步骤 3: 编写倾斜水平  

两个函数checkRoll（）和checkPitch（）将从tiltExtent（）获得的倾斜度等级写入到tiltList中，分别用于在坐标轴上执行roll（左右）和pitch（前后）。

在使用倾斜值之前，我们用一个0值来校准之后所写的校准函数中的pitch (zeroPitch) 和roll (zeroRoll)。

因为不管是向左倾斜还是向前倾斜，加速度传感器读取的值都是负数，所以我们需要使用函数Math.abs() function来获取tiltExtent()函数中得到的负数值的系数，用于作为这两个方向的参数。

### 步骤 4: 编写 LEDPlotList函数  

在tiltList获得了倾斜度之后，我们现在就可以编写LED绘制函数，因为任何情况都有可能发生，即
plotSingle(): 只向一个方向倾斜，把所给方向的倾斜范围作为参数。
plotDiagonal(): 向2个方向等量倾斜，把任意一个方向的倾斜范围作为参数。
plotUnequal(): 向2个方向倾斜不同量级，把每个方向的倾斜范围作为参数。先使用plotDiagonal()，然后将其添加至ledPlotList数组。

这些绘制函数将一个LED坐标数组写入稍后编写的ledPlotList。

### 步骤 5: 绘制LED点阵  

选择步骤4中的3个绘制函数，现在我们就可以绘制实际的LED点阵来满足倾斜角度可能出现的不同组合。因为步骤4中的3个函数没有方向的区别，我们需要调整LED点阵的坐标值，将LED绘制到正确的方位。

PlotResult() 包含了多个if条件语句。它可以检验倾斜的类型，并使用led.plot(x, y).绘制相应的点阵。这些可能出现的倾斜组合是：
单向倾斜: 只向左倾斜或只向右倾斜。


单向倾斜: 只向前倾斜或只向后倾斜。



双向倾斜：向前向左倾斜或向后向左倾斜。



双向倾斜：向前向右倾斜或向后向右倾斜。


注意：对于双向倾斜，每个组合可能有相同或者不同量级（通过对比maxX和maxY来检查）。因此，它们分别使用plotDiagonal() 或plotUnequal() 来绘制。


### 步骤 6: 编写 Calibration（校准）函数  

编写完这么多代码之后，现在我们需要添加calibTilt() 和resetTilt()函数。

calibTilt()可以把micro:bit现在位置的倾斜角度变为0。
resetTilt()可以重置micro:bit，让它回到最初的状态。

### 步骤 7: 编写State（状态）函数  

为了检查倾斜角度是否有变化，我们添加了一个简单的函数checkState()。

如果倾斜角度不变，也就是说stateChange == 0，我们就能直接进入到下一个程序描述，并且跳过LED点阵的绘制，减少所需的计算。

### 步骤 8: 代码整合1  

现在我们终于把所有的必要的函数添加到了infinite（无限）循环中让它们反复运行。

首先，用input.onButtonPressed()将micro:bit上的按钮A和B分别设置到函数calibTilt()和resetTilt()中。当校准完成的时候，在LED点阵上绘制一个勾。

### 步骤 9: 代码整合2  

接下来，根绝我们在步骤0里面的代码流程图，运行必要的函数，检查状态的变化(这指的是在上一段代码运行之后，micro:bit的倾斜角度有变化)。

如果倾斜角度有变化，也就是说stateChange == 1，代码将会把prevState里面的角度更新为新的倾斜角度，,下一段代码中的stateChange将设置为0，并用PlotResult()在LED点阵上绘制更新后的倾斜角度。

如果你不想自己亲自动手编写代码，你可以从下面这个链接直接下载程序的完整代码：

[https://makecode.microbit.org/56811-31458-64502-76623](https://makecode.microbit.org/56811-31458-64502-76623)

或者，你可以从下面这个页面下载代码：

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:56811-31458-64502-76623" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>


### 步骤 10: 部件组装  

将完整的代码存储至micro:bit。将micro:bit和电池组小心地贴在某个物体上，然后就可以开始使用了哦！

### 太棒啦!  

祝你玩得愉快！当你熟练之后，你可以尝试更多关于倾斜传感器的扩展可能或者把它变成一个小游戏哦！
 

## 常见问题
---