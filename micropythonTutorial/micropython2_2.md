## 2.2 Python中的程序结构 ##
----------
- 上一节`Hello World`程序已经烧录到Micro:bit板子中，并且完成相应的代码功能,现在我们来分析一下这段代码中具体做了什么。


```Python
	from microbit import * 
		display.scroll("Hello, World!")
```
1. 第一行代码：`from microbit import *`

- 为了理解这行代码，我们引入MicroPython的第一个概念：**模块**。
- Python 模块(Module)，是一个 Python 文件，以 .py 结尾，包含了 Python 对象定义，类和变量，也能包含可执行的代码。
- 模块让你能够有逻辑地组织你的 Python 代码段，把相关的代码分配到一个模块里能让你的代码更好用，更易懂。
- 模块定义好后，我们可以使用 import 语句来引入模块，语法如下：

```python

from import module1[, module2[,... moduleN]

```

 - 这行代码的意思是：我需要获得MicroPython的所有东西，我们需要“`from`(来自)”“`microbit`(模块)”的东西，具体需要“`import`(导入)”“`*`(所有文件)”
	- 总体来说：**导入MICROBIT模块所有的文件。**
	- 为了给Micro:bit上的模块编程，每一个MicroPython程序都需要导入MicroPython模块，以后用到的其他外部扩展模块也同样需要导入相应的MicroPython。

2. 第二行代码：`display.scroll("Hello, World!")`
	
	- 这样代码的意思是：“`display`(显示)”“`scroll`(滚动显示)”“`(Hello, World!)`(显示内容)”
	- 总体来说：**滚动显示“Hello, World!”。**

- MicroPython的运行方式是解释性运行，从上之下逐条运行，每一行代码都可以解释成需要完成的工作，代码简洁易懂。
- 当代码运行到最下边一条，意味着程序的结束。
- 接下来我们详细的分析代码中的每一个单词的具体用法。 


