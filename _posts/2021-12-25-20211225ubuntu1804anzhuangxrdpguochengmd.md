---
layout: post
title: "ubuntu1804安装xrdp过程"
date:   2024-02-06
tags: [xrdp,远程桌面,sudo,安装,Ubuntu]
comments: true
author: admin
---
# ubuntu18.04安装xrdp过程

本文档提供了一份详细指南，旨在帮助用户在Ubuntu 18.04操作系统上顺利安装xrdp，实现远程桌面访问功能。xrdp是一款开源的远程桌面协议服务器，允许用户通过微软的RDP协议控制其Linux桌面环境。

### 1. 安装桌面环境

- **准备步骤**：首先确保系统更新至最新。
- **命令**：使用`sudo apt install xfce4 xfce4-goodies xorg dbus-x11 x11-xserver-utils`安装XFCE4桌面环境，这提供了完整的桌面体验。

### 2. 安装xrdp

- **执行命令**：运行`sudo apt install xrdp`来安装xrdp服务器。
- **服务状态**：安装完毕后，通过`sudo systemctl status xrdp`检查xrdp服务是否已启动。

### 3. 配置xrdp

- **编辑配置**：打开`/etc/xrdp/xrdp.ini`文件，并在末尾添加`exec startxfce4`来指定使用XFCE4作为远程桌面会话。
- **重启服务**：修改后，使用`sudo systemctl restart xrdp`重启服务以应用更改。

### 4. 防火墙配置

- **开放端口**：如果你开启了防火墙，需允许TCP端口3389的流量，命令为`sudo ufw allow 3389`，或者限制特定IP范围。

### 5. 连接xrdp

- **客户端连接**：在Windows系统中，使用自带的远程桌面客户端，输入Ubuntu服务器的IP地址即可建立连接。

### 6. 解决蓝屏问题的简便方法

- **脚本安装**：为了避免常见的配置错误导致的蓝屏问题，推荐使用预编译脚本。访问特定站点下载`xrdp-installer-1.2`脚本（请注意下载最新且适用于你的Ubuntu版本），赋予执行权限并运行，这样通常能更简单快捷完成安装，避免手动配置的复杂性。

### 注意事项

- 在配置过程中，确保所有的步骤都以正确的权限执行，一般使用sudo命令来获得必要的权限。
- 配置完xrdp后，确保防火墙不会阻止远程桌面连接。
- 若遇到连接问题，检查网络配置和xrdp服务的状态。

通过以上步骤，即使对Linux系统不太熟悉的用户也能轻松在Ubuntu 18.04上搭建远程桌面环境，提升工作效率。

## 下载链接

[ubuntu18.04安装xrdp过程](https://pan.quark.cn/s/d81b1b4d73a0)