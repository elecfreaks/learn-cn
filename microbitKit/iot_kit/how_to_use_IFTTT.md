# 第二节：ITFFF平台操作指南

## 如何通过IFTTT发送温度阈值报警电子邮件
---
![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_ifttt_01.jpg)
在文章 如何发送Micro：bit Data到ThingSpeak IoT Platform中,我们讨论了如何使用micro：bit将数据上传到Thingspeak IoT平台。在本文中，我们将讨论如何使用IFTTT发送micro：bit温度预警邮件。
## 什么是IFTTT？ ##
IFTTT是“if this then that”的缩写。事实上，它会对您的网站行为产生一系列连锁反应，目标是“让互联网为您服务”，这将为您带来更多的使用便利。IFTTT旨在帮助人们利用不同网站的公共API，将网站（如Facebook，Twitter等）或应用程序链接在一起，以完成您的任务。因此，每个人都可以成为整个互联网的程序员而无需编写程序。IFTTT通过流程连接各种信息，然后集中呈现您所需的信息，解决杂项信息的问题，接收或关注重要信息。根据IFTTT，“this”的操作被称为“触发器”，也就是说你在某个网站上的行为; 而“那”意味着由连锁反应引起的另一种行为“行为”。这些触发器和操作都基于某个网站，在IFTTT中称为“渠道”。整个“if this then that”动作被定义为“任务”。让我用一个例子向你解释一下。在IFTTT中，用户可以通过创建和实现“任务”来实现网站连锁反应。例如，如果您刚刚使用micro：bit将温度数据上传到Thingspeak，当温度达到阈值时，它将激活触发器以执行您指定的操作：向您的邮箱发送电子邮件。
通过IFTTT发送micro：bit温度报警电子邮件
首先，请确保您已成功将温度数据从micro：bit上传到Thingspeak。如果您不知道如何操作，可以阅读本文 如何将Micro：bit Data发送到ThingSpeak IoT Platform 以获取帮助。  

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_ifttt_02.png)

## 第1步：注册IFTTT帐户
---
登录IFTTT。如果您还没有帐户，请先注册一个帐户。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_ifttt_03.png)

## 第2步：IFTTT Webhooks设置
---
创建一个Applet。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_ifttt_04.png)

点击“这个”。 

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_ifttt_05.png)

搜索“webhooks”。 

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_ifttt_06.png)

选择触发器。 

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_ifttt_07.png)

命名此任务。这里我们称之为“microbit_temperature_alarm”。 

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_ifttt_08.png)

完成触发设置后，单击“那个”。 

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_ifttt_09.png)

搜索“电子邮件”。 

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_ifttt_10.png)

填写您的电子邮件内容并注意显示的格式，其中{{}}允许我们从Web请求中提取具有相同名称的数据，然后将其转发到电子邮件中。

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_ifttt_11.png)

已完成。 

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_ifttt_12.png)

单击“文档”。 

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_ifttt_13.png)

此链接是Web请求的链接。这在后来的Thingspeak设置中非常重要。 


![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_ifttt_14.png)

## 第3步：Thingspeak设置
---
在此之前，您必须将温度数据从micro：bit上传到Thingspeak。如果您不知道如何操作，请阅读本文 如何将Micro：bit Data发送到ThingSpeak IoT平台 以获取帮助。首先，创建一个新的ThingHTTP服务。 

![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_ifttt_15.png)

这是与IFTTT连接的设置：

 ![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_ifttt_16.png)

注意：
URL是Web请求的链接，其必须包含IFTTT提供的私钥。
内容类型必须是JSON，因为IFTTT Maker Channel的预期格式是JSON。
在Body中，您可以调用Channel中的任何数据。这是将发送到IFTTT的数据，格式如下：{“value1”：“%% channel_138112_field_1 %%”}
有关ThingHTTP应用程序的更多详细信息，请参阅:[//ww2.mathworks.cn/help/thingspeak/thinghttp-app.html](https://ww2.mathworks.cn/help/thingspeak/thinghttp-app.html). 最后，创建一个React服务。 

 ![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_ifttt_17.png)

以下是设置：测试通道400589（不同的帐户有不同的通道，请将其更改为您自己的通道）以查看温度值是否高于30.如果是，则触发ThingHTTP中的temperature_alarm服务。

 ![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_ifttt_18.png)
case_ifttt_04
有关React APP的更多详细信息，请参阅 [https://ww2.mathworks.cn/help/thingspeak/react-app.html](https://ww2.mathworks.cn/help/thingspeak/react-app.html).
### 第4步：测试
到此步骤，您已完成所有设置。现在让我们来测试吧！如果温度尚未达到30度，您可以用手握住micro：bit来提高温度。
 
 ![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_ifttt_18.png)

我们可以从Thingspeak频道的数据中看到温度超过30m度。  

 ![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_ifttt_19.png)

检查您的电子邮箱，看看您是否收到了IFTTT的电子邮件！ 

 ![](https://raw.githubusercontent.com/elecfreaks/learn-cn/master/microbitKit/iot_kit/images/case_ifttt_20.png)

