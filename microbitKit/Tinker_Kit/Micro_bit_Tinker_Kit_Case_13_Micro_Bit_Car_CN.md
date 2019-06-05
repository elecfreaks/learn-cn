# 课程_13 micro:bit小车

一起来动动手制作一个属于你的micro:bit自驱车吧！ 
(说明:这只是小车自己驱动就和一块石头自己从山顶滚下来一样 。)


## 制作目标
---

1.学习Micro:bit、扩展板以及舵机的使用； 
2.认识舵机以及如何搭配micro:bit、扩展板和Makecode一起使用； 
3.了解这个神奇的小车是如何制作出来的。

备注: 
此项目使用了一些Tinker Kit里面没有的元器件。 
(请继续关注我们官网的小车套件的更新吧！)


## Materials
---

- 1 x BBC micro:bit
- 1 x USB线
- 1 x 电池盒
- 2 x AA电池
- 1 x 扩展板
- 2 x 舵机
- 1 x 亚克力车身
- 2 x 车轮
- 1 x 毛毡垫
- 胶布

![](./images/adwP5Zd.jpg)
![](./images/vAquseh.jpg)

**温馨提示: 如果你想要以上所有这些元器件，你可以购买我们的[micro:bit小小发明家套件](https://item.taobao.com/item.htm?spm=a230r.7195193.1997079397.9.z3IMPf&id=564707672256&abbucket=5)。** 


## 制作过程
---

### 步骤 1  

如图所示，将你的小车的各个部件组装好。  
如果你使用的是我们的小车套件，请按照车身上的标签正确插入各个部件，并用胶布固定住。  
将舵机连接至扩展板上的引脚P0和P1.  
注意普通舵机的线的颜色并不一定和扩展板上的黄、红、黑颜色一致。将橙色的舵机线插入黄色的引脚，棕色的线插入黑色的引脚。  

![](./images/ip1yXX6.jpg)
![](./images/GW3ty3N.jpg)
![](./images/YgZeCEN.jpg)
![](./images/raPJYlm.jpg)


### 步骤 2  

将显示的积木块添加至On Start积木块。  
为什么要这么做呢？因为在启动的时候，我们需要把舵机调整成固定角度。  
在MakeCode里面的舵机积木块（红色）取0到180的值。你可以在Advanced下面的pins里面找到舵机的积木块。  
我们使用的360舵机，如果取值90，则刚好转动至中间。 换句话说，我们这时正在告诉舵机“保持不动”。  
我们将代码下载到micro:bit时会显示一个图像，通知你代码已经下载完成了。   


### 步骤 3  

现在让车轮动起来吧！添加右侧Foever积木块中显示的代码。  
你在Advanced项下的pins里面还可以找到Digital Write Pin to 0 这个积木块。  
这里会发生什么呢？我们正在让舵机顺时针旋转180度，并且让另外一个舵机停止转动。 然后，短暂停顿之后，我们让前面的舵机停止转动，并且让后面的舵机逆时针旋转0度。记住，90度是前进！  
为什么我们需要让一个舵机在某个时间停止转动呢？这是因为电池供电要求，micro:bit一次只能驱动一个电机。如果你有兴趣的话，你可以用一个直流电机和一个外接电源试试看。或者你也可以给我们来信获取更多解决方案!  
检查舵机的旋转方向，确保舵机的转动方向都是正确的。通过切换0和180的值，你就可以改变电机的前进方向。  

![](./images/iy5uy4V.jpg)  

如果你不想自己亲手编写代码，你可以通过下面这个链接直接下载程序的完整代码：

[https://makecode.microbit.org/_Ef87EJAepcve](https://makecode.microbit.org/_Ef87EJAepcve)

或者，你也可以从下面这个页面下载：

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_Ef87EJAepcve" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>


### 成功!  

当你准备让你的小车跑起来的时候，把电池装上，然后你的小车就能跑起来了。此外，你也可以添加一些工艺材料，改变小车的空气动力属性，让你的小车更加个性化!为了进一步扩展，你也可以连接ADKeypad来手动控制电机，而不是让小车自动跑起来。

## 常见问题
---