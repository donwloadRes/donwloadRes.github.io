---
layout: post
title: "在Windows Server 2012 R2系统上安装和使用Docker"
date:   2024-10-25
tags: [Docker,虚拟机,Windows,安装,Server]
comments: true
author: admin
---
# 在Windows Server 2012 R2系统上安装和使用Docker

本文档提供了在Windows Server 2012 R2系统上安装和使用Docker的详细步骤和指南。通过本文档，您可以了解如何在Windows Server 2012 R2系统上配置Docker环境，并进行基本的Docker操作。

## 内容概述

1. **环境准备**
   - 确保CPU支持虚拟化
   - 检查虚拟化支持状态

2. **下载Docker Toolbox工具**
   - 获取Docker Toolbox安装包
   - 下载链接：[点我下载]

3. **安装Docker Toolbox**
   - 双击运行安装程序
   - 选择安装路径
   - 安装过程中的选项设置

4. **使用虚拟机**
   - 启动虚拟机管理工具
   - 运行默认的虚拟机
   - 虚拟机默认信息

5. **端口映射**
   - 配置Docker容器端口映射
   - 在Windows Server宿主机上访问Docker容器服务

6. **目录挂载**
   - 将Windows本地目录映射到虚拟机
   - 将Docker内部目录映射到虚拟机目录

## 详细步骤

### 1. 环境准备

在安装Docker之前，确保您的CPU支持虚拟化。可以通过任务管理器中的“性能”选项卡查看虚拟化支持状态。

### 2. 下载Docker Toolbox工具

由于Windows Server 2012 R2版本需要Docker Toolbox工具支持才能运行Docker，请下载并安装Docker Toolbox。

### 3. 安装Docker Toolbox

双击下载好的Docker Toolbox程序进行安装。安装路径可自行选择，建议勾选相关选项，其余默认下一步即可。

### 4. 使用虚拟机

安装完成后，双击虚拟机管理工具，进入后默认有一个名为default的虚拟机，右击运行。虚拟机默认信息如下：
- host：192.168.99.100
- user：docker
- password：tcuser

### 5. 端口映射

如果需要将Docker容器内部的服务端口映射出来，例如将端口8001映射到宿主机，需要在Docker Toolbox工具中进行设置。

### 6. 目录挂载

如果需要将Docker内部的目录映射到Windows Server本地，需要先将Windows本地目录映射到Linux虚拟机，然后再将Docker内部目录映射到虚拟机目录。

## 总结

通过以上步骤，您可以在Windows Server 2012 R2系统上成功安装和使用Docker。希望本文档对您有所帮助。

## 下载链接

[在WindowsServer2012R2系统上安装和使用Docker](https://pan.quark.cn/s/f278c68eddb3)

## 下载链接

[在WindowsServer2012R2系统上安装和使用Docker](https://pan.quark.cn/s/91d41fb2dbe9)