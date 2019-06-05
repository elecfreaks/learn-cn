# 7.3 指南针

> micro:bit主板带有一个指南针，可以精确的根据地球磁场判断方向(根据初始化情况而定)，每次调用前都需要初始化模块，如果你需要设计制作气象站，可以根据此模块计算风向。

![](./images/2UMV4MA.png)

### 指南针API ###

| API | 描述 | 
| :------------: | :-----------: |
|`microbit.compass.calibrate()`|初始化指南针模块,详情见温馨提示。|
|`microbit.compass.is_calibrated()`|如果指南针已成功校准吗，返回True否则返回False。|
|`microbit.compass.clear_calibration()`|撤销校准，使指南针再次校准。|
|`microbit.compass.get_x()`|根据磁场力，给出X轴上的读数，返回值为正整数或者负整数。|
|`microbit.compass.get_y()`|根据磁场力，给出y轴上的读数，返回值为正整数或者负整数。|
|`microbit.compass.get_z()`|根据磁场力，给出z轴上的读数，返回值为正整数或者负整数。|
|`microbit.compass.heading()`|根据上述数值，计算出方向，以度为单位表示，顺时针方向，正北方返回值为0，范围为0~360度。|
|`microbit.compass.get_field_strength()`|测量设备周围磁场强度，返回值为整数。|

***温馨提示：***每次使用指南针之前都需要初始化校准，校准是一个小游戏，旋转移动micro:bit使LED屏上完成一个圆，校准成功会显示一个笑脸。

![](./images/V4wZAP1.png) ![](./images/EW3J71r.png)

### 示例：简易的指南针 ###

- 用指南针模块和点阵显示屏模块完成一个简单的指南针，还记得在点阵显示屏那一章中提到了内置图像有`clocks`时钟类型，时钟的时针就像是指南针的表针一样，可以用这个来表示北方。

```python

from microbit import *

compass.calibrate()							#初始化指南针模块

while True:
    sleep(100)
    needle = ((15 - compass.heading()) // 30) % 12			#处理指南针模块返回参数
    display.show(Image.ALL_CLOCKS[needle])					#根据参数needle，显示ALL_CLOCKS列表中的图像来指示北方方向

```
