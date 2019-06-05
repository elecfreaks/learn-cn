# 7.1 Python中的随机数

### 随机选择 ###
- 有时候你想让事情变得无序一点，让程序看似有自己的想法，这时候你需要生成一些随机的东西，MicroPython提供了一个对象用来生成随机数，他就是`random`可以轻松为你的代码引入随机和混乱。
- `random`对象可以从提供的列表字符串元组等符合数据类型中，随机选择一个元素作为参数返回，例如：

```python

from microbit import *
import random

str_list = ["A","B","C","D","E","F","G"]

display.show(random.choice(str_list))

```

- 上边的例子代码完成了一个随机选择功能，`random.choice`这个方法为从参数中选择一个元素作为参数返回，例子中从number列表里选择了A-G中间一个字母返回，并且显示在点阵显示屏上，每次上电运行时，字母都可能不一样。


### 随机数字 ###

- 随机数字非常有用，在游戏中非常常见，还有需要程序自己完成的选择代码也很常见。
- MicroPython附带了几个很有用的生成随机数的方法，例如：

```python

from microbit import *
import random

display.show(str(random.randint(1,6)))

```

- 上边的代码完成了一个随机数字的功能，每次上电运行时显示的数字都可能不一样。

- 如果你需要生成一个带有指定步幅的列表，可以使用`random.randrange(start,stop,step)`，`start`表示开始的范围，包括开始，`stop`表示结束的范围，不包括结束。`step`表示步幅。例如：

```python

random.randrange(1,10,2)		#生成1到10之间的基数。

```
- 有时候你需要生成带有小数点的数字，这些数字被成为浮点数，可以使用`random.random()`的方法生成带有小数的数字,它生成的范围是0.0到1.0之间。

### 随机数相关API ###

| API | 描述 | 
| :------------: | :-----------: |
|`random.seed()`|使用已知整数初始化随机数生成器n。这将从给定的起始状态（n）给出可重现的确定的随机性。|
|`random.randint(a，b)`|返回一个随机整数N，范围a <= N <= b|
|`random.randrange(stop)`|返回0到`stop`(但不包括)之间随机选择的整数。|
|`random.randrange(start, stop)`|从`start`到`stop`中返回一个随机选择的整数。|
|`random.randrange(start, stop, step)`|从中返回随机选择的元素。|
|`random.choice(seq)`|从非空序列中返回一个随机元素`seq`。如果`seq`是空的，报错`IndexError`|
|`random.random()`|返回[0.0,1.0]范围内的下一个随机浮点数|
|`random.uniform(a, b)`|返回随机浮点数N，使得对a <= N <= b。|



