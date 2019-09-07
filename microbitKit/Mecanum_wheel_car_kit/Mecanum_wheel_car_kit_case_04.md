# Mecanum wheel car kit套件案例04：遥控麦克纳姆轮小车

## 目的
---

- 使用Mecanum wheel car kit套件和joystick:bit制作一辆可以遥控的小车

## 使用材料
---

- Mecanum wheel car kit套件、joystick:bit

## 背景知识
---

## 软件
---

[微软makecode](https://makecode.microbit.org/#)

## 编程
---

### 步骤 1
 在MakeCode的代码抽屉中点击“高级”，查看更多代码选项。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/Mecanum_wheel_car_kit/images/Mecanum%20wheel%20car%20kit_case_01_01.png)

为了给Mecanum wheel car kit套件编程，我们需要添加一个扩展库。在代码抽屉底部找到“扩展”，并点击它。这时会弹出一个对话框，搜索”wukong”，然后点击下载这个代码库。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/Mecanum_wheel_car_kit/images/Mecanum%20wheel%20car%20kit_case_01_02.png)

为了使用joystick:bit，我们需要添加一个扩展库。在代码抽屉底部找到“扩展”，并点击它。这时会弹出一个对话框，搜索”joystickbit”，然后点击下载这个代码库。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/Mecanum_wheel_car_kit/images/Mecanum%20wheel%20car%20kit_case_04_04.png)



*注意：*如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。

### 步骤 2

麦克纳姆轮小车程序如下：


![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/Mecanum_wheel_car_kit/images/Mecanum%20wheel%20car%20kit_case_04_05.png)


先设置无线设置组，然后初始化麦克纳姆轮小车舵机。将无线接收到的数据存入`I`。然后通过判断变量`I`的值来控制麦克纳姆轮小车的动作。


### 步骤 3

游戏手柄程序如下：


![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/Mecanum_wheel_car_kit/images/Mecanum%20wheel%20car%20kit_case_04_06.png)


设置无线设置组，然后通过判断手柄摇杆和按键的状态来发送数字。


### 程序

麦克纳姆轮小车程序：请参考程序连接：[https://makecode.microbit.org/_T2iiDyJyEJyp](https://makecode.microbit.org/_T2iiDyJyEJyp)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_T2iiDyJyEJyp]" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  


游戏手柄程序：请参考程序连接：[https://makecode.microbit.org/_e5dHb6c9xbt8](https://makecode.microbit.org/_e5dHb6c9xbt8)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_e5dHb6c9xbt8]" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  

### 现象

通过游戏手柄控制小车行动。


## 思考
---

## 常见问题
---
## 相关阅读  
---
