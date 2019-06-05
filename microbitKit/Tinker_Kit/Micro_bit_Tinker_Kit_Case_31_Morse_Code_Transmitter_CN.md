

# 课程_31 摩斯密码发射
---
- 在MakeCode页面给你的micro:bit编程，做一个简单的莫斯密码发射器（需要准备几个弹簧夹哦）

    此项目由加州大学伯克利分校的Anahita在新加坡暑期实习期间设计。



## 目标
---

![](./images/YOYd2Bm.png)


 1. 成功连接2台micro:bit
 2. 通过A,B按钮控制micro:bit间的信号发送
 3. 通过A,B按钮控制micro:bit间的信号接收
 4. 学习在MakeCode中编程

            
    
## 所需材料
---
- 2 x micro:bits
- 4 x 鳄鱼夹
- 1 x micro USB接线


## 步棸 0 – 预备
---
- 我们会编写两则代码：一则是从micro:bit中发送信号；另一则是从micro:bit中接收信号。
- 为了让接收信号的micro:bit辨别信号发送，我们需要在信号发送和信号停止之间设定一个时间段。
- 这样，我们可以通过暂停时长来辨别信号的发送。


## 步棸 1 – 鳄鱼夹
---

![](./images/b7We5ZR.png)

我们希望通过第一台micro:bit上的pin1金手指发送信号，通过第二台micro:bit的pin2金手指接收（反之亦然）

连接:

1. GND（第一台micro:bit） 连 GND（第二台micro:bit）。
2. 3V （第一台micro:bit）连 3V（第二台micro:bit）。
3. Pin 1（第一台micro:bit） 连 Pin 2（第二台micro:bit）。
4. Pin 2（第一台micro:bit） to Pin 1（第二台micro:bit）。


## 步棸2 – 信号发送: 按钮 A
---

![](./images/6nlQFM9.png)

按下按钮A即发送信号。把此信号定义为一个“小点”（如上图示）。

1. 打开一个未编程的MakeCode页面，命名为“Sender（发送）”。
2. 从Logic中拖出“if-then-else”嵌入至forever下方。
3. 从Input中拖出“button A is pressed”嵌入至if后方。
4. 从Basic中拖出“show led block”嵌入至then后方，在led屏中间点一个小点。
5. 点击Advacnced，在Pins中找到“digital write pin”，设置P0为1。(这个代码表示发送信号)。
6. 从Basic中拖出“pause（ms）”，设置为230 ms。（这个暂停时间指信号发送时间）。
7. 点击Advacnced，在Pins中找到“digital write pin”，设置P0为0。(这个代码表示信号停止发送)。
8. 从Basic中拖出“pause（ms）”，设置为50 ms。

## 步棸 3 – 信号发送: 按钮 B
---

![](./images/gtjlrr9.png)

按下按钮B即发送信号。把此信号定义为一个“三小点”。

1. 在“if-then-else”添加一个“else if”。
2. 如上图所示，按照步棸2重复操作。（按下按钮B，“三小点”显示并暂停 470 ms）。
3. 在“else”后方嵌入”show icon“ 表示信号发送完成。



## 步棸 4 – 接收: 感应信号
---

![](./images/z13lhzA.png)

我们需要用到“running time (ms)”代码框记录信号接收和信号停止的时间。

1. 在MakeCode新建一个项目，命名为“Receiver”。
2. 从Loops抽屉中拖出“while do”方块嵌入至“forever”下方。
3. 从“Logic”抽屉中拖出“=”嵌入至while后方。
4. 在“=”前面嵌入digital read pin方块，将数字设为1（这个代码意为micro:bit已探测到信号;一定要将digital read pin设为P2弹簧夹夹取的位置）。
5. 在“Variables”中设置一个新变量为“keyDownTime”。
6. 添加“if-then”嵌入至“do”后方。
7. 从Logic中拖出“not”至if后方嵌入，附上keyDownTime变量。
8. 进入Input，点击more，拖出running time (ms)至“set keyDownTime to”后方。


 
## 步棸5 – 接收: 显示信号
---

![](./images/Z4yzOpc.png)

在屏幕上显示正确信号。

1. 在“Logic”中拖出“if-then”方块嵌入至“while”下方，嵌入DragkeyDownTime变量至if后方 (此代码表示方框内的指令会在接收信号后运行)。
2. 在“Variable”抽屉中添加变量“duration”，在后面嵌入“Math”抽屉中的“0-0”方块，添加“running 。time”和“keyDownTime” ，此代码表示编程开始运行的时长和信号被侦测的时间。
3. 从“Logic”中拖出“if-then”方块，在后方嵌入“0<0”为duration < 250(我们在此设定为250是因为前面的代码“小点”设定的是230ms)。
4. 如上图编码所示“show led”，一个小点。
5. 如上图编码所示“show led”，三个小点。
6. 添加一个“clear screen”，在信号被接收后，屏幕信息会被清除。
7. 设置keyDownTime为0，当你发送新信号的时候，micro:bit又会开始运行。



## 完成!
---

先检查两台micro:bit的LED显示屏是可工作的，当你按下按钮，两台micro:bit都会显示相同信号。 

想要挑战更多？试试在第二台micro:bit上转换摩斯密码把
