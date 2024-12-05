---
layout: post
title: "Ubuntu 2004 离线安装 RabbitMQ 指南"
date:   2024-07-18
tags: [RabbitMQ,安装,Erlang,离线,Ubuntu]
comments: true
author: admin
---
# Ubuntu 20.04 离线安装 RabbitMQ 指南

欢迎来到 Ubuntu 20.04 系统下离线安装 RabbitMQ 的教程。本仓库提供了包含 Erlang 和其他必要的依赖包，以帮助您在没有互联网连接的情况下顺利完成 RabbitMQ 的安装。RabbitMQ 是一个广泛使用的开源消息队列系统，基于 AMQP（高级消息队列协议）。Erlang 则是其运行所需的编程语言环境。

## 离线安装步骤

### 准备阶段

1. **下载资源**：首先从本仓库下载提供的 ubuntu20.04 离线安装包，其中包含了 Erlang 安装包和其他所需依赖。
   
2. **传输文件**：将下载的文件通过USB驱动器、网络共享或其他离线方式传输到您的Ubuntu 20.04服务器或桌面系统上。

### 步骤一：安装 Erlang

1. **解压 Erlang 包**：找到并解压缩下载的Erlang包，通常命令为 `tar -xzf erlang*.tgz`。
2. **配置与安装**：进入解压后的目录，执行 `./configure`，然后 `make`，最后需要 root 权限执行 `sudo make install`。

### 步骤二：安装 RabbitMQ

1. **下载并安装 RabbitMQ**：若包中包含RabbitMQ直接安装文件，则同样解压后根据说明进行安装；否则，可能需要手动下载RabbitMQ的预编译包或通过已准备的脚本安装。
   
2. **设置环境变量**：Erlang安装后，可能需要将 `ERL_ROOTDIR` 或相关路径添加到环境变量中。可以编辑 `.bashrc` 或 `.profile` 文件，并加入如下行：
   ```
   export ERLANG_HOME=/path/to/your/erlang/installation
   export PATH=$ERLANG_HOME/bin:$PATH
   ```

3. **安装 RabbitMQ 服务**：使用命令 `sudo dpkg -i rabbitmq-server*.deb` 或相应的方式安装RabbitMQ Deb包。

### 步骤三：启动与验证

1. **启动 RabbitMQ**：输入命令 `sudo systemctl start rabbitmq-server` 启动服务。
2. **检查状态**：运行 `sudo systemctl status rabbitmq-server` 以确认RabbitMQ是否成功启动。
   
如果一切顺利，您现在应该已经在 Ubuntu 20.04 上成功安装了 RabbitMQ，可以在无网络环境下使用这一消息中间件了。

请注意，这个指南是一个简化的流程，具体操作时可能需要根据实际情况调整。确保在每一步执行前阅读对应软件的官方文档，以获取最新的安装指示和最佳实践。

## 下载链接

[Ubuntu20.04离线安装RabbitMQ指南](https://pan.quark.cn/s/e00b66978bc3)