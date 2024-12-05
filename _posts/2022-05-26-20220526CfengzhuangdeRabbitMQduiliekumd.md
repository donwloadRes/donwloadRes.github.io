---
layout: post
title: "C封装的RabbitMQ队列库
date   20230404
tags RabbitMQ队列rabbitMQService模式RabbitMQService
comments true
author admin

 C封装的RabbitMQ队列库

 简介
本仓库提供了一个使用C封装的RabbitMQ队列库支持工作队列模式和发布订阅模式通过配置文件中的RabbitMQ服务器相关信息您可以轻松地在项目中引用封装好的RabbitMQService类库从而方便地操作RabbitMQ的工作队列模式和发布订阅模式

 功能特点
 工作队列模式支持多消费者处理任务实现负载均衡
 发布订阅模式支持消息广播多个消费者可以同时接收消息
 配置简单只需在配置文件中设置RabbitMQ服务器信息即可快速集成到项目中

 使用方法
1 配置RabbitMQ服务器信息
   在项目的配置文件如appsettingsjson中添加RabbitMQ服务器的相关配置信息例如
   json
   
     RabbitMQ 
       HostName localhost
       Port 5672
       UserName guest
       Password guest"
date:   2023-04-04
tags: [RabbitMQ,队列,rabbitMQService,模式,RabbitMQService]
comments: true
author: admin
---
# C#封装的RabbitMQ队列库

## 简介
本仓库提供了一个使用C#封装的RabbitMQ队列库，支持工作队列模式和发布订阅模式。通过配置文件中的RabbitMQ服务器相关信息，您可以轻松地在项目中引用封装好的RabbitMQService类库，从而方便地操作RabbitMQ的工作队列模式和发布订阅模式。

## 功能特点
- **工作队列模式**：支持多消费者处理任务，实现负载均衡。
- **发布订阅模式**：支持消息广播，多个消费者可以同时接收消息。
- **配置简单**：只需在配置文件中设置RabbitMQ服务器信息，即可快速集成到项目中。

## 使用方法
1. **配置RabbitMQ服务器信息**：
   在项目的配置文件（如`appsettings.json`）中添加RabbitMQ服务器的相关配置信息，例如：
   ```json
   {
     "RabbitMQ": {
       "HostName": "localhost",
       "Port": 5672,
       "UserName": "guest",
       "Password": "guest"
     }
   }
   ```

2. **引用RabbitMQService类库**：
   在您的项目中引用本仓库提供的`RabbitMQService`类库。

3. **初始化RabbitMQ服务**：
   在代码中初始化RabbitMQ服务，并根据需要选择工作队列模式或发布订阅模式进行操作。

   ```csharp
   var rabbitMQService = new RabbitMQService(configuration);
   rabbitMQService.Initialize();
   ```

4. **发送和接收消息**：
   根据业务需求，使用`RabbitMQService`类库提供的方法发送和接收消息。

   ```csharp
   // 发送消息到工作队列
   rabbitMQService.SendToWorkQueue("queueName", "message");

   // 发送消息到发布订阅模式
   rabbitMQService.SendToPublishSubscribe("exchangeName", "message");

   // 接收工作队列消息
   rabbitMQService.ReceiveFromWorkQueue("queueName", message => {
       // 处理消息
   });

   // 接收发布订阅模式消息
   rabbitMQService.ReceiveFromPublishSubscribe("exchangeName", "queueName", message => {
       // 处理消息
   });
   ```

## 注意事项
- 确保RabbitMQ服务器已正确安装并运行。
- 配置文件中的RabbitMQ服务器信息需与实际环境一致。
- 在使用发布订阅模式时，确保交换机和队列已正确配置。

## 贡献
欢迎提交Issue和Pull Request，共同完善本RabbitMQ队列库。

## 许可证
本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 下载链接

[C封装的RabbitMQ队列库](https://pan.quark.cn/s/15b39bb31684)