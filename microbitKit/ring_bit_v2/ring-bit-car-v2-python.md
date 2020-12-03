# Ring:bit car V2的Python示例代码


### 步骤 1
下载压缩包并解压[EF_Produce_MicroPython-master](https://github.com/lionyhw/EF_Produce_MicroPython/archive/master.zip)
打开[Python editor](https://python.microbit.org/v/2.0)

![](./images/05001_07.png)

为了给Ring:bit car V2编程，我们需要添加Ringbit.py文件。点击Load/Save，然后点击Show Files（1）下拉菜单，再点击Add file在本地找到下载并解压完成的EF_Produce_MicroPython-master文件夹，从中选择Ringbit.py文件添加进来。

![](./images/03444_11.png)

![](./images/03444_12.png)

![](./images/ Ring-bit-car-V2-01.png)

### 步骤 2
### 参考程序

```
from microbit import *
from Ringbit import *
rb = RINGBIT(pin1, pin2)
while True:
    rb.set_motors_speed(50,50)
    sleep(1000)
    rb.set_motors_speed(0, 0)
    sleep(1000)
```


### 结果
- Ring:bit_V2小车前进一秒，静止一秒。

### 避障

```
from microbit import *
from Ringbit import *

rb = RINGBIT()
while True:
    i = rb.get_distance(0)
    if i < 20 and i > 5:
        rb.set_motors_speed(100,-100)
        sleep(1000)
    else:
        rb.set_motors_speed(100,100)
```


### 结果
- Ring:bit_V2小车避障行驶。

### 巡线

```
from microbit import *
from Ringbit import *

rb = RINGBIT()
while True:
    i = rb.get_tracking()
    if i == 11:
        rb.set_motors_speed(100,100)
    if i == 01:
        rb.set_motors_speed(100,20)
    if i == 10:
        rb.set_motors_speed(20,100)
```


### 结果
- Ring:bit_V2小车巡线行驶。


## 相关案例
---    ```
## 技术文档
---
