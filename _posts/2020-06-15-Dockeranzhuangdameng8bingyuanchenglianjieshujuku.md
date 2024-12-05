---
layout: post
title: "Docker安装达梦8并远程连接数据库"
date:   2022-09-03
tags: [数据库,达梦,dm8,连接,Docker]
comments: true
author: admin
---
# Docker安装达梦8并远程连接数据库

本资源文件提供了如何在Docker环境中安装达梦8数据库，并配置远程连接的详细步骤。通过本指南，您可以轻松地在Docker容器中部署达梦数据库，并实现远程访问。

## 内容概述

1. **下载达梦数据库镜像**  
   从官方下载达梦数据库的镜像文件，并上传至服务器。

2. **加载和运行达梦数据库**  
   使用Docker命令加载镜像文件，并启动数据库服务。

3. **配置远程连接**  
   配置数据库服务以允许远程连接，并提供默认的用户名和密码信息。

4. **使用DataGrip连接数据库**  
   介绍如何使用DataGrip作为连接工具，下载驱动并配置连接。

## 详细步骤

### 1. 下载达梦数据库镜像

从官方提供的下载地址下载达梦数据库镜像文件，并确认文件大小无误。

### 2. 加载和运行达梦数据库

将下载的镜像文件上传至服务器的`/opt`目录下，使用以下命令加载并运行数据库：

```bash
cd /opt
docker load -i dm8_20220822_rev166351_x86_rh6_64_ctm.tar
docker run -d -p 5236:5236 --restart=always --name dm8_01 --privileged=true -e PAGE_SIZE=16 -e LD_LIBRARY_PATH=/opt/dmdbms/bin -e INSTANCE_NAME=dm8_01 -v /data/dm8_01:/opt/dmdbms/data dm8_single:v8.1.2.128_ent_x86_64_ctm_pack4
```

### 3. 配置远程连接

确保服务器防火墙已打开对应端口（如5236），以便远程连接数据库。默认的用户名和密码为：

- 最新版：`SYSDBA` / `SYSDBA001`
- 旧版：`SYSDBA` / `SYSDBA`

### 4. 使用DataGrip连接数据库

使用DataGrip连接达梦数据库时，需下载相应的驱动并配置连接。驱动文件可通过百度云网盘获取。

## 其他操作

- **停止数据库**：
  ```bash
  docker stop dm8_01
  ```

- **启动数据库**：
  ```bash
  docker start dm8_01
  ```

- **重启数据库**：
  ```bash
  docker restart dm8_01
  ```

通过以上步骤，您可以在Docker环境中成功安装并远程连接达梦8数据库。

## 下载链接

[Docker安装达梦8并远程连接数据库](https://pan.quark.cn/s/eab18fc594c5)