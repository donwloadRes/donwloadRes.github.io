---
layout: post
title: "SonarQube 和 SonarScanner 在 Linux 服务器上的配置指南"
date:   2022-10-25
tags: [SonarQube,SonarScanner,sonar,版本,配置]
comments: true
author: admin
---
# SonarQube 和 SonarScanner 在 Linux 服务器上的配置指南

本文档详细介绍了如何在 Linux 服务器上安装和配置 SonarQube 以及 SonarScanner。由于在安装过程中可能会遇到各种错误，因此本文提供了详细的步骤和解决方案，帮助您顺利完成配置。

## 内容概述

1. **环境准备**
   - JDK 版本要求
   - MySQL 版本要求

2. **安装步骤**
   - 下载并解压 SonarQube 和 SonarScanner
   - 创建非 root 用户并授权
   - 配置 SonarQube 和 SonarScanner

3. **常见错误及解决方案**
   - 权限问题
   - 数据库配置问题
   - 启动失败问题

## 详细步骤

### 1. 环境准备

#### JDK 版本要求
- SonarQube 7.8 及以下版本支持 JDK 8
- 从 SonarQube 7.9 版本开始，要求 JDK 11

#### MySQL 版本要求
- SonarQube 7.5 版本要求 MySQL 版本 >= 5.6 且 < 8.0

### 2. 安装步骤

#### 下载并解压 SonarQube 和 SonarScanner
- 下载 SonarQube 7.5 和 SonarScanner 4.8.0.2856-linux 版本
- 解压到指定目录，例如 `/etc/docker`

#### 创建非 root 用户并授权
- 创建一个非 root 用户 `useradd sonar`
- 授权 `chown -R sonar:sonar /etc/docker/sonarqube-7.5`

#### 配置 SonarQube 和 SonarScanner
- 编辑 `sonar.properties` 文件，配置数据库连接信息
- 配置环境变量，确保 SonarScanner 可执行

### 3. 常见错误及解决方案

#### 权限问题
- 如果遇到 `AccessDeniedException` 错误，使用 `chown -R sonar:sonar /etc/docker/sonarqube-7.5` 授权

#### 数据库配置问题
- 确保数据库版本符合要求，并在 `sonar.properties` 中正确配置数据库连接信息

#### 启动失败问题
- 检查日志文件，排查启动失败的具体原因

## 总结

通过本文档，您可以顺利在 Linux 服务器上安装和配置 SonarQube 以及 SonarScanner，并解决可能遇到的各种错误。希望本文对您有所帮助！

## 下载链接

[SonarQube和SonarScanner在Linux服务器上的配置指南](https://pan.quark.cn/s/035a93e83f52)