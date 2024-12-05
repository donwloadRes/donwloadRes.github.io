---
layout: post
title: "Windows 10 下 Redis 安装指南 (Redis-3.2.100 版)"
date:   2024-01-13
tags: [Redis,redis,Windows,3.2,100]
comments: true
author: admin
---
# Windows 10 下 Redis 安装指南 (Redis-3.2.100 版)

本文将详细介绍如何在 Windows 10 操作系统下安装 Redis 3.2.100 版本。Redis 是一个开源的高性能键值存储系统，常用于数据库、缓存和消息中间件。

## 1. 下载 Redis 的 Windows 版本

由于 Redis 官方不提供 Windows 版本的下载，因此我们需要从 GitHub 上获取旧版本的 Redis。以下是下载步骤：

1. 访问 GitHub 上的 Redis 仓库，找到适合 Windows 的 3.2.100 版本。
2. 下载 Redis-x64-3.2.100.zip 压缩包。

## 2. 安装步骤

### 2.1 解压文件

1. 将下载的压缩包解压到一个文件夹中，例如 `C:\redis`。

### 2.2 启动 Redis 服务

1. 打开命令提示符（快捷键：WIN键+R键，输入 `cmd` 并回车）。
2. 切换到 Redis 解压目录，例如：
   ```
   cd C:\redis
   ```
3. 输入以下命令启动 Redis 服务：
   ```
   redis-server redis.windows.conf
   ```

### 2.3 部署 Redis 为 Windows 服务

1. 关闭前面启动的 Redis 窗口。
2. 打开一个新的命令提示符窗口，切换到 Redis 解压目录。
3. 输入以下命令将 Redis 安装为 Windows 服务：
   ```
   redis-server --service-install redis.windows.conf
   ```
4. 在电脑服务中启动 Redis 服务：
   - 右击“此电脑” -> 选择“管理” -> 进入“服务和应用程序” -> 选择“服务”。
   - 找到 Redis 服务并启动。

## 3. Redis 常用指令

- 安装服务：`redis-server --service-install redis.windows.conf`
- 卸载服务：`redis-server --service-uninstall`
- 开启服务：`redis-server --service-start`
- 停止服务：`redis-server --service-stop`

## 4. 测试验证

1. 通过命令提示符进入 Redis 解压目录。
2. 输入以下命令测试 Redis 是否正常工作：
   ```
   redis-cli
   ```
3. 使用 `SET` 和 `GET` 命令验证数据存储和读取功能。

## 5. 注意事项

- Redis 常用指令需要在 Redis 安装位置（或解压包位置）处使用命令提示符执行，否则会提示不是系统命令。
- 可以通过配置环境变量的方式解决上述问题，但未验证。

通过以上步骤，您应该能够在 Windows 10 下成功安装并运行 Redis 3.2.100 版本。

## 下载链接

[Windows10下Redis安装指南Redis-3.2.100版分享](https://pan.quark.cn/s/05ab2386dc2e)