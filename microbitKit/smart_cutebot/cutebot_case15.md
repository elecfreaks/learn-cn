# 案例15:寻光小车

## 目的
---
- 让cutebot智能赛车完成自动寻找光源的功能

## 使用材料
---
- 1 x [Cutebot套件](https://www.elecfreaks.com/store/cute-bot.html)
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

注意：如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。

### 步骤 2

- 在`无限循环`中，判断`亮度级别`的大小，当亮度级别小于设定阈值时，小车`全速左转`，当亮度级别大于设定阈值时，小车`全速前进`，

![](./images/case_15_01.png)


### 程序

请参考程序连接：[https://makecode.microbit.org/_UatK2a6cgc7u](https://makecode.microbit.org/_UatK2a6cgc7u)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;">
<iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:https://makecode.microbit.org/_UatK2a6cgc7u" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin">
</iframe>
</div>  
---

## 结论
---
- 当没有检测到光源的时候小车原地旋转，当检测到光源时，小车全速前进。

## 思考
---

## 常见问题
---
## 相关阅读  
---
