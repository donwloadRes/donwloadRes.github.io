---
layout: post
title: "OpenSSH for Windows 64位 下载与安装指南"
date:   2024-12-02
tags: [OpenSSH,Windows,64,下载,安装]
comments: true
author: admin
---
# OpenSSH for Windows (64位) 下载与安装指南

本仓库提供了一个适用于Windows 64位系统的OpenSSH资源文件下载。以下是详细的下载和安装步骤。

## 资源文件描述

- **文件标题**: OpenSSH for Windows (64位)
- **文件描述**: 该资源文件包含了适用于Windows 64位系统的OpenSSH安装包。请按照以下步骤进行下载和安装。

## 安装步骤

1. **下载OpenSSH**: 
   - 下载本仓库提供的OpenSSH for Windows (64位)安装包。

2. **解压文件**:
   - 将下载的文件解压到 `C:\Program Files\OpenSSH` 目录下。请确保路径完全一致，因为官方要求必须安装在此路径下。

3. **安装OpenSSH服务**:
   - 打开命令提示符（cmd），并导航到 `C:\Program Files\OpenSSH` 目录。
   - 依次执行以下命令：
     1. 安装sshd服务:
        ```powershell
        powershell.exe -ExecutionPolicy Bypass -File install-sshd.ps1
        ```
     2. 开放22号端口（可选）:
        - 如果你已经关闭了Windows防火墙并配置了入站规则，可以跳过此步骤。
        - 执行以下命令以开放22号端口：
          ```powershell
          netsh advfirewall firewall add rule name=sshd dir=in action=allow protocol=TCP localport=22
          ```

## 注意事项

- 请确保按照上述步骤进行操作，特别是路径和命令的执行顺序。
- 如果在安装过程中遇到任何问题，请参考官方文档或联系技术支持。

## 贡献与反馈

如果你在使用过程中遇到任何问题或有改进建议，欢迎提交Issue或Pull Request。

感谢你的使用！

## 下载链接

[OpenSSHforWindows64位下载与安装指南](https://pan.quark.cn/s/a7638881c27a)