---
layout: post
title: "RabbitMQ 超详细安装教程"
date:   2020-05-29
tags: [RabbitMQ,安装,Erlang,安装包,双击]
comments: true
author: admin
---
# RabbitMQ 超详细安装教程

本资源文件提供了 RabbitMQ 的详细安装教程，适用于希望在自己的系统上安装和配置 RabbitMQ 的用户。以下是安装步骤的简要概述：

## 安装准备

1. **Erlang 安装**：
   - RabbitMQ 是基于 Erlang 语言开发的，因此在安装 RabbitMQ 之前，需要先安装 Erlang 环境。
   - 下载 Erlang 安装包并按照提示进行安装。

2. **RabbitMQ 安装**：
   - 下载 RabbitMQ 安装包。
   - 双击安装包进行安装，注意不要安装在包含中文和空格的目录下。

## 安装步骤

1. **安装 Erlang**：
   - 双击下载的 Erlang 安装包，按照安装向导进行安装。

2. **安装 RabbitMQ**：
   - 双击 RabbitMQ 安装包，按照向导进行安装。
   - 安装完成后，RabbitMQ 会作为一个 Windows 服务存在，并且处于启动状态。

3. **安装管理界面（插件）**：
   - 进入 RabbitMQ 安装目录的 `sbin` 目录。
   - 在命令行中输入 `rabbitmq-plugins enable rabbitmq_management` 命令，启用管理插件。

4. **重启服务**：
   - 双击 `rabbitmq-server.bat` 文件，重启 RabbitMQ 服务。

5. **访问管理界面**：
   - 打开浏览器，输入 `http://127.0.0.1:15672`，即可看到管理界面的登录页。
   - 使用默认用户名和密码 `guest` 登录。

## 注意事项

- RabbitMQ 是基于 Erlang 语言开发的，因此在安装 RabbitMQ 之前，必须先安装 Erlang 环境。
- 安装过程中，请确保所有路径不包含中文和空格，以避免安装失败。

通过以上步骤，您可以顺利完成 RabbitMQ 的安装和配置，并开始使用其强大的消息队列功能。

## 下载链接

[RabbitMQ超详细安装教程](https://pan.quark.cn/s/1e67743590e7)