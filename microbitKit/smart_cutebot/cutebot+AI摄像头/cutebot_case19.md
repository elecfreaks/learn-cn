# 案例19:cutebot+AI摄像头：小球追踪

## 目的
---
- 使用cutebot智能赛车搭配AI摄像头实现小球追踪功能。

## 使用材料
---
- 1 × [Cutebot V3.0](https://www.elecfreaks.com/store/cute-bot.html)
- 1 × [Cutebot套件锂电池扩展包](https://www.elecfreaks.com/cutebot-lithium-battery-pack.html)
- 1 × [AI摄像头](https://www.elecfreaks.com/elecfreaks-smart-ai-lens-kit.html)

*注意：AI摄像头适用于 Cute bot V 3.0只有（可以看到底板上打印的版本号）。*

![](./images/cutebot-16-04.png)

## 安装方式
---
### 锂电池安装步骤：

![](./images/cutebot-step-01.png)

### 积木支架结构搭建步骤：

零件清单：

![](./images/cutebot-step-02.png)

搭建步骤：

![](./images/cutebot-step-03.png)

![](./images/cutebot-step-04.png)

![](./images/cutebot-step-05.png)

![](./images/cutebot-step-06.png)

![](./images/cutebot-step-07.png)

![](./images/cutebot-step-08.png)

![](./images/cutebot-step-09.png)



### AI摄像头连线方式：
将连接线的RJ11接口的一端连接到AI摄像头，另一端杜邦线接口的一端连接到下图所示的位置，需要注意连接线的接口是否正确。

![](./images/cutebot-step-10.png)

*注意：这个积木支架结构是可以活动的，我们可以手动调节AI摄像头的视角，在使用AI摄像头时，应该根据功能需求来调节角度。*

## 软件平台
---
[微软 makecode](https://makecode.microbit.org/#)

## 编程
---
### 步骤 1
- 在MakeCode的代码抽屉中点击“高级”，查看更多代码选项。

![](./images/cutebot-pk-1.png)

- 为了给Cutebot套件编程，我们需要添加一个代码库。在代码抽屉底部找到“扩展”，并点击它。这时会弹出一个对话框。搜索`Cutebot`，然后点击下载这个代码库。

![](./images/cutebot-pk-11.png)


为了给AI摄像头编程，我们需要添加一个代码库。在代码抽屉底部找到“扩展”，并点击它。这时会弹出一个对话框。搜索` https://github.com/elecfreaks/pxt-PlanetX-AI`，然后点击下载这个代码库。

![](./images/cutebot-pk-12.png)


*注意：如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。*

### 步骤 2

- 在`当开机时`中，初始化AI摄像头，切换摄像头功能为小球识别模式。

![](./images/case-19-01.png)

- 在`无限循环`中，从摄像头获取一帧图像的信息，
- 如果图像中包含小球，则判断小球的尺寸，当小球尺寸小于100时，说明小球离cutebot较远，此时通过从图像中获取小球的X坐标值来判断小球位置，如果X坐标值小于80时，说明小球在cutebot的左前方，设置cutebot左轮速度为0%，右轮速度为20%，小车左转，否则如果X坐标值大于144时，说明小球在cutebot的右前方，设置cutebot左轮速度为20%，右轮速度为0%，小车右转，否则设置cutebot左右轮速度为25%；当小球尺寸不小于100时，则说明小球离cutebot比较近，设置cutebot停止行驶。

![](./images/case-19-02.png)


### 程序

![](./images/case-19-03.png)

请参考程序连接：[https://makecode.microbit.org/_FWL7247fyfCk](https://makecode.microbit.org/_FWL7247fyfCk)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;">
<iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:https://makecode.microbit.org/_FWL7247fyfCk" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin">
</iframe>
</div>  
---

## 结论
---
- 当摄像头识别到小球时，cutebot向小球行驶，当cutebot离小球的距离足够近时，cutebot停止行驶。




## 思考
---

## 常见问题
---
## 相关阅读  
---
