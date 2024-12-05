---
layout: post
title: "青龙面板搭建教程"
date:   2023-08-18
tags: [ql,面板,PWD,青龙,Docker]
comments: true
author: admin
---
# 青龙面板搭建教程

## 概述

本文档旨在为初次接触青龙面板的用户提供详细、步骤式的指导，帮助您在自己的服务器上顺利部署青龙面板。青龙面板是一款流行的自动化脚本管理平台，广泛应用于各种自动化任务，尤其是在网络薅羊毛和日常网络任务自动化方面表现突出。以下是基于Linux系统的安装流程，适合具有基本Linux知识的用户。

## 准备工作

- **服务器**: 推荐使用腾讯云或阿里云的VPS，确保其操作系统为CentOS 7.x。
- **SSH工具**: 强烈推荐使用FinalShell作为远程连接工具。
- **Docker**: 青龙面板需要在Docker环境中运行，因此您需要预先安装Docker。

## 安装步骤

### 1. 服务器基础配置

- 设置好服务器的基本信息，包括设置一个安全的SSH登录密码。
- 安装宝塔面板（可选），便于管理服务器。

### 2. 安装Docker

- 使用SSH连接到服务器，运行命令安装Docker：
  ```
  yum install -y wget && wget -O install.sh http://download.bt.cn/install/install_6.0.sh && sh install.sh
  ```

### 3. 拉取并安装青龙面板

- 通过Docker拉取青龙面板的最新镜像：
  ```
  docker pull whyour/qinglong:latest
  ```
- 创建并运行青龙容器，根据需要映射相应的目录：
  ```
  docker run -dit \
    -v $PWD/ql/config:/ql/config \
    -v $PWD/ql/log:/ql/log \
    -v $PWD/ql/db:/ql/db \
    -v $PWD/ql/repo:/ql/repo \
    -v $PWD/ql/raw:/ql/raw \
    -v $PWD/ql/scripts:/ql/scripts \
    -v $PWD/ql/jbot:/ql/jbot \
    -v $PWD/ql/deps:/ql/deps \
    -v $PWD/ql/ninja:/ql/ninja \
    -p 5700:5700 \
    -p 5701:5701 \
    --name qinglong \
    --hostname qinglong \
    --restart unless-stopped \
    whyour/qinglong:latest
  ```

### 4. 访问青龙面板

- 通过浏览器访问你的服务器IP地址加上对应的端口（默认5700），完成青龙面板的初始化设置。

### 5. 配置与优化

- 登录后，根据界面提示安装必要的依赖和配置环境。
- 可能需要执行一些脚本来一键安装依赖项和配置环境变量。

### 结语

至此，您已完成青龙面板的基本搭建。为了更好地利用青龙面板，建议熟悉其使用界面和脚本编写/管理功能。加入社区交流群可以获得更多的帮助和脚本资源，享受自动化带来的便捷。记得定期关注面板的更新，以便获得最新的特性和安全补丁。祝您使用愉快！

---

请注意，具体的操作细节可能会随着软件版本更新而有所变化，建议对照最新版本的官方文档或教程进行操作。

## 下载链接

[青龙面板搭建教程](https://pan.quark.cn/s/d180adf0945e)