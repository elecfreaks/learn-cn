## 3.3 显示屏相关API ##
----------
### API ###
	
- 在之前 *2.4 什么是API* 小节中介绍过什么是API，MicroPython编程离不开API支持，下边就是5X5点阵显示屏可能涉及和使用到的API详细说明。

***注意：***某些方法的参数可以缺省表示。


| API | 描述 | 
| :------------: | :-----------: |
|`display.show(iterable, delay=400, wait=True, loop=False, clear=False)`|显示`iterable`中的每个图像或字母，每个显示之间延迟400ms`delay`，阻塞等待`wait`，不循环`loop`，不清屏`clear`。 |
|`display.show(image, delay=0, wait=True, loop=False, clear=False)`|显示一个内置图像`image`，每个显示之间延迟0ms`delay`，阻塞等待`wait`，不循环`loop`，不清屏`clear`。|
|`display.scroll(string, delay=400)`|在显示屏上滚动一个字符串`string`，延时`400`ms`delay`。|
|`display.get_pixel(x, y)`|获取`(x，y)`位置的亮度，亮度范围为0(关闭)到9(最亮)。
|`display.set_pixel(x, y, val)`|设置`（x，y）`位置的亮度为`val`（介于0 [关闭]和9[最亮]之间）。
|`display.clear()`|清空屏幕。|

### microbit内置图像 ###
- MicroPython中内置了很多有趣的图片，以点阵的方式显示。
- 内置的所有图形如下图所示，其英文名为图像描述。
| | | | | |
| :------------: | :-----------: | :------------: | :-----------: | :------------: |
|Image.HEART|Image.CLOCK12| Image.CLOCK11|Image.CLOCK10|Image.CLOCK9|
|Image.CLOCK8|Image.CLOCK7| Image.CLOCK6|Image.CLOCK5|Image.CLOCK4|
|Image.CLOCK3|Image.CLOCK2|Image.CLOCK1|Image.ARROW_N|Image.ARROW_NE|
|Image.ARROW_E|Image.ARROW_SE|Image.ARROW_S|Image.ARROW_SW| Image.ARROW_W| 
|Image.ARROW_NW|Image.TRIANGLE|Image.TRIANGLE_LEFT|Image.CHESSBOARD|Image.DIAMOND|
|Image.DIAMOND_SMALL|Image.SQUARE|Image.SQUARE_SMALL|Image.RABBIT|Image.COW|
|Image.MUSIC_CROTCHET|Image.MUSIC_QUAVER|Image.MUSIC_QUAVERS|Image.PITCHFORK|Image.XMAS|
|Image.PACMAN|Image.TARGET|Image.TSHIRT|Image.ROLLERSKATE|Image.DUCK|
|Image.HOUSE|Image.TORTOISE|Image.BUTTERFLY|Image.STICKFIGURE|Image.GHOST|
|Image.SWORD|Image.GIRAFFE|Image.SKULL|Image.UMBRELLA|Image.SNAKE|
|Image.HEART_SMALL |Image.HAPPY|Image.SMILE |Image.SAD |
|Image.YES |Image.NO |
