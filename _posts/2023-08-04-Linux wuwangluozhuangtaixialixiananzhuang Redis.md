---
layout: post
title: "Linux 无网络状态下离线安装 Redis"
date:   2024-08-21
tags: [redis,rpm,Redis,local,usr]
comments: true
author: admin
---
# Linux 无网络状态下离线安装 Redis

## 简介

本资源文件提供了在Linux无网络状态下离线安装Redis的详细步骤和所需文件。通过本指南，您可以在没有互联网连接的环境中成功安装和配置Redis。

## 安装步骤

### 1. 准备安装包

在开始安装之前，您需要准备好以下文件：
- Redis安装包：`redis-7.0.2.tar.gz`
- GCC依赖包：`gcc系列依赖包`

### 2. 上传文件

使用FTP工具或Xftp工具将上述文件上传到Linux服务器的`/usr/local`目录下。

### 3. 解压安装包

进入`/usr/local`目录，并解压Redis安装包：
```bash
cd /usr/local
tar -zxvf redis-7.0.2.tar.gz
```

### 4. 安装GCC

如果系统中没有安装GCC，请按照以下步骤安装GCC依赖包：
```bash
cd /usr/local
rpm -ivh mpfr-3.1.1-4.el7.x86_64.rpm
rpm -ivh libmpc-1.0.1-3.el7.x86_64.rpm
rpm -ivh kernel-headers-3.10.0-957.12.2.el7.x86_64.rpm
rpm -ivh glibc-headers-2.17-260.el7.x86_64.rpm
rpm -ivh glibc-devel-2.17-260.el7.x86_64.rpm
rpm -ivh cpp-4.8.5-36.el7.x86_64.rpm
rpm -ivh gcc-4.8.5-36.el7.x86_64.rpm
```

### 5. 编译和安装Redis

进入Redis目录并进行编译和安装：
```bash
cd redis-7.0.2
make
cd src
make install
```

### 6. Redis配置

编辑Redis配置文件`redis.conf`，进行必要的配置：
```bash
vim redis.conf
```
- 注释掉`bind 127.0.0.1 -::1`，允许远程访问。
- 将`protected-mode`设置为`no`。
- 将`daemonize`设置为`yes`，使Redis后台运行。
- 设置密码：将`requirepass foobared`中的`foobared`更改为您的密码。

### 7. 设置开机自动启动

编辑`/etc/rc.d/rc.local`文件，添加以下命令：
```bash
/usr/local/redis-7.0.2/src/redis-server /usr/local/redis-7.0.2/redis.conf
```

### 8. 启动Redis

使用以下命令启动Redis：
```bash
/usr/local/redis-7.0.2/src/redis-server /usr/local/redis-7.0.2/redis.conf
```

检查Redis是否启动成功：
```bash
ps -ef | grep redis
```

## 总结

通过以上步骤，您可以在无网络状态下成功安装和配置Redis。如果在安装过程中遇到任何问题，请参考提供的资源文件和详细步骤进行排查。

## 下载链接

[Linux无网络状态下离线安装Redis分享](https://pan.quark.cn/s/3463bcc2efaf)