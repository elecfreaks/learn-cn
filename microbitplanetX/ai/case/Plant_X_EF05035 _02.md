# 颜色识别氛围灯

## 目的
让你的AI摄像头，可以根据识别到的颜色控制氛围灯的灯光颜色。

![](./images/05035_01.png)


---

### 所需器材及连接示意图
---

- 如下图所示，将AI摄像头连接到哪吒扩展板的IIC端口，将彩虹灯条连接到哪吒扩展板的J1端口。


![](./images/05035_02_03.png)



## makecode编程
---

### 步骤 1
在MakeCode的代码抽屉中点击“高级”，查看更多代码选项。

![](./images/05001_04.png)

为了AI摄像头编程，我们需要添加一个扩展库。在代码抽屉底部找到“扩展”，并点击它。这时会弹出一个对话框，搜索”PlanetX“，然后点击下载这个代码库。

![](./images/05001_05.png)

*注意：*如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。
### 步骤 2

### 案例一 卡片识别

### 如图所示编写程序

![](./images/05035_02_06.png)


### 参考程序
请参考程序连接：[https://makecode.microbit.org/_iqM92mR7oL1d](https://makecode.microbit.org/_iqM92mR7oL1d)

你也可以通过以下网页直接下载程序，下载完成后即可开始运行程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_iqM92mR7oL1d" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

### 结果
- 将不同颜色的卡片放在AI摄像头镜头前，彩虹灯条会根据当前卡片的颜色显示相应颜色的灯光。

