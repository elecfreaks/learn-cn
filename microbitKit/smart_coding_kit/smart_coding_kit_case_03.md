# 案例03：便携温度计

## 目的
---
- 使用smart coding kit手表套件完成可穿戴便携式温度计。

## 使用材料
---

- 1 x [手表套件Pro（淘宝购买链接）](https://item.taobao.com/item.htm?ft=t&id=582042009614)




![](./images/smart_coding_kit_case_03_01.png)



## 软件
---

[微软makecode](https://makecode.microbit.org/#)

## 编程
---
### 步骤 1

- 当开机时显示置顶图标并设置变量`i`为0。


![](./images/smart_coding_kit_case_03_02.png)



### 步骤 2

- 无限循环显示变量`i`的值，如果变量`i`的值大于设定值，则发出警报声，如果变量`i`的值小于设定值，则不发出警报声。




![](./images/smart_coding_kit_case_03_03.png)


### 步骤3

- 当按钮`A`被按下时则将变量`i`设置为micro:bit主板的温度返回值。


![](./images/smart_coding_kit_case_03_04.png)



### 程序
- 请参考程序连接：[https://makecode.microbit.org/_hR9djPETmd38](https://makecode.microbit.org/_hR9djPETmd38)

- 你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_hR9djPETmd38" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---


## 结论
---

- 按下按钮`A`获取当前温度并显示。


## 思考
---


## 常见问题
---
问：有时候温度明显低于20度，显示的数值更高？

答：micro:bit获取的温度为主板芯片温度，并不是环境温度。当主板运行时间过久等芯片会明显发热。

## 相关阅读  
---

