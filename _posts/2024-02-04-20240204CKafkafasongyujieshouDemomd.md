---
layout: post
title: "C Kafka 发送与接收 Demo"
date:   2024-03-26
tags: [Kafka,string,using,C#,Confluent]
comments: true
author: admin
---
# C# Kafka 发送与接收 Demo

## 概述

本仓库提供了一个完整的C#示例，用于演示如何使用Kafka进行消息的发送与接收。Kafka是一个分布式的、高吞吐量的消息系统，广泛应用于大数据处理和实时数据管道中。通过这个Demo，开发者可以快速上手C#环境下Kafka的基本应用，包括生产者如何发布消息到主题（topic）以及消费者如何订阅并消费这些消息。

## 技术栈

- **编程语言**：C#
- **库依赖**：推荐使用Confluent.Kafka，这是一个广受欢迎的Kafka客户端库，支持.NET。
- **Kafka版本**：确保所使用的Kafka服务器版本与客户端库兼容。
- **开发环境**：适用于任何支持.NET Core或.NET Standard的平台。

## 快速入门

### 安装必要的NuGet包

首先，你需要在你的项目中安装`Confluent.Kafka` NuGet包。可以通过Visual Studio的管理NuGet包功能或者命令行使用以下命令：

```sh
dotnet add package Confluent.Kafka
```

### 发送消息

示例代码展示了如何创建一个Kafka生产者并发送消息到指定的主题。

```csharp
using System;
using Confluent.Kafka;

class ProducerExample {
    static void Main(string[] args) {
        var config = new ProducerConfig { BootstrapServers = "localhost:9092" };
        using (var producer = new ProducerBuilder<string, string>(config).Build()) {
            producer.ProduceAsync("your-topic", new Message<string, string> { Value = "Hello, Kafka!" });
            Console.WriteLine("Message sent.");
            producer.Flush();
        }
    }
}
```

### 接收消息

同样地，这里展示的是如何创建一个Kafka消费者来订阅并读取消息。

```csharp
using System;
using Confluent.Kafka;

class ConsumerExample {
    static void Main(string[] args) {
        var config = new ConsumerConfig {
            BootstrapServers = "localhost:9092",
            GroupId = "my-group",
            AutoOffsetReset = AutoOffsetReset.Earliest
        };

        using (var consumer = new ConsumerBuilder<string, string>(config)
                                  .Configure(c => c.Logger += (_, m) => Console.WriteLine($"{m.LogLevel} at {DateTime.Now}: {m.Message}"))
                                  .Build()) {

            consumer.Subscribe("your-topic");

            while (true) {
                var consumeResult = consumer.Consume(TimeSpan.FromSeconds(1));
                if (consumeResult.IsPartitionEOF)
                    continue;
                Console.WriteLine($"Consumed message '{consumeResult.Value}' at: '{consumeResult.Offset}'.");
            }

        }
    }
}
```

## 注意事项

- 确保Kafka服务正在运行，并且配置中的BootstrapServers指向正确的地址和端口。
- 更复杂的用例，如错误处理、消息确认等，在实际应用中需要进一步考虑。
- 对于生产环境，应详细配置消费者组、分区分配策略等以满足特定需求。

这个简单的Demo仅为入门级示例，深入学习Kafka与C#的集成时，建议查阅官方文档及更详细的教程。

## 下载链接

[CKafka发送与接收Demo](https://pan.quark.cn/s/e4a19822c508)