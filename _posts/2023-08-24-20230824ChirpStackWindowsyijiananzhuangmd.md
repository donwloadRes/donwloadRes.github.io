---
layout: post
title: "ChirpStack@Windows：一键安装"
date:   2021-01-22
tags: [ChirpStack,双击,Windows,chirpstack,exe]
comments: true
author: admin
---
# ChirpStack@Windows：一键安装

## 简介

本资源文件提供了一个在Windows操作系统上快速安装ChirpStack的解决方案。ChirpStack是一个开源的LoRaWAN网络服务器，具备工程性、模块化、功能实现和维护活跃度等优点，是LoRaWAN Server的首选系统。

## 安装步骤

### 第1步：下载软件包

下载名为`chirpstack_simplest_vxxx.zip`的软件包，并将其解压到目录`D:\loraserver\`。

### 第2步：安装Mosquitto

1. 进入Mosquitto目录，双击`mosquitto-1.4.14-install-win32`，按默认方式安装。
2. 按下徽标+R键，运行`services.msc`，启动Mosquitto Broker服务。

**小窍门**：如果提示缺少dll文件，请进入`mosquitto_dll`拷贝所有的dll文件到`C:\Windows\SysWOW64`，再继续安装。

### 第3步：安装PostgreSQL

1. 进入PostgreSQL目录，双击`postgresql-9.6.5-1-windows-x64`，按默认方式安装。
2. 双击`postgresql_cfg`，该脚本语句自动配置用户和数据库。

**小窍门**：请将PostgreSQL安装在默认路径（`C:\Program Files\PostgreSQL\9.6\`），以便脚本语句自动配置用户和数据库。

### 第4步：启动LoRa Server

1. 双击`一键启动 ChirpStack`。
2. 浏览器会自动打开LoRa Server，请使用用户名`admin`和密码`admin`登录。

**小窍门**：如果弹出Windows防火墙提示窗，请点击“允许访问”。

## 后记

恭喜您，ChirpStack@Win7_10已经成功部署。接下来，可以通过Web添加“应用+网关+节点”。如果浏览器无法访问ChirpStack，请检查以下4个组件是否正常启动：

1. `redis-server.exe`
2. `chirpstack-gateway-bridge.exe`
3. `chirpstack-network-server.exe`
4. `chirpstack-application-server.exe`

确保这些组件正常运行，以避免ChirpStack停机。

## 下载链接

[ChirpStackWindows一键安装分享](https://pan.quark.cn/s/c64d68544ffa)