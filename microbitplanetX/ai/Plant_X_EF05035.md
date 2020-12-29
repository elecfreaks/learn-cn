# AI摄像头

## 简介
AI摄像头，可以实现人脸识别、小球追踪、卡片识别和一键学习的功能。

![](./images/05035_01.png)

## 特性
---
- RJ11端口设计，防止误插，易于使用。
## 技术规格
---

项目 | 参数 
:-: | :-: 
SKU|EF05044
接口|RJ11
接口类型|IIC
工作电压|3.3V
核心IC|K210





## 外形与定位尺寸
---


![](./images/05035_02.png)


## 使用RJ11转杜邦线的接线方式
---

当使用没有RJ11扩展接口的micro:bit扩展板时，可以使用RJ11转杜邦线的连接线，将RJ11接口连接摄像头，杜邦线接口的一端黑线接GND，红线接VCC，绿线接P19（SDA）端口，黄线接P20（SCL）端口；如果使用过程中摄像头无法启动，请尝试给AI摄像头单独供电。

![](./images/05035_03.png)

以iot:bit为例：

![](./images/05035_04.png)

注意：当使用哪吒扩展板之外的micro:bit扩展板连接AI摄像头时，添加扩展库应搜索
 [https://github.com/elecfreaks/pxt-PlanetX-AI](https://github.com/elecfreaks/pxt-PlanetX-AI)


### 添加python文件

为了方便的使用python对AI摄像头进行编程，我们可以使用已经编写好的库[EF_Produce_MicroPython-master](https://github.com/lionyhw/EF_Produce_MicroPython/archive/master.zip)，只需要调用函数并修改参数即可实现对应的功能。

下载压缩包并解压[EF_Produce_MicroPython-master](https://github.com/lionyhw/EF_Produce_MicroPython/archive/master.zip)

打开[Python editor](https://python.microbit.org/v/2.0)

![](./images/AI-py-01.png)

为了给AI摄像头编程，我们需要添加AILens.py这个文件。点击Load/Save，然后点击Show Files（1）下拉菜单，再点击Add file在本地找到下载并解压完成的EF_Produce_MicroPython-master文件夹，从中选择AILens.py这个文件添加进来。


![](./images/AI-py-02.png)

![](./images/AI-py-03.png)

![](./images/AI-py-04.png)


### API


| API | 描述 | 
| :------------: | :-----------: |
|`AILENS()`|初始化AI摄像头模块。|
|`switch_function(func)`|选择摄像头功能，`func`选择功能：（`Learn`特征学习；`Card`卡片识别；`Face`人脸识别；`Tracking`巡线识别；`Color`颜色识别；`Ball`小球识别）。|
|`get_card_content()`|识别卡片内容。|
|`get_card_data()`|用列表的方式返回画面中卡片的信息：（X轴坐标、Y轴坐标、宽度、高度、置信度、图像中卡片总数、当前卡片ID）。|
|`get_face()`|判断画面中是否存在人脸。|
|`get_face_data()`|用列表的方式返回画面中人脸的信息：（X轴坐标、Y轴坐标、宽度、高度、置信度、图像中人脸总数、当前人脸ID）。|
|`get_ball_color()`|检测画面中的小球颜色|
|`get_ball_data()`|用列表的方式返回画面中小球的信息：（X轴坐标、Y轴坐标、宽度、高度、置信度、图像中小球总数、当前小球ID）。|
|`get_track_data()`|用列表的方式返回画面中线段的信息：（偏移角度、偏移距离、线段长度）。|
|`get_color_type()`|检测画面中的卡片颜色|
|`get_color_data()`|用列表的方式返回画面中的颜色信息：（X轴坐标、Y轴坐标、宽度、高度、置信度、图像中颜色总数、当前颜色ID）。|
|`learn_object(learn_id)`|以ID号来学习一个物品，ID号：1~5。|
|`get_learn_data()`|用列表的方式返回画面中已学习物品的信息：（物品ID、置信度）。|







### 示例代码
### 示例一     特征学习
```
from microbit import *
from AILens import *
ai = AILENS()
ai.switch_function(Learn)
while True:
    ai.get_image()
    if button_a.is_pressed():
        ai.learn_object(1)
    buff = ai.get_learn_data()
    if buff[0] == 1:
        display.show(Image.HAPPY)
    else:
        display.show(Image.SAD)


```
### 结果
- 按下A键学习物品，当识别到所学习的物品时，显示笑脸，否则显示哭脸。


### 示例二    颜色识别
```
from microbit import *
from AILens import *
ai = AILENS()
ai.switch_function(Color)
while True:
    ai.get_image()
    if (ai.get_color_type() == "Green"):
        display.show(Image.HAPPY)
        sleep(2000)
    else:
        display.show(Image.SAD)
```
### 结果
- 当识别到绿色卡片的时候，显示笑脸两秒，否则显示哭脸。

### 示例三    小球识别
```
from microbit import *
from AILens import *
ai = AILENS()
ai.switch_function(Ball )
while True:
    ai.get_image()
    if (ai.get_ball_color() == "Red"):
        display.show(Image.HAPPY)
        sleep(2000)
    else:
        display.show(Image.SAD)
```
### 结果
- 当识别到红色小球的时候，显示笑脸两秒，否则显示哭脸。

### 示例四    识别黑线
```
from microbit import *
from AILens import *
ai = AILENS()
ai.switch_function(Tracking)
while True:
    ai.get_image()
    buff = ai.get_track_data()
    
    if buff[1] > 100:
        display.show(Image.HAPPY)
    else:
        display.show(Image.SAD)
```
### 结果
- 当摄像头中的黑线偏向左边时，LED矩阵显示哭脸，当黑线偏向右边时，LED矩阵显示笑脸。

### 示例五    识别人脸 
```
from microbit import *
from AILens import *
ai = AILENS()
ai.switch_function(Face )
while True:
    ai.get_image()
    
    if ai.get_face():
        display.show(Image.HAPPY)
    else:
        display.show(Image.SAD)
```
### 结果
- 当识别到人脸时显示笑脸，否则显示哭脸。

### 示例六   识别卡片
```
from microbit import *
from AILens import *
ai = AILENS()
ai.switch_function(Card)
while True:
    ai.get_image()
    
    if (ai.get_card_content() == "Stop"):
        display.show(Image.HAPPY)
        sleep(2000)
    else:
        display.show(Image.SAD)
```
### 结果
- 当识别到“停止”卡片时显示笑脸，否则显示哭脸。





