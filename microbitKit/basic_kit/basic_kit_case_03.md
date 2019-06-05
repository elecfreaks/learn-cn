# 案例03：功能选择器

## 目的
---

- 使用basic:bit套件完成功能选择器。

## 使用材料
---

- 1 x basic kit 基础套件



## 硬件连接图
---

- 如图所示，将按键模块连接到basic:bit主板的P0口，电位器模块连接到P1。

![](./images/F9hvl7u.jpg)

## 软件
---
- [微软makecode](https://makecode.microbit.org/#)在线积木块编程[https://makecode.microbit.org/#](https://makecode.microbit.org/#)

- 按钮模块以模拟值读取I/O口返回值，值如下。
	1. A按钮<10
	2. B按钮10-80
	3. C按钮80-130
	4. D按钮130-160
	5. E按钮160-600

## 编程
---
### 步骤 1

- 设置一个永久循环，以模拟数字方式读取P0口，将返回值赋值给`itmmm`变量，用于判断哪个键按下。
- 当变量`itmmm`小于10，意为A按钮按下。当A按钮按下，调用函数`func_A`调用结束后将变量`flag`(函数内部循环判断变量)设置为0。
- 当变量`itmmm`小于80，意为B按钮按下。当B按钮按下，调用函数`func_B`调用结束后将变量`flag`(函数内部循环判断变量)设置为0。
- 当变量`itmmm`小于130，意为C按钮按下。当C按钮按下，调用函数`func_C`。

![](./images/2lRCpIO.png)

### 步骤 2

- `func_A`函数：当`flag`变量大于600，(也就是没有按下按钮)读取P1口并且描绘在点阵显示屏上。读取P0口按键状态，当按下E按钮，循环结束，函数调用结束。
- `func_B`函数：当`flag`变量大于600，(也就是没有按下按钮)显示一颗闪烁的心，每闪烁一次后，读取P0口按键状态，当按下E按钮，循环结束，函数调用结束。
- `func_C`函数，清空屏幕，调用结束。


![](./images/HpH2rIY.png)

### 程序

请参考程序连接：[https://makecode.microbit.org/_cuufKuP6FARo](https://makecode.microbit.org/_cuufKuP6FARo)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_cuufKuP6FARo" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---


## 结论
---

- 上电时因为判断按钮并不为ABC按钮，则显示一个小房子图标。
- 按下按钮A，调用func_A函数，用电位器控制点阵显示屏亮度。按下任意按钮调用结束。
- 按下按钮B，调用func_B函数，显示一颗跳动的心。按下任意按钮调用结束。
- 按下按钮C，调用func_C函数，清空屏幕。
- 其他情况显示一个小房子图标。


## 思考
---


## 常见问题
---
问：有时候按下按钮却没有反应。
答：按钮判断不是每时每刻，在运行其他代码期间按下按钮程序不会判断。

## 相关阅读  
---

中断：[中断是指计算机运行过程中，出现某些意外情况需主机干预时，机器能自动停止正在运行的程序并转入处理新情况的程序，处理完毕后又返回原被暂停的程序继续运行。](https://baike.baidu.com/item/%E4%B8%AD%E6%96%AD/3933007)
