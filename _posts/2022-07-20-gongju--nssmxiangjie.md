---
layout: post
title: "工具--nssm详解"
date:   2023-05-09
tags: [nssm,servername,服务,webapp8888,程序]
comments: true
author: admin
---
# 工具--nssm详解

## 简介
nssm（Non-Sucking Service Manager）是一个服务封装程序，它可以将普通exe程序封装成服务，实现开机自启动。同类型的工具还有微软自己的srvany，不过nssm更加简单易用，并且功能强大。

### 特点
- 支持普通exe程序（控制台程序或者带界面的Windows程序都可以）
- 安装简单，修改方便
- 可以自动守护封装了的服务，程序挂掉了后可以自动重启

## 配置详解

### 下载地址
可以从官网地址下载最新版本的nssm。

### 解压与安装
1. 解压压缩包，根据系统位数选择64或32位程序。
2. 管理员权限打开命令行工具，切换到nssm.exe所在路径，运行 `nssm install` 打开程序配置界面。

### 配置项说明
- **Path**：运行应用程序的程序路径。
- **Startup directory**：应用程序所在的目录。
- **Arguments**：应用运行的参数。
- **Service name**：生成服务的名称。

### 常用命令
- `nssm install servername`：创建servername服务，弹出配置界面。
- `nssm start servername`：启动服务。
- `nssm stop servername`：暂停服务。
- `nssm restart servername`：重新启动服务。
- `nssm remove servername`：删除创建的servername服务。
- `nssm edit servername`：更改servername服务，弹出修改界面。
- `nssm set servername 参数名 参数值`：设置服务参数值。
- `sc delete servername`：Windows删除服务命令。

## 实战：将应用做成服务

### 程序说明
这里演示将net6的web项目制作成windows服务。应用的启动命令是：`dotnet WebApplication_nssm.dll --urls=http://*:8888/ --port=8888`。

### 安装服务
1. 配置Path、Startup directory、Arguments和Service name。
2. 点击install service完成windows服务安装，在windows服务列表就能看到创建的服务了。

### 管理服务
- 启动服务：`nssm start webapp8888`
- 关闭服务：`nssm stop webapp8888`
- 重启服务：`nssm restart webapp8888`
- 修改服务：`nssm edit webapp8888`
- 删除服务：`nssm remove webapp8888`

通过nssm，你可以轻松地将任何可执行程序封装为Windows服务，实现系统的自动化和无人值守运行。

## 下载链接

[工具--nssm详解](https://pan.quark.cn/s/a98f004c2362)