# 课程_04 光敏电阻

![](./images/MwngMAi.jpg)

## 简介
---
光敏电阻是一种基于内光电效应的特殊电阻，光线越强阻值就越低，光控开关通常就是以光敏电阻为核心元件。本次实验，我们通过光敏电阻来控制micro:bit5x5LED屏幕的亮度。

## 元件清单
---
### 硬件：
- 1 x micro:bit  
- 1 x USB线  
- 1 x micro:bit面包板扩展板  
- 1 x 面包板83 x 55 mm  
- 1 x 光敏电阻  
- 1 x 10kΩ电阻   
- 若干跳线

**温馨提示：如果你需要以上所有元件，你可以购买我们的[Elecfreaks小小科学家套件](https://item.taobao.com/item.htm?ft=t&id=597096675822)。**

![](./images/W4tseua.jpg)

## 主要元件介绍
---
### 光敏电阻
光敏电阻是用CdS或CdSe等半导体材料制成的特殊电阻器，其工作原理是基于内光电效应。光照愈强，阻值就愈低，随着光照强度的升高，电阻值迅速降低，亮电阻值可小至1KΩ以下。光敏电阻对光线十分敏感，其在无光照时，呈高阻状态，暗电阻一般可达1.5MΩ。  

![](./images/jS03zGQ.jpg)

## 实验步骤
---
### 硬件连接
根据下面的图片将你的元件连接起来：

- 1.将光敏电阻与P0口连接

- 2.将10kΩ电阻与光敏电阻并连

![](./images/FtQDhiS.jpg)

连接完成后如图:

![](./images/TMd3Fq8.jpg)

### 软件

[微软Makecode在线编辑器:makecode.microbit.org](https://makecode.microbit.org/)



### 如图所示编写程序

![](./images/case_04_01.png)

### 代码详解
- 1.当开机时，读取模拟电压作为亮度的参考值。

![](./images/case_04_02.png)

- 2.在无限循环程序块中，循环扫描P0口的模拟电压。一旦当前电压值低于基准值减去2（表示光照强度变低，光敏电阻阻值下降），就说明已经关灯，此时显示一个爱心图标，calibrationVal-2用于调节感应灵敏度，数值越小灵敏度越高。

![](./images/case_04_03.png)

### 参考程序
请参考程序连接：[https://makecode.microbit.org/_3tFFoPhLF7hX](https://makecode.microbit.org/_3tFFoPhLF7hX)

你也可以通过以下网页直接下载程序，下载完成后即可开始运行程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_3tFFoPhLF7hX" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

## 实验结果
---
开灯时，micro:bit的LED屏幕上什么都不显示；而关灯后，屏幕上显示了一个爱心图标。

![](./images/1Xu4lBR.gif)


## 思考
---
如果想要用光敏电阻来控制一颗LED的开与关，那么我们该如何设计电路与编程？

## 常见问题
---    

## 更多信息，欢迎访问：
---
[micro:bit知识库地址](https://www.elecfreaks.com/learn-cn/)       
micro:bit官方推荐供应商：[恩孚科技淘宝店](https://shop69086944.taobao.com/?spm=a230r.7195193.1997079397.2.RSthR0)    
QQ技术交流群：570756726     
