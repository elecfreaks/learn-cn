# 专用超声波扩展模块

## 简介
---
- Sonar:bit是一个3线宽压超声波模块，它的工作电压为3.0V-5V，3.3v或5V的单片机系统均能使用；它只需要3根线（G、V、S）就可以工作，比常规的4线超声波模块节省一个IO口。Sonar:bit量程为4cm~400cm，测量数据稳定准确，误差仅为±1cm。
- 它可以使用扩展片与Ring:bit连接，为Ring:bit小车扩展超声波功能。
 
![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/ring_bit_v2/images/ring_bit_v2_sonar_01.jpg)

## 特性
---
- 输入电压为3V~5V，micro:bit能直接驱动。

- 标准的3线GVS接口，仅占用一个IO口。

## 参数
---

 项目 | 参数 | 备注
 :-: | :-: |:-:
 品名|Ring:bit car v2专用超声波扩展模块|-
 SKU|EF04089|-
 工作电压|DC 3-5V|-
 接口|3pin GVS接口|-
 输出信号类型|模拟|-
 量程|4-400cm|-
 尺寸|40.60mm * 51.60mm|-
 净重|12g|-


## 外形与安装定位尺寸
---

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/ring_bit_v2/images/ring_bit_v2_sonar_02.jpg)

## 快速上手
---	
### 硬件连接  
---

- 首先使用铆钉将扩展亚克力连接到Ring:bit小车后板插口。
 
![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/ring_bit_v2/images/ring_bit_v2_sonar_03.jpg)

- 再将Sonar:bit使用铆钉连接到扩展亚克力板上方。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/ring_bit_v2/images/ring_bit_v2_sonar_04.jpg)

- 使用3pin连接线连接到Ring:bit扩展板，扩展完成。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/ring_bit_v2/images/ring_bit_v2_sonar_05.jpg)

### 软件编程  
---

- 首先在makecode中扩展`sonar:bit`积木块。
- 在搜索框中搜索`https://github.com/elecfreaks/pxt-sonarbit`，点击图标下载该库。
- 在[makecode](https://makecode.microbit.org/)在线编辑器中编写一段超声波测距代码。


![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/ring_bit_v2/images/ring_bit_v2_sonar_06.png)

 程序代码链接：[https://makecode.microbit.org/_dKHX3EReM78X](https://makecode.microbit.org/_dKHX3EReM78X)

 你也能通过下列窗口直接下载代码：

 <div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_dKHX3EReM78X" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>

### 结果
---

- LED 点阵显示屏显示超声波返回的厘米数值

## 相关文档
---
[案例10:防撞小车](http://www.elecfreaks.com/learn-cn/microbitKit/ring_bit_v2/ring_bit_car_v2_case_10.html)

