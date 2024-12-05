---
layout: post
title: "Linux离线安装NTP服务指南"
date:   2022-06-12
tags: [NTP,rpm,bash,服务,el7]
comments: true
author: admin
---
# Linux离线安装NTP服务指南

本仓库提供了一个资源文件，用于在无外网环境下配置本地时间同步的Linux离线安装NTP服务。通过本指南，您可以在没有互联网连接的情况下，成功安装和配置NTP服务，确保系统时间的准确性。

## 资源文件内容

- **ntp-4.2.6p5-29.el7.centos.2.x86_64.rpm**: NTP服务的主安装包。
- **ntpdate-4.2.6p5-29.el7.centos.2.x86_64.rpm**: NTP时间同步工具的安装包。
- **autogen-libopts-5.18-5.el7.x86_64.rpm**: NTP服务的依赖包。

## 安装步骤

1. **下载资源文件**: 从本仓库下载上述资源文件到您的Linux系统中。

2. **安装依赖包**: 
   ```bash
   rpm -ivh autogen-libopts-5.18-5.el7.x86_64.rpm
   ```

3. **安装NTP服务**:
   ```bash
   rpm -ivh ntp-4.2.6p5-29.el7.centos.2.x86_64.rpm
   ```

4. **安装NTP时间同步工具**:
   ```bash
   rpm -ivh ntpdate-4.2.6p5-29.el7.centos.2.x86_64.rpm
   ```

5. **配置NTP服务**:
   - 编辑NTP配置文件 `/etc/ntp.conf`，根据您的网络环境进行配置。
   - 启动NTP服务:
     ```bash
     systemctl start ntpd
     ```
   - 设置NTP服务开机自启动:
     ```bash
     systemctl enable ntpd
     ```

6. **验证NTP服务**:
   - 查看NTP服务状态:
     ```bash
     systemctl status ntpd
     ```
   - 查看NTP服务器与上层NTP的状态:
     ```bash
     ntpq -p
     ```

## 注意事项

- 在配置NTP服务时，确保防火墙允许UDP 123端口的通信。
- 如果系统中已存在其他时间同步服务（如chronyd），请先停止并禁用该服务。

## 参考文档

本指南参考了CSDN博客文章《Linux离线安装NTP服务，无外网环境下配置本地时间同步》，详细内容请参阅该文章。

---

通过以上步骤，您可以在无外网环境下成功安装和配置NTP服务，确保系统时间的准确性。

## 下载链接

[Linux离线安装NTP服务指南](https://pan.quark.cn/s/350e17fc9d3a)