---
layout: post
title: "Windows 安装 Redis 图文详解"
date:   2024-09-09
tags: [Redis,Windows,redis,安装,命令提示符]
comments: true
author: admin
---
# Windows 安装 Redis 图文详解

## 简介

本资源文件详细介绍了如何在 Windows 系统上安装 Redis，并提供了图文并茂的步骤说明。Redis 是一个开源的高性能键值对存储数据库，广泛应用于缓存、消息队列等场景。通过本指南，您可以轻松地在 Windows 环境下完成 Redis 的安装和配置。

## 安装步骤

### 1. 下载 Redis

首先，您需要从指定的下载地址获取 Redis 的 Windows 版本压缩包。下载完成后，将其解压到一个文件夹中。

### 2. 启动 Redis 服务

1. 打开命令提示符（cmd），并导航到解压后的 Redis 文件夹。
2. 输入以下命令启动 Redis 服务：
   ```
   redis-server redis.windows.conf
   ```

### 3. 部署 Redis 服务

1. 关闭上一步中启动的 Redis 服务窗口，然后打开一个新的命令提示符窗口。
2. 输入以下命令将 Redis 部署为 Windows 服务：
   ```
   redis-server --service-install redis.windows.conf
   ```
3. 进入 Windows 服务管理界面，找到 Redis 服务并启动它。

### 4. 测试 Redis 安装

1. 打开一个新的命令提示符窗口，输入以下命令启动 Redis 客户端：
   ```
   redis-cli.exe
   ```
2. 在客户端中输入以下命令进行测试：
   ```
   set name hello
   get name
   keys *
   ```
   这些命令将设置一个键值对，获取该键的值，并列出当前数据库中的所有键。

### 5. 开启 Redis 远程访问

1. 由于 Redis 默认只允许本地访问，要使 Redis 可以远程访问，需修改 Redis 配置文件。
2. 打开 `redis.windows.conf` 文件，找到并修改以下配置：
   - 注释掉 `bind 127.0.0.1`。
   - 将 `protected-mode yes` 修改为 `protected-mode no`。
3. 保存文件并重启 Redis 服务。

## 总结

通过以上步骤，您已经成功在 Windows 系统上安装并配置了 Redis。现在，您可以开始使用 Redis 进行开发和测试了。如果在安装过程中遇到任何问题，请参考本文提供的详细步骤进行排查。

## 下载链接

[Windows安装Redis图文详解分享43107](https://pan.quark.cn/s/a09747241c05)