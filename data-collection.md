# Data Collection

## FedCamp

#### 源码：[https://github.com/Thea-Feng/FedC.git](https://github.com/Thea-Feng/FedC.git)

#### 主要内容看Main activity，从这个文件看他调用了啥，其他不需要管；目前实现了基础UI，即用户在主界面输入信息后：1.上传数据或者获得系统参数，2.跳转到一个新的基本信息页面

使用说明

* 前置知识：安卓&网络编程
* 安卓开发：新手可以看第一行代码by guolin 前面部分是安卓MQTT编程，如果会TCP的也可以自己手写跳到任务

1. 搭建一个Apollo broker, 流程参照：[https://blog.csdn.net/weixin\_39808143/article/details/112576683](https://blog.csdn.net/weixin\_39808143/article/details/112576683) （我用的MAC，Windows也可以博客找相关教程，注意地址重映射和JAVA\_HOME路径问题，可以用教程方法检验是否成功）
2. 用Mqtt.fx / MqttX / EMqtt 检验Mqtt是否可以通信
3. 安卓Mqtt通信，可以搜索教程，网上的写法大同小异，目前的一个问题就是安卓端只能发消息不能接收(subscribe)到消息，问题是在于MainActivity.java回调函数中messageArrived没有调用成功（一个待解决bug)
   1. 任务1: 完善mqtt subscribe (publish已完成)
   2. 任务2: 完善数据库：本地用的LitePal（已实现，可以看第一行代码学）,云端可以用阿里云(支持MQTT)，学习文档，搭建控制台：[https://help.aliyun.com/document\_detail/163032.html](https://help.aliyun.com/document\_detail/163032.html)
4. 任务3: 在成功通信后完成每轮差分隐私，算法可以问我和佳琪
5. 任务4: 完善UI（简单）: 目前只有两个基础页面，需要美化+英语版供国际生使用
6. （后期）等取得权限后华为Health Kit获取数据，让用户不用手动输入，官网的教程很详细 [https://developer.huawei.com/consumer/cn/doc/development/HMSCore-Guides/apply-kitservice-0000001050071707](https://developer.huawei.com/consumer/cn/doc/development/HMSCore-Guides/apply-kitservice-0000001050071707)
7. （后期）与ML接洽
