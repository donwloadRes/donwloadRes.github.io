---
layout: post
title: "【deepin】离线安装x11vnc和xrdp，使用Windows远程访问Deepin系统"
date:   2021-04-16
tags: [x11vnc,xrdp,Windows,Deepin,安装]
comments: true
author: admin
---
# 【deepin】离线安装x11vnc和xrdp，使用Windows远程访问Deepin系统

## 概述

本资源包旨在帮助深影（deepin）Linux系统用户在无网络环境下，顺利安装x11vnc和xrdp软件，从而实现从Windows系统远程桌面访问Deepin的操作。x11vnc允许您远程访问Linux桌面，而xrdp则是让Windows远程桌面协议(RDP)能够连接到Linux桌面的关键。

## 离线安装步骤概述

### 下载离线包
首先，您需下载离线安装包及其依赖文件。原博主提供了百度网盘链接，提取码为`a57h`，确保下载完整包至本地。

### x11vnc离线安装
1. **切换用户**: 使用`su`命令切换到root用户。
2. **文件上传**: 将下载的x11vnc安装包和相关依赖上传至服务器的特定路径，例如`/data/packages/x11vnc/`。
3. **安装包部署**: 进入存放包的目录，使用命令`dpkg -i *.deb`来安装所有`.deb`包。
4. **配置密码**: 运行`x11vnc -storepasswd /etc/x11vnc/pass`设定访问密码，并调整文件权限以确保可访问性。
5. **配置与启动**: 更新x11vnc的systemd服务配置文件，并通过`systemctl daemon-reload`重载配置，随后启动服务(`service x11vnc start`)。

### xrdp离线安装
1. **类似步骤**: 对xrdp重复上述的上传和安装过程，在同一或相应目录下操作。
2. **服务状态检查**: 使用`systemctl status xrdp`确认服务是否成功安装并处于活动状态。
3. **远程连接**: 设置完毕后，从Windows端使用远程桌面连接功能，输入Deepin的IP地址即可尝试远程访问。

## 注意事项
- 确保在执行这些步骤之前，您的系统已做好数据备份，并理解命令可能带来的系统变化。
- 若在安装过程中遇到依赖问题，可能需要手动查找并安装缺失的依赖文件。

以上步骤基于博主xmzmqx在CSDN上的分享，具体实施时可能需根据实际系统环境做出适当调整。成功实施后，您将能够在Windows系统上便捷地远程操作Deepin桌面，提高跨平台的工作效率。

## 下载链接

[deepin离线安装x11vnc和xrdp使用Windows远程访问Deepin系统](https://pan.quark.cn/s/cdaa9bf10261)