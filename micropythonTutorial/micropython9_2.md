# 9.2 无线电相关API

- 无线电模块允许设备通过简单的无线网络协同工作。
- 无线电在概念上非常简单：
	1. 广播发射的消息具有一定的可配置长度(最多251个字节)。
	2. 从可配置长度的消息队列中接受消息(队列越大，使用的RAM越多)。
	3. 如果队列已满，则会忽略新消息，读取消息会将其在队列中删除。
	4. 广播时设置一个广播功率，功率越大接受范围越大。
	5. 接收时按地址和组进行过滤。
	6. 发送和接受字节来处理任意数据。
	7. 使用`receive_full`获取传入消息的完整信息包括：消息数据、信号强度和时间。
	8. 为了方便初学者使用，无线电可以使用字符串的形式发送和接受消息。
	9. 默认配置兼容其他micro:bit平台。
- 想要使用无线电模块，请在程序开头使用`import radio`导入无线电模块。

### 无线电API ###

| API | 描述 | 
| :------------: | :-----------: |
|`radio.on()`|打开无线电，这需要明确使用，因为无线电消耗很多功率并且占用你可能需要使用的内存。|
|`radio.off()`|关闭无线电，以节约点亮和内存。|
|`radio.reset()`|将设置重置为其默认值（如下面配置功能的文档中所列）。|
|在收音机打开之前，以下所有发送或接收方法都不起作用。|------------------|
|`radio.send_bytes(message)`|发送包含字节的消息。|
|`radio.receive_bytes()`|接收消息队列中的下一个传入消息。 如果没有待处理消息，则返回None。 消息以字节形式返回。|
|`radio.receive_bytes_into(buffer)`|接收消息队列中的下一个传入消息。 将消息复制到缓冲区中，必要时修剪消息的结尾。 如果没有消息，则返回None，否则返回消息的长度（可能超过缓冲区的长度）。
|`radio.send(message)`|发送消息字符串。 这相当于send_bytes(bytes(message，'utf8'))，但b'\ x01 \ x00 \ x01'前置于消息队列前面(使其与其他以micro：bit为目标的平台兼容)。|
|`radio.receive()`|与`receive_bytes()`工作方式相同，它的返回值等同于`str(receive_bytes(), 'utf8')`,但检查前三个字节是b'\ x01 \ x00 \ x01'(以使其与micro的其他平台兼容)。 在转换为字符串之前剥离前置字节。如果转换为字符串失败，则会引发`ValueError`异常。|
|`radio.receive_full()`|返回一个元组，其中包含三个值，表示消息队列中的下一个传入消息。 如果没有待处理消息，则返回None。 元组中的三个值表示：消息队列中的下一个传入消息为字节。 RSSI（信号强度）：以dBm为单位测量的0（最强）和-255（最弱）之间的值。 时间戳：收到消息时time.ticks_us()返回的值。|
|`radio.config(**kwargs)`|配置与无线电相关的各种设置，其默认值如下。|

- `length`(默认值= 32)定义通过无线电发送的消息的最大长度(以字节为单位)。它最长可达251个字节(S0，LENGTH和S1前导码为254-3个字节)。

- `queue`(默认值= 3)指定可以存储在传入消息队列中的消息数。如果队列中没有剩余空间用于传入消息，则丢弃传入消息。

- `channel`(默认值= 7)可以是0到83(含)的整数值，它定义了无线电调谐到的任意“通道”。消息将通过此通道发送，只有通过此通道接收的消息才会被放入传入消息队列。每个步长为1MHz宽，基于2400MHz。

- `power`(默认值= 6)是0到7(含)的整数值，表示广播消息时使用的信号强度。值越高，信号越强，但设备消耗的功率越多。编号转换为以下dBm(分贝毫瓦)值：-30，-20，-16，-12，-8，-4,0,4。

- `address`(默认值= 0x75626974)是一个任意名称，表示为32位地址，用于过滤硬件级别的传入数据包，仅保留与您设置的地址匹配的数据包。其他micro：bit相关平台使用的默认设置是此处使用的默认设置。

- `group`(默认值= 0)是一个8位值(0-255)，用于过滤消息时的地址。从概念上讲，“地址”就像是一个住宅/办公室地址，而“组”就像您要将消息发送到该地址的人。

- `data_rate`(default = radio.RATE_1MBIT)表示数据吞吐量发生的速度。可以是无线电模块中定义的以下容量之一：
	1. |`radio.RATE_250KBIT`|常量用于表示每秒256 Kbit的吞吐量。|
	2. |`radio.RATE_1MBIT`|常量用于表示每秒1 MBIT的吞吐量。|
	3. |`radio.RATE_2MBIT`|常量用于表示每秒2 MBIT的吞吐量。|

- 如果未调用config，则使用上述默认值。
