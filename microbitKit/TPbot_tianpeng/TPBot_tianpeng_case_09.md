# 案例09：寻找光源

## 目的
---
- 通过编程让天蓬智能车在黑暗中朝着光源的方向行驶。

## 使用材料
---

- 1 x [天蓬智能车](https://item.taobao.com/item.htm?spm=a1z10.5-c-s.w4002-18602834185.41.68d15ccfBFHNPy&id=618758535761)



![](./images/TPBot_tianpeng_case_01_01.png)





## 软件
---
[微软makecode](https://makecode.microbit.org/#)


## 编程
---


- 在MakeCode的代码抽屉中点击`高级`，查看更多代码选项。

![](./images/TPBot_tianpeng_case_01_02.png)

- 为了给天蓬智能车编程，我们需要添加一个扩展库。在代码抽屉底部找到`扩展`，并点击它。这时会弹出一个对话框，搜索`tpbot`，然后点击下载这个代码库。

![](./images/TPBot_tianpeng_case_01_03.png)

##示例程序
- `当开机时`设置天蓬智能车亮白色灯光。
- 在`无限循环`中，判断亮度级别是否大于设定阈值，当亮度级别大于设定阈值时，天蓬智能车向前行驶，当亮度级别小于设定阈值时，小车原地转圈。

![](./images/TPBot_tianpeng_case_09_04.png)

### 程序
- 请参考程序连接：[https://makecode.microbit.org/_dLAeeX0HFDUj](https://makecode.microbit.org/_dLAeeX0HFDUj)

- 你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_dLAeeX0HFDUj" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

## 结论
---

- 开机后天蓬智能车车头灯亮白色并原地转圈，当检测到亮度级别大于设定阈值时，则向前行驶。


## 思考
---


## 常见问题
---
Q:使用案例中的代码发现小车不能正常运行？
A:电池电量不足，增大程序中的小车速度参数的数值，并测试。

## 相关阅读  
---

