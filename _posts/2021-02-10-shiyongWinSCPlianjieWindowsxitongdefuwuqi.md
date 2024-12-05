---
layout: post
title: "使用WinSCP连接Windows系统的服务器"
date:   2020-09-01
tags: [WinSCP,服务器,Windows,OpenSSH,软件]
comments: true
author: admin
---
# 使用WinSCP连接Windows系统的服务器

本文详细介绍了如何使用WinSCP工具连接Windows系统的服务器，并进行文件传输。WinSCP是一款功能强大的文件传输工具，支持SFTP、SCP等协议，适用于Windows系统。

## 前置准备

1. **下载WinSCP软件**：在本地电脑上下载并安装WinSCP软件。
2. **下载OpenSSH软件**：在服务器主机上下载并安装OpenSSH软件。

## 操作步骤

### 第一步：安装OpenSSH

1. 在服务器上解压下载好的OpenSSH软件。
2. 在解压的文件夹内，使用管理员身份打开PowerShell。
3. 在命令行中输入以下指令：
   ```powershell
   powershell.exe -ExecutionPolicy Bypass -File install-sshd.ps1
   ```

### 第二步：设置防火墙规则

1. 打开Windows防火墙设置。
2. 添加允许OpenSSH服务通过防火墙的规则。

### 第三步：开始连接

1. 打开WinSCP软件。
2. 输入服务器的IP地址、用户名和密码。
3. 点击“登录”按钮，即可成功连接到Windows服务器。

## 注意事项

- 确保服务器已开启SSH协议。
- 防火墙设置需允许OpenSSH服务通过。
- 使用管理员权限运行PowerShell以安装OpenSSH。

通过以上步骤，您可以顺利使用WinSCP连接Windows系统的服务器，并进行文件传输操作。

## 下载链接

[使用WinSCP连接Windows系统的服务器分享](https://pan.quark.cn/s/954d56fff9c2)