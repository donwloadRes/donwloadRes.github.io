---
layout: post
title: "Windows 10 安装 RabbitMQ 详细步骤"
date:   2021-02-12
tags: [RabbitMQ,安装,rabbitmq,安装包,Erlang]
comments: true
author: admin
---
# Windows 10 安装 RabbitMQ 详细步骤

## 简介
本资源文件提供了在 Windows 10 操作系统上安装 RabbitMQ 的详细步骤。RabbitMQ 是一个开源的消息代理软件，广泛用于构建分布式系统和微服务架构中的消息传递。

## 安装步骤

### 第一步：下载 Erlang
1. 下载 Erlang 安装包：`otp_win64_25.0.3.exe`。
2. 双击安装包，按照默认设置一路点击“下一步”直至安装完成。
3. 默认安装路径为：`C:\Program Files\Erlang OTP\erts-13.0.3`。

### 第二步：配置 Erlang 环境变量
1. 新建系统变量：
   - 变量名：`ERLANG_HOME`
   - 变量值：`Erlang 安装路径`
2. 在系统 `Path` 变量中添加：`%ERLANG_HOME%\bin`。
3. 打开命令提示符（CMD），输入 `erl`，确认 Erlang 版本号显示，表示安装成功。

### 第三步：下载 RabbitMQ
1. 下载 RabbitMQ 安装包：`rabbitmq-server-3.10.7.exe`。
2. 双击安装包，按照默认设置一路点击“下一步”直至安装完成。
3. 默认安装路径为：`C:\Program Files\RabbitMQ Server\rabbitmq_server-3.10.7`。

### 第四步：配置 RabbitMQ
1. 打开命令提示符（CMD），进入 RabbitMQ 的 `sbin` 目录：
   - 路径：`C:\Program Files\RabbitMQ Server\rabbitmq_server-3.10.7\sbin`
2. 运行命令：`rabbitmq-plugins enable rabbitmq_management`。

### 第五步：验证安装
1. 在浏览器中访问：`http://localhost:15672`。
2. 使用默认用户名和密码 `guest` 登录，确认 RabbitMQ 管理界面正常显示。

## 基本命令
- 启动 RabbitMQ 服务：`net start RabbitMQ`
- 停止 RabbitMQ 服务：`net stop RabbitMQ`
- 查看 RabbitMQ 状态：`rabbitmqctl status`

## 异常情况处理
如果在安装过程中遇到“拒绝访问”等异常情况，请确保以管理员权限运行命令提示符，并检查环境变量配置是否正确。

## 结语
通过以上步骤，您应该能够在 Windows 10 上成功安装并配置 RabbitMQ。如果在安装过程中遇到任何问题，请参考相关文档或社区支持。

## 下载链接

[Windows10安装RabbitMQ详细步骤](https://pan.quark.cn/s/585d218116cf)