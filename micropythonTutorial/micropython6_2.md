# 6.2 播放内置音乐

- 要知道编写一首音乐是很难的，MicroPython中内置了许多好听的音乐，你可以直接调用他们直接播放。
- 要使用micro:bit中的音乐属性和方法，需要额外导入`music`模块，关于模块详见2.2。
### 播放相关API ###

| API | 描述 | 
| :------------: | :-----------: |
|`music.play(music，pin = microbit.pin0，wait = True，loop = False)`|播放定义的音乐。如果是一个字符串，则应该是单个音符，如果为音符列表，则将它们一个接一个播放。|
|`music.pitch(frequency, len=-1, pin=microbit.pin0, wait=True)`|以给定指定毫秒数的整数频率播放一个音调。|
|`music.stop(pin=microbit.pin0)`|停止给定引脚上的所有音乐播放。|
|`music.reset()`|以下列数据`ticks = 4,bpm = 120,duration = 4,octave = 4`重启播放|
|`music.set_tempo(ticks=4, bpm=120)`|设置每分钟总节拍数`bpm`和节拍`ticks`|
|`music.get_tempo()`|获取总节拍数和节拍存放到元组中|




### 内置音乐 ###

|  |  | 
| :------------: | :-----------: |
|DADADADUM|贝多芬第五交响曲C小调的开场白。 |
|ENTERTAINER|Scott Joplin的Ragtime经典歌剧“The Entertainer”的开场片段。 |
|PRELUDE|J.S.Bach的48首前奏曲和赋格曲中第一首C大调的开头。 |
|ODE|来自贝多芬D小调第九交响曲的“欢乐颂”主题。 |
|NYAN|Nyan Cat主题（http://www.nyan.cat/）。作曲家不详。 |
|RINGTONE|听起来像手机铃声的东西。用于指示传入消息。 |
|FUNK|为秘密特工和犯罪主谋提供的时髦低音系列。|
|BLUES|一种boogie-woogie 12杆蓝调步行低音。|
|BIRTHDAY|“生日快乐......”版权状态见：http：//www.bbc.co.uk/news/world-us-canada-34332853 |
|WEDDING|来自瓦格纳歌剧“Lohengrin”的新娘合唱团。 |
|FUNERAL|“葬礼进行曲”，也被称为FrédéricChopin的钢琴奏鸣曲第2号B-minor，Op。 35. |
|PUNCHLINE|一个有趣的片段，表示一个笑话。|
|PYTHON| John Philip Sousa的游行“自由钟”又称“Monty Python's Flying Circus”的主题（之后以Python编程语言命名）。 |
|BADDY| 沉默的电影时代入口的一个坏人。 |
|CHASE| 无声电影时代的追逐场景。 |
|BA_DING|表示发生了某些事情的短信号。 |
|WAWAWAWAA|一个非常悲伤的长号。|
|JUMP_UP|用于游戏，表示向上移动。|
|JUMP_DOWN|用于游戏，表示向下移动。|
|POWER_UP|表示解锁成就的大张旗鼓。|
|POWER_DOWN|表示失去成就的悲伤声。|
