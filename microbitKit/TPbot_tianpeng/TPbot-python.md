# 天蓬智能车python使用示例



---


### 添加python文件
下载压缩包并解压[EF_Produce_MicroPython-master](https://github.com/lionyhw/EF_Produce_MicroPython/archive/master.zip)
打开[Python editor](https://python.microbit.org/v/2.0)

![](./images/TPbot-py-01.png)

为了给天蓬智能车编程，我们需要添加TPBot.py这个文件。点击Load/Save，然后点击Show Files（1）下拉菜单，再点击Add file在本地找到下载并解压完成的EF_Produce_MicroPython-master文件夹，从中选择TPBot.py这个文件添加进来。

![](./images/TPbot-py-02.png)

![](./images/TPbot-py-03.png)

![](./images/TPbot-py-04.png)

### 示例代码
### 示例一     让小车全速前进
```
from microbit import *
from TPBot import *

tp = TPBOT()
tp.set_motors_speed(100,100)
# 设置左右轮电机速度

```
### 结果
- 天蓬智能车左轮速度为100，右轮速度为100，全速前进。


### 示例二    车头LED灯随机变色
```
from microbit import *
from TPBot import *
import random

tp = TPBOT()

while True:
    R = random.randint(0,255);
    G = random.randint(0,255);
    B = random.randint(0,255);
    tp.set_car_light(R,G,B)
    sleep(500)
```
### 结果
- 天蓬智能车的车头LED灯随机变色。

### 示例三    超声波避障小车
```
from microbit import *
from TPBot import *

tp = TPBOT()
while True:
    i = tp.get_distance(0)
    if i>3 and i<30:
        tp.set_motors_speed(-50, 50)
        sleep(500)
    else:
        tp.set_motors_speed(50, 50)
```
### 结果
- 天蓬智能车在行驶过程中如果遇到障碍物，则立即转向。

### 示例四    巡线行驶
```
from microbit import *
from TPBot import *

tp = TPBOT()
while True:
    
    i = tp.get_tracking()
    if i == 10:
        tp.set_motors_speed(10, 50)
    if i == 1:
        tp.set_motors_speed(50, 10)   
    if i == 11:
        tp.set_motors_speed(25, 25)  
```
### 结果
- 天蓬智能车巡线行驶。

### 示例五    控制舵机
```
from microbit import *
from TPBot import *

tp = TPBOT()
while True:
    tp.set_servo(1,180)
    sleep(1000)
    tp.set_servo(1,0)
    sleep(1000)
```
### 结果
- 天蓬智能车S1端口连接的舵机往复转动。

## 相关案例
---

## 技术文档
---
