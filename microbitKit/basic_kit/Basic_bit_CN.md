# 3路IO基础扩展板（basic:bit）

## 简介
---

basic:bit是micro:bit基础扩展板。它板载了蜂鸣器，有P0、P1、P2三组GVS排针。它体积小巧、结构简单，足够完成98%以上的micro:bit案例。


## 特性
---

- 体积小巧，设计巧妙，完美地匹配micro:bit。
- 螺丝钉既能固定主板，又能引出电源与IO口。
- 引出Micro:bit主板上的P0、P1、P2、3V、GND引脚。
- 引出的三个IO口足够完成98%以上的micro:bit案例。
- 板载蜂鸣器，可通过开关选择接通与断开。


## 参数
---

- 电压：3.3V。（说明：由Micro:bit供电。）
- 可扩展IO数量：3
- 尺寸:51.7mm x 29.1mm。

### 尺寸图


## 包装清单
---

- 1 x basic:bit主板
- 7 x 螺丝钉（说明：只需要五个，另外两个备用）


## 案例学习
---

### 所需材料

- 1 x micro:bit
- 1 x basic:bit
- 1 x Octopus LED模块
- 1 x USB数据线
- 1 x GVS线（或跳线）


### 组装

![](./images/CIdYsAa.jpg)
用螺丝将basic:bit固定到micro:bit上。
将Octopus LED模块连接至P1口。
开关拨至蜂鸣器一端。

### 示例代码

程序链接：https://makecode.microbit.org/_TWuPw3eE8eEE

你也能通过以下页面直接下载该程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_TWuPw3eE8eEE" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>


### 显示效果

将以上代码保存到micro:bit上后，按下按钮A，蜂鸣器开始循环播放铃声，同时Octopus LED模块上的LED灯间隔一秒闪烁。


