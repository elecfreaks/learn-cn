# 案例15：可调速天蓬智能车

## 目的
---
- 使用电位器模块调节天蓬智能车的行驶速度。

## 使用材料
---

- [天蓬智能车（淘宝购买链接）](https://item.taobao.com/item.htm?ft=t&id=627045784239)



![](./images/TPBot_tianpeng_case_01_01.png)


## 硬件连接

将电位器连接到天蓬智能车的端口1。


![](./images/TPBot_tianpeng_case_15_02.png)

## 软件
---
[微软makecode](https://makecode.microbit.org/#)


## 编程
---


- 在MakeCode的代码抽屉中点击`高级`，查看更多代码选项。

![](./images/TPBot_tianpeng_case_01_02.png)

- 为了给天蓬智能车编程，我们需要添加一个扩展库。在代码抽屉底部找到`扩展`，并点击它。这时会弹出一个对话框，搜索`tpbot`，然后点击下载这个代码库。

![](./images/TPBot_tianpeng_case_01_03.png)

- 为了给电位器模块编程，我们需要添加一个代码库。在代码抽屉底部找到“扩展”，并点击它。这时会弹出一个对话框。搜索`PlanetX`，然后点击下载这个代码库。

![](./images/TPBot_tianpeng_case_15_03.png)

##示例程序
- `当开机时`设置micro:bit的LED矩阵显示图标。
- 在`无限循环`中，将电位器模块的返回值由0~1023映射到0~100，然后将映射之后得到的值设置为天蓬智能车前进的速度。

![](./images/TPBot_tianpeng_case_15_04.png)


### 程序
- 请参考程序连接：[https://makecode.microbit.org/_ArRM71PD6de0](https://makecode.microbit.org/_ArRM71PD6de0)

- 你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_ArRM71PD6de0" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

---
## 结论
---

- 开启电源后，通过调节电位器模块来控制天蓬智能车的行驶速度。


## 思考
---


## 常见问题
---
Q:使用案例中的代码发现小车不能正常运行？
A:电池电量不足，增大程序中的小车速度参数的数值，并测试。

## 相关阅读  
---

