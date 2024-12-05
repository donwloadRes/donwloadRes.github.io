---
layout: post
title: "虚拟机Linux中安装MySQL教程"
date:   2022-10-08
tags: [MySQL,虚拟机,安装,压缩包,连接]
comments: true
author: admin
---
# 虚拟机Linux中安装MySQL教程

本教程详细介绍了如何在虚拟机Linux环境中安装MySQL数据库管理系统。教程涵盖了从下载MySQL压缩包到安装和配置MySQL的整个过程，适合初学者参考学习。

## 教程内容概述

### 第一步：下载MySQL压缩包和Xftp应用
1. **下载MySQL压缩包**  
   选择与虚拟机版本相应的MySQL压缩包，并将其下载到本地。

2. **下载Xftp应用**  
   下载Xftp应用，用于将MySQL压缩包传输到虚拟机中。

### 第二步：登录Xshell
1. **检查是否已安装MySQL**  
   使用命令检查系统中是否已安装MySQL，如果已安装则进行卸载。

2. **卸载旧版本MySQL**  
   使用`rpm -e`命令卸载旧版本的MySQL，并处理依赖关系。

### 第三步：解压安装软件包并删除原有日志文件
1. **创建MySQL文件夹**  
   在`/usr/local/`目录下创建一个名为`mysql`的文件夹，用于存储解压后的MySQL文件。

2. **解压缩MySQL压缩包**  
   将下载的MySQL压缩包解压到`/usr/local/mysql/`目录下。

3. **安装MySQL软件包**  
   使用`rpm -ivh`命令安装MySQL软件包，并处理依赖检测失败的问题。

4. **删除MySQL原有日志文件**  
   删除`/var/lib/mysql/`目录下的原有日志文件。

### 第四步：启动MySQL服务
1. **启动MySQL服务**  
   使用`systemctl start mysqld.service`命令启动MySQL服务，并查看运行状态。

2. **查看初始密码**  
   查看MySQL的初始密码，并使用该密码登录MySQL。

3. **修改配置文件**  
   修改MySQL的配置文件`/etc/my.cnf`，设置字符集和排序规则。

### 第五步：进入数据库并进行配置
1. **重设密码**  
   使用`set password`命令重设MySQL的root用户密码。

2. **允许远程连接**  
   修改MySQL用户权限，允许远程连接。

3. **刷新系统权限表**  
   使用`flush privileges`命令刷新系统权限表。

### 第六步：与外部客户端建立连接
1. **关闭防火墙**  
   关闭虚拟机的防火墙，确保外部客户端可以连接到MySQL服务器。

2. **在Navicat中建立连接**  
   在Navicat中新建MySQL连接，输入主机IP、用户名和密码，测试连接是否成功。

## 注意事项
- 在安装过程中，确保虚拟机已连接网络。
- 安装前检查系统中是否已安装旧版本的MySQL，并进行卸载。
- 安装过程中可能会遇到依赖检测失败的问题，需根据提示进行处理。

通过本教程，您可以顺利在虚拟机Linux环境中安装和配置MySQL数据库，并实现与外部客户端的连接。

## 下载链接

[虚拟机Linux中安装MySQL教程分享](https://pan.quark.cn/s/cd5692b79668)