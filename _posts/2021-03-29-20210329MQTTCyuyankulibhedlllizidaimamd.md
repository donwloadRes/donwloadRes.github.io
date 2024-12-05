---
layout: post
title: "MQTT C语言库lib和dll例子代码"
date:   2022-10-29
tags: [MQTT,paho,示例,lib,代码]
comments: true
author: admin
---
# MQTT C语言库（lib和dll）+例子代码

## 简介

本仓库提供了一个MQTT C语言库的资源文件，包括lib和dll文件，以及相关的例子代码。这些资源可以帮助开发者快速集成MQTT协议到他们的C语言项目中。

## 目录结构

```
.
├── bin
│   ├── MQTTVersion.exe
│   ├── paho-mqtt3a.dll
│   └── paho-mqtt3c.dll
├── CONTRIBUTING.md
├── edl-v10
├── epl-v10
├── include
│   ├── MQTTAsync.h
│   ├── MQTTClient.h
│   ├── MQTTClientPersistence.h
│   ├── MQTTProperties.h
│   ├── MQTTReasonCodes.h
│   └── MQTTSubscribeOpts.h
├── lib
│   ├── paho-mqtt3a.lib
│   └── paho-mqtt3c.lib
├── notice.html
├── README.md
├── samples
│   ├── MQTTAsync_publish.c
│   ├── MQTTAsync_subscribe.c
│   ├── MQTTClient_publish_async.c
│   ├── MQTTClient_publish.c
│   ├── MQTTClient_subscribe.c
│   ├── paho_c_pub.c
│   ├── paho_cs_pub.c
│   ├── paho_cs_sub.c
│   ├── paho_c_sub.c
│   └── pubsub_opts.c
└── 说明.txt
```

## 文件说明

- **bin**: 包含MQTT库的可执行文件和动态链接库（dll）。
  - `MQTTVersion.exe`: 用于查看MQTT库版本的工具。
  - `paho-mqtt3a.dll`: MQTT异步库的动态链接库。
  - `paho-mqtt3c.dll`: MQTT同步库的动态链接库。

- **include**: 包含MQTT库的头文件。
  - `MQTTAsync.h`: MQTT异步客户端的头文件。
  - `MQTTClient.h`: MQTT同步客户端的头文件。
  - `MQTTClientPersistence.h`: MQTT客户端持久化相关的头文件。
  - `MQTTProperties.h`: MQTT属性相关的头文件。
  - `MQTTReasonCodes.h`: MQTT原因码相关的头文件。
  - `MQTTSubscribeOpts.h`: MQTT订阅选项相关的头文件。

- **lib**: 包含MQTT库的静态链接库（lib）。
  - `paho-mqtt3a.lib`: MQTT异步库的静态链接库。
  - `paho-mqtt3c.lib`: MQTT同步库的静态链接库。

- **samples**: 包含MQTT库的示例代码。
  - `MQTTAsync_publish.c`: 异步发布示例代码。
  - `MQTTAsync_subscribe.c`: 异步订阅示例代码。
  - `MQTTClient_publish_async.c`: 同步发布异步示例代码。
  - `MQTTClient_publish.c`: 同步发布示例代码。
  - `MQTTClient_subscribe.c`: 同步订阅示例代码。
  - `paho_c_pub.c`: 发布示例代码。
  - `paho_cs_pub.c`: 同步发布示例代码。
  - `paho_cs_sub.c`: 同步订阅示例代码。
  - `paho_c_sub.c`: 订阅示例代码。
  - `pubsub_opts.c`: 发布订阅选项示例代码。

## 使用说明

1. **编译库文件**: 你可以使用`lib`目录下的静态链接库文件，或者使用`bin`目录下的动态链接库文件。
2. **包含头文件**: 在你的C语言项目中，包含`include`目录下的头文件。
3. **运行示例代码**: 你可以参考`samples`目录下的示例代码，了解如何使用MQTT库进行发布和订阅操作。

## 贡献

如果你有任何改进或建议，欢迎提交PR或Issue。请参考`CONTRIBUTING.md`文件了解如何贡献代码。

## 许可证

本项目遵循EPL-1.0和EDL-1.0许可证。详细信息请参考`epl-v10`和`edl-v10`文件。

## 联系

如果你有任何问题或需要帮助，请在仓库中提交Issue。

## 下载链接

[MQTTC语言库lib和dll例子代码](https://pan.quark.cn/s/0889041a0414)