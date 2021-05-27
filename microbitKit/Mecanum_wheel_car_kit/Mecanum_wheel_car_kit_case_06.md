# 麦克纳姆轮小车套件案例06：智能避障小车

## 目的
---

- 使用麦克纳姆轮小车套件制作一辆可以避障的小车

## 使用材料
---

- [麦克纳姆轮小车套件（淘宝购买链接）](https://item.taobao.com/item.htm?ft=t&id=604443327840)
- [超声波传感器（不包含在套件里，需要额外购买）](https://item.taobao.com/item.htm?ft=t&id=642627759623)

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

为了使用超声波模块，我们需要添加一个扩展库。在代码抽屉底部找到“扩展”，并点击它。这时会弹出一个对话框，搜索”github.com/elecfreaks/pxt-sonarbit”，然后点击下载这个代码库。

![](./images/Mecanum_wheel_car_kit_case_03_04.png)



*注意：*如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。

### 步骤 2

点击`悟空`选择`麦克纳姆轮`模块。



![](./images/Mecanum_wheel_car_kit_case_01_03.png)


### 步骤 3

如图所示，在`当开机时`中插入`设置麦克纳姆轮`积木块，并设置相应舵机连接口。



![](./images/Mecanum_wheel_car_kit_case_06_05.png)


### 步骤 4

如图所示，设置小车向前移动，并判断前方障碍物与超声波传感器的距离，如果距离小于25cm，则小车后退500ms，然后左转500ms。

![](./images/Mecanum_wheel_car_kit_case_06_06.png)


### 程序

请参考程序连接：[https://makecode.microbit.org/_39AepD2A95jM](https://makecode.microbit.org/_39AepD2A95jM)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_39AepD2A95jM]" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  

### 现象

小车开启后向前行驶，如果检测到前方有障碍物，则后退并向左转弯，避开障碍物，然后继续前进。

## 思考
---

## 常见问题
---
## 相关阅读  
---
