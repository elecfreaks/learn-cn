# 7.4 演示案例

### 占卜8号球 ###

- 占卜8号球，向它问一个问题，然后摇动它，点阵显示屏显示出它的答案。

```python

from microbit import *
import random

answers = [
    "It is certain",			#当然了
	"It is decidedly so",		#绝对是这样
    "Without a doubt",			#毫无疑问
    "Yes, definitely",			#是的，当然
    "You may rely on it",		#你可能会依靠它
    "As I see it, yes",			#在我看来是的
    "Most likely",				#很有可能
    "Outlook good",				#看起来不错
    "Yes",						#是的
    "Signs point to yes",		#结果指向正确
    "Reply hazy try again",		#不太清楚再来一次
    "Ask again later",			#稍后再问一次
    "Better not tell you now",	#最好先不告诉你
    "Cannot predict now",		#现在还不能预测
    "Concentrate and ask again",#集中注意力再问一次
    "Don't count on it",		#别指望了
    "My reply is no",			#我的回答是 不
    "My sources say no",		#我的占卜结果说 不
    "Outlook not so good",		#看起来不太好
    "Very doubtful",			#充满疑惑
]

while True:
    display.show('8')
    if accelerometer.was_gesture('shake'):
        display.clear()
        sleep(1000)
        display.scroll(random.choice(answers))
    sleep(10)

```

***温馨提示：***由于中文编码问题，现在micro:bit主板还不能显示中文。
