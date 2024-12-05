---
layout: post
title: "Windows 安装Redis7.4版本图文教程"
date:   2022-10-30
tags: [Redis,redis,安装,Windows,7.4]
comments: true
author: admin
---
# Windows 安装Redis7.4版本图文教程

本教程详细介绍了如何在Windows操作系统上安装Redis 7.4版本，并将其配置为服务以实现开机自启动。通过本教程，您可以轻松地在Windows环境中部署Redis，并确保其稳定运行。

## 目录
1. [下载安装包](#下载安装包)
2. [安装步骤](#安装步骤)
3. [设置环境变量](#设置环境变量)
4. [验证结果](#验证结果)
5. [启动/关闭/删除Redis服务命令](#启动关闭删除redis服务命令)

## 下载安装包
首先，您需要下载Redis 7.4版本的安装包。可以通过以下链接获取安装包：

[Redis-7.4.0-Windows-x64-cygwin-with-Service.zip](https://pan.baidu.com/s/1NFGXrCwumDzlhBd9dnlbUQ)

提取码：32j7

## 安装步骤
1. 将下载的安装包解压到系统上的某个位置。
2. 进入解压目录，找到`install_redis_service.bat`文件。
3. 右键以管理员身份运行`install_redis_service.bat`。

## 设置环境变量
为了在电脑上的任何位置使用Redis相关命令，您需要将Redis的安装目录路径添加到系统环境变量PATH中。

## 验证结果
安装完成后，您可以通过以下命令验证Redis是否成功安装并运行：

```bash
redis-cli ping
```

如果返回`PONG`，则表示Redis已成功安装并运行。

## 启动/关闭/删除Redis服务命令
以下所有命令都需要在管理员权限下执行，否则会报权限不足。

### 启动Redis服务
```bash
net start redis
```

### 关闭Redis服务
```bash
net stop redis
```

### 删除Redis服务
```bash
sc delete redis
```

通过以上步骤，您应该能够顺利在Windows系统上安装并配置Redis 7.4版本。如果在安装过程中遇到任何问题，请参考官方文档或相关社区寻求帮助。

## 下载链接

[Windows安装Redis7.4版本图文教程](https://pan.quark.cn/s/53f11593ffc7)