# 专用巡线模块

## 简介
---
- Ring:bit car V2巡线模块，是Ring:bit二代小车的专用扩展模块，连接简单功能强大，一卡一锁为你的Ring:bit小车扩展巡线功能。
- 搭载双红外探头，有效探测距离2~12mm，可以完成巡线绕圈，黑线检测，边缘检测等功能。
 
![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/ring_bit_v2/images/ring_bit_v2_line_01.jpg)![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/ring_bit_v2/images/ring_bit_v2_line_02.jpg)

## 特性
---
- 输入电压为3V~5V，micro:bit能直接驱动。

- 标准的3线GVS接口，仅占用一个IO口。

- 利用红外光探测，抗干扰能力强

## 参数
---

 项目 | 参数 | 备注
 :-: | :-: |:-:
 品名|Ring:bit car v2专用巡线扩展模块|-
 SKU|EF03424|-
 工作电压|DC 3-5V|-
 接口|Ring:bit car专用弹针卡口|螺丝固定
 输出信号类型|模拟|-
 有效距离|2~12mm|-
 尺寸|34.15 x 27.20mm|-
 净重|4.7g|-


## 外形与安装定位尺寸
---

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/ring_bit_v2/images/ring_bit_v2_line_03.png)


## 快速上手
---	
### 硬件连接  
---

- 首先将巡线模块插入Ring:bit小车底板插口。
 
![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/ring_bit_v2/images/ring_bit_v2_line_04.gif)

- 随后在反面用两颗螺丝固定。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/ring_bit_v2/images/ring_bit_v2_line_05.gif) ![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/ring_bit_v2/images/ring_bit_v2_line_06.gif)

- 扩展完成。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/ring_bit_v2/images/ring_bit_v2_line_07.jpg)

### 软件编程  
---

- 在[makecode](https://makecode.microbit.org/)在线编辑器中编写一段简单的巡线代码。

- 开机时初始化左右轮连接口为P1和P2。
- 当左检测头偏离黑线，右轮停止，左轮以50的速度以矫正回归黑线。
- 右检测头同理。
- 当两个检测头均检测到黑线，以100的速度向前行驶。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/ring_bit_v2/images/ring_bit_v2_line_08.png)

 程序代码链接：[https://makecode.microbit.org/_Tsp78xP5yPu2](https://makecode.microbit.org/_Tsp78xP5yPu2)

 你也能通过下列窗口直接下载代码：

 <div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_Tsp78xP5yPu2" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>

### 结果
---
- 可以实现缓慢的巡线绕圈跑。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/ring_bit_v2/images/ring_bit_v2_line_09.gif)

## 常见问题
---
