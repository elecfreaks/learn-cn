# 9.3 演示案例

#### micro:bit萤火虫 ####
- 首先，它检查按钮A是否被按下，如果是，则使用无线电发送消息“flash”。
- 然后它使用`radio.receive()`从消息队列中读取任何消息。如果有消息，它会暂停一段短暂的随机时间(以使显示更有趣)，并使用`display.show()`设置动画。最后，为了让事情变成随机发生，它选择一个随机数，以便它有十分之一的机会将“flash”消息重新广播给其他人(这就是在几个设备中维持萤火虫显示的可能性)。如果它决定重新广播，那么在再次发送“闪光”信号之前等待半秒(因此初始闪光消息的显示有可能消失)。


```Python

import radio
import random

from microbit import *

flash = [Image().invert()*(i/9) for i in range(9, -1, -1)]

radio.on()

while True:
	if button_a.was_pressed():
        radio.send('flash') 

    incoming = radio.receive()

    if incoming == 'flash':
        sleep(random.randint(50, 350))
        display.show(flash, delay=100, wait=False)
        if random.randint(0, 9) == 0:
            sleep(500)
            radio.send('flash')  

```

- 使用多个micro:bit效果看起来是这样：

![](./images/ambosND.gif)
