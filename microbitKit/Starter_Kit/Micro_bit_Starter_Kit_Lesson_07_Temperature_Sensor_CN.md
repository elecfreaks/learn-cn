# 课程_07 温度传感器

![](./images/fMCJitN.jpg)

## 简介
---
温度传感器是指能感受温度并转换成可用输出信号的传感器。温度传感器是温度测量仪表的核心部分，品种繁多。在这次的实验中，我们将学习模拟温度传感器——TMP36，并将它的数值读出显示在micro:bit的显示屏上。

## 元件清单
---
### 硬件：
- 1 x micro:bit
- 1 x USB线
- 1 x microbit面包板扩展板
- 1 x 面包板83 x 55 mm
- 1 x TMP36温度传感器  
- 若干跳线

**温馨提示：如果你需要以上所有元件，你可以购买我们的[Elecfreaks小小科学家套件](https://item.taobao.com/item.htm?spm=a1z10.1-c-s.w4024-17803785896.2.18dc3f94XOgpWg&id=562837851877&scene=taobao_shop)。**

![](./images/W4tseua.jpg)

## 主要元件介绍
---
### TMP36

TMP36是一种模拟温度传感器，它的输出电压与温度成线性关系，温度越高，输出电压越大。

![](./images/SDoXRcM.jpg)

**注意：**

当我们正视TMP36芯片有文字的一面时，芯片最左边的引脚为VCC，中间引脚为Vout，最右边的引脚为GND。千万不要把芯片接反了，否则也能引起器件损坏。

![](./images/P6ZkUDh.jpg)

TMP36输出电压随温度变化的曲线是这样的：

![](./images/5R7izFc.jpg)
![](./images/U2c4qdp.jpg)

由上图可知温度的计算公式为：

温度（℃）=（输出电压(mV) - 500 ) / 10

## 实验步骤
---
### 硬件连接
根据下面的图片将你的元件连接起来：

- 1.温度传感器与扩展板P0口连接

![](./images/HnUeLBR.jpg)

连接完成后如图:

![](./images/IAor80B.jpg)

### 软件

[微软Makecode在线编辑器:makecode.microbit.org](https://makecode.microbit.org/)

![](./images/JHZUvh2.png)

### 如图所示编写程序

![](./images/8kZxYpc.png)

### 代码详解
- 1.将P0通过传感器获取的数值，使用map函数，映射成0~1023之间的一个值，保存在voltage中
- 2.将voltage中的值进行处理，转换成温度值，在点阵屏上面显示

![](./images/8kZxYpc.png)

### 参考程序
请参考程序连接：[https://makecode.microbit.org/_AKuYFoDsLJ7D](https://makecode.microbit.org/_AKuYFoDsLJ7D)

你也可以通过以下网页直接下载程序，下载完成后即可开始运行程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_AKuYFoDsLJ7D" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

## 实验结果
---
micro:bit屏幕上显示当前温度值。

![](./images/b0w5PkN.gif)


## 思考
---

## 常见问题
---

## 更多信息，欢迎访问：
---
[micro:bit知识库地址](https://www.elecfreaks.com/learn-cn/)    
micro:bit官方推荐供应商：[恩孚科技淘宝店](https://shop69086944.taobao.com/?spm=a230r.7195193.1997079397.2.RSthR0)  
QQ技术交流群：570756726   



