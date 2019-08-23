# 专用灯条模块

## 简介
---
- Ring:bit car V2灯条模块，是Ring:bit二代小车的专用扩展模块，连接简单功能强大，一卡一锁为你的Ring:bit小车扩展更多灯带。
- 搭载8颗Rainbow LED灯珠，全彩色，可以实现自动车灯、彩虹车灯等功能。
 
![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/ring_bit_v2/images/ring_bit_v2_Rainbow_01.jpg)![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/ring_bit_v2/images/ring_bit_v2_Rainbow_02.jpg)

## 特性
---
- 输入电压为3V~5V，micro:bit能直接驱动。

- 标准的3线GVS接口，仅占用一个IO口。

- 8颗小型灯珠，更加省电。

- 每颗灯珠都可以独立编程，显示RGB色彩。

## 参数
---

 项目 | 参数 | 备注
 :-: | :-: |:-:
 品名|Ring:bit car v2专用灯条扩展模块|-
 SKU|EF03425|-
 工作电压|DC 3-5V|-
 接口|Ring:bit car专用弹针卡口|螺丝固定
 输出信号类型|模拟|-
 搭载灯珠|8颗|-
 尺寸|60.8 x 33.20mm|-
 净重|5.7g|-


## 外形与安装定位尺寸
---

 ![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/ring_bit_v2/images/ring_bit_v2_Rainbow_03.png)

## 快速上手
---	
### 硬件连接  
---

- 首先将灯条模块插入Ring:bit小车底板插口。
 
 ![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/ring_bit_v2/images/ring_bit_v2_Rainbow_04.gif)

- 随后在反面用两颗螺丝固定。

 ![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/ring_bit_v2/images/ring_bit_v2_Rainbow_05.gif) ![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/ring_bit_v2/images/ring_bit_v2_Rainbow_06.gif)

- 扩展完成。

 ![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/ring_bit_v2/images/ring_bit_v2_Rainbow_07.jpg)

### 软件编程  
---

- 在[makecode](https://makecode.microbit.org/)在线编辑器中编写一段简单的彩虹灯代码。
- 设置Strip变量，初始化连接到到P0的10颗LED。
- 设置LED显示rainbow彩虹色。
- 在forever中循环位移颜色。
- 显示颜色。

 ![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/ring_bit_v2/images/ring_bit_v2_Rainbow_08.png)

 程序代码链接：[https://makecode.microbit.org/_3Wc1k8Ckg9vF](https://makecode.microbit.org/_3Wc1k8Ckg9vF)

 你也能通过下列窗口直接下载代码：

 <div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_3Wc1k8Ckg9vF" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>

### 结果
---
- 彩虹车灯。

## 常见问题
---
