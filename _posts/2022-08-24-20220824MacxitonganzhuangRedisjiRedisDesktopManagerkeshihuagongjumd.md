---
layout: post
title: "Mac系统安装Redis及RedisDesktopManager可视化工具
date   20240810
tags RedisRedisDesktopManager安装Mac可视化
comments true
author admin

 Mac系统安装Redis及RedisDesktopManager可视化工具

 简介
本资源文件提供了在Mac系统上安装Redis以及RedisDesktopManager可视化工具的详细步骤和配置说明通过本资源您可以轻松地在Mac系统上搭建Redis环境并使用RedisDesktopManager进行可视化管理

 安装步骤

 1 安装Homebrew
首先确保您的Mac系统上已安装Homebrew包管理工具如果没有安装请在终端中运行以下命令进行安装
bash
binbash c curl fsSL httpsrawgithubusercontentcomHomebrewinstallHEADinstallsh"
date:   2024-08-10
tags: [Redis,RedisDesktopManager,安装,Mac,可视化]
comments: true
author: admin
---
# Mac系统安装Redis及RedisDesktopManager可视化工具

## 简介
本资源文件提供了在Mac系统上安装Redis以及RedisDesktopManager可视化工具的详细步骤和配置说明。通过本资源，您可以轻松地在Mac系统上搭建Redis环境，并使用RedisDesktopManager进行可视化管理。

## 安装步骤

### 1. 安装Homebrew
首先，确保您的Mac系统上已安装Homebrew包管理工具。如果没有安装，请在终端中运行以下命令进行安装：
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### 2. 安装Redis
使用Homebrew安装Redis，运行以下命令：
```bash
brew install redis
```

### 3. 配置Redis
安装完成后，您需要对Redis进行一些基本配置：
1. 打开Finder，按下`Command + Shift + G`，输入`/usr/local/etc/`，找到并打开`redis.conf`文件。
2. 将`daemonize no`改为`daemonize yes`，使Redis以守护线程方式运行。
3. 注释掉`bind 127.0.0.1 -::1`。
4. 将`protected-mode yes`改为`protected-mode no`，关闭保护模式。
5. 设置密码：将`requirepass foobared`改为`requirepass 111`，密码设置为`111`。

### 4. 启动Redis
在终端中输入以下命令启动Redis：
```bash
redis-server /usr/local/etc/redis.conf
```
使用以下命令检查Redis是否已启动：
```bash
ps aux | grep redis
```

### 5. 安装RedisDesktopManager
下载并安装RedisDesktopManager可视化工具。安装完成后，打开RedisDesktopManager，点击左上角的 "+" 按钮创建新连接。

### 6. 配置RedisDesktopManager连接
在弹出的对话框中填写以下信息：
- Name: 连接名称，自定义。
- Address: Redis服务器地址，默认为`localhost`。
- Port: Redis服务器端口，默认为`6379`。

点击 "Test Connection" 按钮测试连接是否成功，如果成功，点击 "Save" 按钮保存连接配置。

## 使用说明
现在您已经成功安装并配置了Redis及RedisDesktopManager可视化工具，可以使用RedisDesktopManager来管理和操作您的Redis数据库。

## 注意事项
- 确保Mac系统上已安装Homebrew。
- 配置Redis时，根据实际需求调整配置文件。
- 使用RedisDesktopManager时，确保Redis服务器已启动并正确配置。

## 参考资料
本资源文件的详细步骤和配置说明参考自CSDN博客文章，作者为追着我跑的猫ღ。

## 下载链接

[Mac系统安装Redis及RedisDesktopManager可视化工具分享](https://pan.quark.cn/s/ce935496ab47)