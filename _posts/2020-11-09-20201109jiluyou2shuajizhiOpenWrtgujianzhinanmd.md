---
layout: post
title: "极路由2刷机至OpenWrt固件指南"
date:   2020-01-30
tags: [固件,刷机,路由器,OpenWrt,SSH]
comments: true
author: admin
---
# 极路由2刷机至OpenWrt固件指南

## 概述

本文档旨在指导拥有极路由2（型号：HC5761）的用户如何将其固件刷成开源的OpenWrt系统。刷机过程涉及开启SSH、准备必要的文件、通过SSH连接路由器以及完成刷机后的初步配置。请注意，刷机有一定风险，可能导致路由器变砖，请在操作前确保数据备份，并熟悉相关刷机知识。

## 准备工作

### 步骤1：开启SSH

由于传统的通过官方插件开启SSH的方法不再可行，您需要通过特定途径获得`local_token`和`cloud_token`以启用远程SSH连接。具体步骤可能包括访问特殊网址并遵循指示进行操作，确保路由器已联网。

### 步骤2：下载固件

从可靠的来源下载适用于极路由2的OpenWrt固件。推荐使用最新且经过验证的固件版本，以保证兼容性和稳定性。

### 工具需求

- SSH客户端（如PuTTY或其他终端模拟器）
- 用于下载固件的浏览器

## 刷机步骤

1. **连接路由器**：使用SSH客户端连接您的极路由2，连接地址一般为路由器的IP地址，默认情况下可能是192.168.1.1。
   
2. **上传固件**：在SSH会话中，根据提供的教程指示，使用适当的命令将下载的OpenWrt固件上传至路由器的临时目录。

3. **刷写固件**：使用`mtd`命令指定正确的分区和固件文件路径进行固件刷写。

4. **重启与配置**

   - 刷机完成后，路由器将会自动重启。
   - 第一次启动可能时间较长，待其完全启动后，需重新配置网络设置和路由器的基本选项。

## 注意事项

- 在整个过程中，确保电源供应稳定，避免中途断电导致刷机失败。
- 刷机前务必备份重要数据，以防意外丢失。
- 若遇到问题，查询社区论坛或文章评论区，往往能找到解决之道。

## 结论

成功刷入OpenWrt后，您将能够享受高度定制化的路由器体验，包括但不限于增强的网络安全、性能优化以及安装各种开源服务的可能性。但请务必谨慎操作，合理评估自身技术能力，必要时寻求专业帮助。

---

通过以上步骤，您可以将极路由2转换为一个更加强大和灵活的网络设备，利用OpenWrt的强大功能来提升家庭或小型办公室的网络管理能力。祝您刷机顺利！

## 下载链接

[极路由2刷机至OpenWrt固件指南](https://pan.quark.cn/s/fb2c89c79990)