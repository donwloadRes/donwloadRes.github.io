---
layout: post
title: "Windows 版本 RabbitMQ 安装包"
date:   2021-07-30
tags: [RabbitMQ,3.9,rabbitmq,插件,Erlang]
comments: true
author: admin
---
# Windows 版本 RabbitMQ 安装包

## 资源描述

本仓库提供了一个适用于 Windows 系统的 RabbitMQ 安装包，包含以下内容：

- **rabbitmq-server-3.9.13.exe**: RabbitMQ 服务器的安装程序。
- **otp_win64_24**: 包含 Erlang 运行时环境的安装包，RabbitMQ 依赖于 Erlang 运行时。
- **rabbitmq_delayed_message_exchange-3.9.0.ez**: RabbitMQ 的延迟消息交换插件，允许消息在指定时间后发送。

## 安装步骤

1. **安装 Erlang 运行时**:
   - 运行 `otp_win64_24` 文件夹中的安装程序，按照提示完成 Erlang 运行时的安装。

2. **安装 RabbitMQ 服务器**:
   - 运行 `rabbitmq-server-3.9.13.exe`，按照提示完成 RabbitMQ 服务器的安装。

3. **启用延迟消息交换插件**:
   - 将 `rabbitmq_delayed_message_exchange-3.9.0.ez` 文件复制到 RabbitMQ 的插件目录（通常位于 `C:\Program Files\RabbitMQ Server\rabbitmq_server-3.9.13\plugins`）。
   - 打开命令提示符，导航到 RabbitMQ 的安装目录，运行以下命令启用插件：
     ```
     rabbitmq-plugins enable rabbitmq_delayed_message_exchange
     ```

4. **启动 RabbitMQ 服务**:
   - 在命令提示符中运行以下命令启动 RabbitMQ 服务：
     ```
     net start RabbitMQ
     ```

## 注意事项

- 确保在安装 RabbitMQ 之前已经安装了 Erlang 运行时环境。
- 安装过程中请确保网络连接正常，以便下载必要的依赖项。
- 如果遇到任何问题，请参考 RabbitMQ 官方文档或社区支持。

## 版本信息

- RabbitMQ 版本: 3.9.13
- Erlang 版本: 24
- 延迟消息交换插件版本: 3.9.0

## 更新日志

- **2023-10-01**: 初始版本发布，包含 RabbitMQ 3.9.13 安装包及相关插件。

## 联系我们

如有任何问题或建议，请通过 GitHub 仓库的 Issues 页面联系我们。

## 下载链接

[Windows版本RabbitMQ安装包](https://pan.quark.cn/s/95876314032b)