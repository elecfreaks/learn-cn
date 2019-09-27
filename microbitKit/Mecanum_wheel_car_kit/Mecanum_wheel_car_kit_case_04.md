# 麦克纳姆轮小车套件案例04：转向灯

## 目的
---

- 使用麦克纳姆轮小车套件制作一辆可以显示转弯方向的小车

## 使用材料
---

- 麦克纳姆轮小车套件

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

为了给麦克纳姆轮小车套件编程，我们需要添加一个扩展库。在代码抽屉底部找到“扩展”，并点击它。这时会弹出一个对话框，搜索”wukong”，然后点击下载这个代码库。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/Mecanum_wheel_car_kit/images/Mecanum%20wheel%20car%20kit_case_01_02.png)

*注意：*如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。

### 步骤 2

点击`悟空`选择`麦克纳姆轮`模块。



![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/Mecanum_wheel_car_kit/images/Mecanum%20wheel%20car%20kit_case_01_03.png)


### 步骤 3

如图所示，在`当开机时`中插入`设置麦克纳姆轮`积木块，并设置相应舵机连接口，然后初始化LED灯。



![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/Mecanum_wheel_car_kit/images/Mecanum%20wheel%20car%20kit_case_04_05.png)


### 步骤 4

如图所示，设置变量`L`和`R`为0~100的随机数；然后判断L和R的数值大小，如果R>L则设置LED0为黑色、LED1为黄色，如果L>R则设置LED1为黑色、LED0为黄色，然后刷新显示；最后将小车左前轮和左后轮速度设置为变量`L`的值，右前轮和右后轮速度设置为变量`R`的值，并延时2秒。



![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/Mecanum_wheel_car_kit/images/Mecanum%20wheel%20car%20kit_case_04_06.png)


### 程序

请参考程序连接：[https://makecode.microbit.org/_4ya4KTUXz5zx](https://makecode.microbit.org/_4ya4KTUXz5zx)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_4ya4KTUXz5zx]" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  

### 现象

小车每2秒随机调整左右轮速度改变前进方向，当左转时则点亮左边LED灯，当左转时则点亮左边LED灯。

## 思考
---

## 常见问题
---
## 相关阅读  
---
