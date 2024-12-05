---
layout: post
title: "Window Terminal 安装与常见命令指南"
date:   2022-02-21
tags: [查看,Window,Terminal,hello,Windows]
comments: true
author: admin
---
# Window Terminal 安装与常见命令指南

本资源文件提供了关于Window Terminal的安装步骤和常见命令的详细指南。Window Terminal是微软开发的一款现代、功能丰富的终端应用程序，专为命令行用户设计。它支持多标签、富文本、全球化、可配置性、主题和样式等功能，是Windows系统下替代老旧DOS窗口的理想选择。

## 安装步骤

1. **下载安装包**：
   - 访问微软官方网站或通过Microsoft Store下载Window Terminal的安装包。
   - 确保你的系统是Windows 10或Windows 11，因为Window Terminal主要支持这两个版本。

2. **安装过程**：
   - 下载完成后，保持网络连接，以管理员身份运行安装文件。
   - 按照默认设置一路点击，直到安装完成。

## 常见命令

### CMD模式下的常用命令

- **进入目录**：`cd hello`
- **浏览当前目录**：`start`
- **启动应用程序**：`start QQ.exe`
- **自动关机**：`shutdown /s /t 300`
- **查看目录树**：`tree /f`
- **新建文件夹**：`md hello`
- **查看端口进程ID**：`netstat -ano | findstr "8080"`
- **获取进程名称**：`tasklist | findstr "1050"`
- **Ping百度**：`ping www.baidu.com`
- **查看本地IP**：`ipconfig /all`

### PowerShell模式下的常用命令

- **查看历史命令**：`history`
- **查看进程**：`ps QQ`
- **清屏**：`cls`
- **查看系统版本**：`wmic os get caption`
- **查看系统位数**：`wmic os get osarchitecture`
- **关闭电脑**：`Stop-Computer`
- **重启电脑**：`Restart-Computer`
- **查看文件SHA256值**：`Get-FileHash -Path \hello.txt | Format-List`
- **查看文件SHA1值**：`Get-FileHash -Path \hello.txt -Algorithm SHA1 | Format-List`
- **查看文件MD5值**：`Get-FileHash -Path \hello.txt -Algorithm MD5 | Format-List`

通过本指南，你可以轻松安装Window Terminal并掌握其常用命令，提升在Windows系统下的命令行操作体验。

## 下载链接

[WindowTerminal安装与常见命令指南分享](https://pan.quark.cn/s/35196cc70cc0)