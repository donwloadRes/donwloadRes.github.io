---
layout: post
title: "Windows 安装 Redis图文详解"
date:   2023-06-02
tags: [Redis,redis,Windows,server,cmd]
comments: true
author: admin
---
# Windows 安装 Redis（图文详解）

本文详细介绍了在 Windows 系统上安装 Redis 的步骤，并提供了图文并茂的说明，帮助用户轻松完成 Redis 的安装和配置。

## 一、Redis 简介

Redis 是一个开源的、高性能的键值存储系统，广泛应用于缓存、消息队列等场景。它支持多种数据结构，如字符串、哈希、列表、集合和有序集合，并提供了多种语言的 API。

## 二、安装步骤

### 1. 下载 Redis

首先，从 GitHub 或百度网盘下载 Redis 的 Windows 版本压缩包。

### 2. 解压文件

将下载的压缩包解压到一个文件夹中，例如 `F:\Redis-x64-3.2.100`。

### 3. 启动 Redis 服务

打开命令提示符（cmd），进入解压后的文件夹，输入以下命令启动 Redis 服务：

```cmd
cd F:\Redis-x64-3.2.100
redis-server redis.windows.conf
```

### 4. 部署 Redis 服务

为了方便管理，可以将 Redis 部署为 Windows 服务。首先关闭上一个打开的窗口，然后打开一个新的命令提示符窗口，输入以下命令：

```cmd
redis-server --service-install redis.windows.conf
```

### 5. 启动 Redis 服务

进入 Windows 服务管理界面，找到 Redis 服务并启动它。

### 6. 测试 Redis 安装

打开命令提示符，输入以下命令测试 Redis 是否安装成功：

```cmd
redis-cli.exe
set name hello
get name
keys *
```

如果命令执行成功，说明 Redis 安装配置完成。

## 三、Redis 开启远程访问

默认情况下，Redis 只允许本地访问。如果需要远程访问，需修改 Redis 配置文件 `redis.windows.conf`，具体步骤如下：

1. 注释掉本地连接对应的 `bind 127.0.0.1`。
2. 将 `protected-mode yes` 修改为 `protected-mode no`。

修改完成后，保存文件并重启 Redis 服务。

## 四、常见命令

- 卸载服务：`redis-server --service-uninstall`
- 开启服务：`redis-server --service-start`
- 停止服务：`redis-server --service-stop`

通过以上步骤，您可以在 Windows 系统上成功安装并配置 Redis，并实现远程访问。

## 下载链接

[Windows安装Redis图文详解分享](https://pan.quark.cn/s/5b80c6ad6ce5)