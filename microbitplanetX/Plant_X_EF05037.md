# 语音识别模块

## 简介
实现语音智能控制，如语音控制智能车前进、后退、启动巡线模式等。

![](./images/05037_01.png)

## 特性
---
- RJ11端口设计，防止误插，易于使用。
## 技术规格
---

项目 | 参数 
:-: | :-: 
SKU|EF05037
接口|RJ11
接口类型|IIC
工作电压|3.3V
核心IC|SNR3512M





## 外形与定位尺寸
---


![](./images/05037_02.png)


## 快速上手
---

### 所需器材及连接示意图
---

- 如下图所示，将语音识别模块连接到哪吒扩展板的IIC端口，并将风扇模块连接到哪吒扩展板的J1端口。


![](./images/05037_03.png)



## makecode编程
---

### 步骤 1
在MakeCode的代码抽屉中点击“高级”，查看更多代码选项。

![](./images/05001_04.png)

为了给语音识别模块编程，我们需要添加一个扩展库。在代码抽屉底部找到“扩展”，并点击它。这时会弹出一个对话框，搜索”PlanetX“，然后点击下载这个代码库。

![](./images/05001_05.png)

*注意：*如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。
### 步骤 2
### 如图所示编写程序

![](./images/05037_06.png)


### 参考程序
请参考程序连接：[https://makecode.microbit.org/_YV1V3d6Ha8bo](https://makecode.microbit.org/_YV1V3d6Ha8bo)

你也可以通过以下网页直接下载程序，下载完成后即可开始运行程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_YV1V3d6Ha8bo" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

### 结果
- 通过语音识别模块控制风扇转动。


## 相关案例
---

## 技术文档
---
