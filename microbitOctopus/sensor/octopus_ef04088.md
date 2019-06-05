# 两路巡线模块电子积木

## 简介
---
两路巡线模块电子积木集成了两组反射式红外对管，可通过它来识别黑线。通常应用该模块来做巡线智能小车，我们可以任意设计黑线轨迹，通过编程使小车按我们设计的黑线轨迹行驶。

## 特性
---
- 利用红外光探测，抗干扰能力强。
- 定位孔尺寸兼容主流小车底盘。
- 两个3P带锁杜邦接口和一个4P焊盘，能够直接用两个GVS线连接连接两个3P杜邦接口，接线十分方便。

## 参数
---
项目 | 参数 
:-: | :-: 
品名|两路巡线电子积木
SKU|EF04088
工作电压|DC 3-5V
接口|两个标准G-V-S接口
输出信号类型|数字
黑线输出电平|低电平
白线输出电平|高电平
有效距离|2~12mm
尺寸|22.74 x 37.45mm
净重|4.8g

### 外型与定位尺寸
![](./images/u76NzbX.png)

## 包装清单
---
- 1 x Octopus 2 Channel Tracking Module。
- 2 x 3P的GVS杜邦连接线 

## 快速上手
---
### 硬件连接
将模块安装在motor:bit小车上。
将左边的接口接入P13，右边的接口接入P14。（均以驾驶员视角为参照）

![](./images/iNdkjrq.jpg) 

![](./images/Y7tolMD.jpg)

### Micro:bit 示例代码
程序链接：https://makecode.microbit.org/_Ep84RMKkhcHs
你也能通过以下页面直接下载该程序。
<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_Ep84RMKkhcHs" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>

### 结果
将小车放在黑线轨迹上，打开开关，小车便沿着黑线轨迹行驶。

## 常见问题
---
