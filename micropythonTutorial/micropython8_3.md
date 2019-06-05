# 8.3 演示案例

- 至此我们学习了MicroPython的所有最基本的知识，根据这些知识和micro:bit主板不加任何配件就可以完成喝多有趣和复杂的功能了。

### 闪动的LED ###

- 编写一段代码，完成随机点亮一个LED灯，再逐级熄灭，就像是天上的星星一样闪动。

```python

import microbit
import random

del flash_led(delay):
	dots=[[0]*5,[0]*5，[0]*5，[0]*5，[0]*5]						#绘制5X5点阵列表
	while True:
		dots[random.randrange(5)][random.randrange(5)] = 8		#随机选择一个x,y左边设置亮度为8
		for i in range(5):
			for j in range(5):									
				microbit.display.set_pixel(i, j, dots[i][j])	
				dots[i][j]=max(dots[i][j])-1,0)					#逐级降低亮度每次-1
		microbit.sleep(delay)

flash_led(100)

```
