# 麦克纳姆轮小车套件案例08：寻找光源

## 目的
---

- 使用麦克纳姆轮小车套件制作一辆可以寻找光源的小车

## 使用材料
---

- [麦克纳姆轮小车套件（淘宝购买链接）](https://item.taobao.com/item.htm?ft=t&id=604443327840)

## 背景知识
---

## 软件
---

[微软makecode](https://makecode.microbit.org/#)

## 编程
---

### 步骤 1
 在MakeCode的代码抽屉中点击“高级”，查看更多代码选项。

![](./images/Mecanum_wheel_car_kit_case_01_01.png)

为了给麦克纳姆轮小车套件编程，我们需要添加一个扩展库。在代码抽屉底部找到“扩展”，并点击它。这时会弹出一个对话框，搜索”wukong”，然后点击下载这个代码库。

![](./images/Mecanum_wheel_car_kit_case_01_02.png)

*注意：*如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。

### 步骤 2

点击`悟空`选择`麦克纳姆轮`模块。



![](./images/Mecanum_wheel_car_kit_case_01_03.png)


### 步骤 3

如图所示，在`当开机时`中插入`设置麦克纳姆轮`积木块，并设置相应舵机连接口，然后初始化LED灯。



![](./images/Mecanum_wheel_car_kit_case_08_05.png)


### 步骤 4

如图所示，设置变量`i`设为亮度级别；然后判断变量`i`的值，当`i`的值小于50 的时候小车向左旋转，当`i`的值大于或等于50 的时候小车向前行驶。



![](./images/Mecanum_wheel_car_kit_case_08_06.png)


### 程序

请参考程序连接：[https://makecode.microbit.org/_Kv3dfY02f52g](https://makecode.microbit.org/_Kv3dfY02f52g)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_Kv3dfY02f52g]" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  

### 现象

小车周围没有光源时，小车原地旋转，当小车旋转的过程中检测到周围有大于阈值的光源时，则向光源方向直线行驶。

## 思考
如何让小车在离光源越远的地方速度越快，在离光源越近的地方速度越慢。

## 常见问题
---
## 相关阅读  
---
