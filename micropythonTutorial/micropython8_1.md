# 8.1 Python中的函数

- 函数是组织好的，可重复使用的，用来实现单一，或相关联功能的代码段。

- 函数能提高应用的模块性，和代码的重复利用率。你已经知道Python提供了许多内建函数，比如sleep(),max(),str()。但你也可以自己创建函数，这被叫做用户自定义函数。

### 定义一个函数 ###

- 你可以定义一个由自己想要功能的函数：

```python

def functionname( parameters ):
   "函数_文档字符串"
   function_suite
   return [expression]

```
- 函数代码块以 `def` 关键词开头，后接`函数标识符名称`“functionname”和圆括号`()`。
- 任何传入参数和自变量必须放在圆括号中间。圆括号`()`之间可以用于定义参数`parameters`。
- 函数内容以冒号起始，并且缩进。
- 函数的**第一行**语句可以选择性地使用文档字符串—用于存放**函数说明**。
- return [表达式] 结束函数，选择性地返回一个值给调用方。不带表达式的return相当于返回 None。
- 默认情况下，参数值和参数名称是按函数声明中定义的顺序匹配起来的。

```pythoh

def my_fun( par_num ):
   "判断传入参数的2倍是否大于50，如大于显示√，否则显示X"
	par_num = par_num * 2
	if par_num > 50:
		display.show(Image.YES)
	else
		display.show(Image.NO)
   return

```

### 函数的调用 ###

- 定义一个函数只给了函数一个名称，指定了函数里包含的参数，和代码块结构。

- 这个函数的基本结构完成以后，你可以通过另一个函数调用执行，也可以直接从Python提示符执行。

- 如下实例调用了上边代码块的`my_fun()`函数：

```python

def my_fun( par_num ):
   ""判断传入参数的2倍是否大于50，如大于显示√，否则显示X"
	par_num = par_num * 2
	if par_num > 50:
		display.show(Image.YES)
	else
		display.show(Image.NO)
   return
 
my_fun(20)				#调用一次函数，传入参数20
my_fun(30)				#第二次调用函数，传入参数30

```
