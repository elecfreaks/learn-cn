# classroom:bit 资料
## 简介
classroom:bit 是一款基于 micro:bit 的扩展板，它扩展了 micro:bit 上的主要IO口，以GVS形式引出，通过它能扩展各种3V的电子积木，如LED灯、光敏、舵机等。它还板载了蜂鸣器和噪音传感器，classroom:bit 与 micro:bit V1.5组合可以实现 micro:bit V2.0的所有功能。
![](/Image-1.png)

## 特性
- 以GVS端子形式扩展出所有费复用的IO口。
- 板载蜂鸣器与噪音传感器，与 micro:bit V1.5组合使用可实现 micro:bit V2.0的功能。
- 单独引出IIC接口，能直接插入OLED、BME280等IIC器件。
- 支持乐高接口。

## 参数  
|**参数**|项目|
|:--:|:--:|
|品名|classroom:bit|
|版本号|V1.0|
|工作电话|2.7~3.3v|
|蜂鸣器|支持|
|噪音传感器|支持|
|乐高接口|支持|
|尺寸|60mm x 48mm|


##外形与定位尺寸
![](/Image-2.png)

## 主要功能模块介绍
### USB电源接口  
![](/Image-3.png)
可接入microUSB 电缆为扩展板供电（也能通过 micro:bit 为扩展板供电），在接入舵机等大电流外设时，推荐使用该接口供电

### GVS排针  
![](/Image-4.png)
可通过该接口扩展3v的电子积木模块。中间的IIC排母亦可接入OLED屏幕、8*16点阵等模块。

### 蜂鸣器及其开关  
![](/Image-5.png)
蜂鸣器通过P0口控制，使用蜂鸣器时需要将开关拨至上方。

### 噪音传感器及其开关    
![](/Image-6.png)
噪音传感器通过P1口控制，使用噪音传感器时需要将开关拨至上方。

### 鳄鱼夹接口  
![](/Image-7.png)
可通过他来连接鳄鱼夹。

### 乐高固定孔  
![](/Image-8.png)
这两个孔的孔径与孔距符合乐高标准，可通过该孔将 classroom:bit 固定在乐高零件上。

## 快速上手
将 micro:bit 插入 classroom:bit 扩展板。  
![](/Image-9.png)

### 软件编程
classroom:bit 上的噪音传感器需要使用软件库驱动。在Makecode中搜索“smarthome”，然后点击下载这个软件库。  
![](/Image-10.png)
注意：如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。

软件库添加完成后编写如下程序：    
![](/Image-11.png)

按下按钮A时，蜂鸣器播放音乐，环境音量大小以柱状图的形式显示在micro:bit 5x5 点阵屏上。

程序代码链接：https://makecode.microbit.org/_AgT0axchq1R5

你也能通过下列窗口直接下载代码：
<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_AgT0axchq1R5" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>

## 常见问题
暂无
