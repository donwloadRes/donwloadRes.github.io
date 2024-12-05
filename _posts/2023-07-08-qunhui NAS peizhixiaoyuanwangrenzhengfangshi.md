---
layout: post
title: "群晖 NAS 配置校园网认证方式"
date:   2021-03-09
tags: [NAS,群晖,校园网,认证,容器]
comments: true
author: admin
---
# 群晖 NAS 配置校园网认证方式

本资源文件提供了如何在群晖 NAS 上配置校园网认证的详细步骤。通过本指南，您可以轻松地在校园网环境下使用群晖 NAS，并实现网络认证功能。

## 内容概述

1. **准备工作**
   - 群晖对应型号的 Container Manager 安装文件
   - 下载连接群晖 Docker 的 siomiz-chrome 容器文件
   - VNC 客户端软件
   - 校园网有线连接的网口
   - 一台有网口的电脑

2. **实操步骤**
   - 网线连接
   - 安装 Container Manager
   - 安装 siomiz-chrome 容器
   - 运行容器并设置端口
   - VNC 访问容器

3. **参考资料**
   - 群晖 Synology NAS 使用 web 验证上网（DSM 7.0）
   - 群晖系统（其他 NAS 也可参考）校园网登录认证

## 使用说明

1. **网线连接**
   - 使用一根网线连接 NAS 与电脑，打开 Synology Assistant 程序进行扫描和安装。

2. **安装 Container Manager**
   - 在系统里的套件中心中，选择从文件安装，选取下载的 Container Manager 文件。

3. **安装 siomiz-chrome 容器**
   - 在 Docker 的容器设置中选择 siomiz-chrome 文件进行导入，并设置运行的端口。

4. **VNC 访问容器**
   - 将校园网的网线插到 NAS 上，使用 VNC Viewer 访问 NAS 的 IP 和设置的端口，进行认证。

通过以上步骤，您可以在校园网环境下成功配置群晖 NAS 的网络认证功能。

## 下载链接

[群晖NAS配置校园网认证方式](https://pan.quark.cn/s/ea38e12f4ba4)