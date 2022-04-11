# Cutebot智能赛车python使用示例



---


### 添加python文件
下载压缩包并解压[EF_Produce_MicroPython-master](https://github.com/elecfreaks/EF_Produce_MicroPython/archive/refs/heads/master.zip)
打开[Python editor](https://python.microbit.org/v/2.0)

![](./images/cutebot-py-01.png)

为了给酷比特智能赛车编程，我们需要添加Cutebot.py这个文件。点击Load/Save，然后点击Show Files（1）下拉菜单，再点击Add file在本地找到下载并解压完成的EF_Produce_MicroPython-master文件夹，从中选择Cutebot.py这个文件添加进来。

![](./images/cutebot-py-02.png)
![](./images/cutebot-py-03.png)
![](./images/cutebot-py-04.png)

### 示例代码
### 示例一     让小车全速前进
```
from microbit import *
from Cutebot import *
ct = CUTEBOT()
ct.set_motors_speed(100, 100)

```
### 结果
- 酷比特小车左轮速度为100，右轮速度为100，全速前进。


### 示例二    点亮车头LED灯
```
from microbit import *
from Cutebot import *
ct = CUTEBOT()
ct.set_car_light(left, 0, 90, 90)
ct.set_car_light(right, 200, 200, 0)
#设置左边车头灯为R:0，G:90,B:90;设置右边车头灯为R:200，G:200,B:0
```
### 结果
- 酷比特小车两个车头灯分别亮不同的颜色。

### 示例三    超声波避障小车
```
from microbit import *
from Cutebot import *

dis = CUTEBOT()

while(True):
    i = dis.get_distance(0)
    if i>3 and i<20:
        dis.set_motors_speed(-50, 50)
        sleep(500)
    else:
        dis.set_motors_speed(50, 50)
```
### 结果
- 酷比特小车在行驶过程中如果遇到障碍物，则立即转向。

### 示例四    巡线行驶
```
from microbit import *
from Cutebot import *

dis = CUTEBOT()

while(True):
    i = dis.get_tracking()
    if i == 10:
        dis.set_motors_speed(10, 50)
    if i == 1:
        dis.set_motors_speed(50, 10)   
    if i == 11:
        dis.set_motors_speed(25, 25)  
```
### 结果
- 酷比特小车巡线行驶。

### 示例五    控制舵机
```
from microbit import *
from Cutebot import *

dis = CUTEBOT()

while(True):
    dis.set_servo(0,180)
    sleep(1000)
    dis.set_servo(0,0)
    sleep(1000)
```
### 结果
- 酷比特小车S1端口连接的舵机往复转动。

## 相关案例
---

## 技术文档
---
