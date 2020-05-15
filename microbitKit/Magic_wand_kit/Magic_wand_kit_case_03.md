# 魔法棒套件案例03：缓解压力

## 目的
---

- 使用魔法棒套件制作一根显示笑脸的法杖

## 使用材料
---



## 故事背景
---
小恩释放飞碟传出信号并与队友汇合，但是在魔法生涯的第一战就这样受挫，整个队伍的气氛都显得有些压抑。这时候小恩决定想个办法让队友重拾自信，积极面对困难。

## 软件
---

[微软makecode](https://makecode.microbit.org/#)

## 编程
---

### 步骤 1
在MakeCode的代码抽屉中点击“高级”，查看更多代码选项。

![](./images/magicwand_case_01_02.png)

为了给魔法棒套件编程，我们需要添加一个扩展库。在代码抽屉底部找到“扩展”，并点击它。这时会弹出一个对话框，搜索”magicwand“(因为目前这个库还在审核中，在正式上架之前先通过这个链接搜索"https://github.com/elecfreaks/pxt-magicwand“)，然后点击下载这个代码库。

![](./images/magicwand_case_01_03.png)

*注意：*如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。
### 步骤 2
在模块选择区中选择变量并点击设置变量，在弹出窗口中输入'i'，点击确定。



![](./images/magicwand_case_03_04.png)


![](./images/magicwand_case_03_05.png)


### 步骤 3
在`当开机时`中，将变量'i'设为`0`。

![](./images/magicwand_case_03_06.png)

### 步骤 4

如图所示，在`无限循环`中插入`如果为...则...`积木块，判断变量'i'的值与连接P2端口的按钮的状态，当变量'i'=1且连接P2端口的按钮被按下时，则显示笑脸图标，延时5s，显示爱心图标，将变量'i'设为`0`。


![](./images/magicwand_case_03_07.png)

### 步骤 5

如图所示，选择输入模块中`当振动`积木块，设置为`6g`，插入显示数字变量'i'的值和将变量'i'设置为1.

![](./images/magicwand_case_03_08.png)




### 程序

请参考程序连接：[https://makecode.microbit.org/_hJwf5WgpT3JH](https://makecode.microbit.org/_hJwf5WgpT3JH)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_hJwf5WgpT3JH]" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  

### 现象
---
- 当摇晃法杖时显示当前法术法力值消耗，当法力值消耗显示后按下按钮则显示笑脸。
## 思考
---


## 常见问题
---
## 相关阅读  
---
