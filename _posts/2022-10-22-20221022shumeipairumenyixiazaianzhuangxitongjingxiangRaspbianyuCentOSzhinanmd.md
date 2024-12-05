---
layout: post
title: "树莓派入门一  下载安装系统镜像Raspbian与CentOS指南"
date:   2021-11-03
tags: [树莓,Raspbian,CentOS,SD,烧录]
comments: true
author: admin
---
# 树莓派入门（一） - 下载安装系统镜像：Raspbian与CentOS指南

欢迎来到树莓派入门系列的第一篇文章，本篇将指导您如何下载并安装两个流行的树莓派操作系统：Raspbian和CentOS。无论是编程新手还是希望在小型设备上尝试Linux的老手，这篇指南都将助您快速起步。

## 引言

树莓派是一款广受欢迎的微型计算机，适用于学习编程、电子项目和小型服务器应用。Raspbian作为官方推荐的操作系统，提供了丰富的教育资源，而CentOS则是面向那些偏好企业级Linux环境的用户。

## Raspbian安装指南

### 下载镜像
首先，从[树莓派官方网站](https://www.raspberrypi.org/downloads/raspbian/)下载Raspbian镜像。您会有几个选项，包括带图形界面的完整版和轻量级的Lite版本。

### 准备SD卡
使用[SD Formatter](https://www.sdcard.org/downloads/formatter/)格式化您的SD卡，确保数据彻底清除以便安全烧录。

### 烧录镜像
利用[Win32DiskImager](https://sourceforge.net/projects/win32diskimager/)，选择已下载的Raspbian镜像文件，并指定SD卡的位置。点击“Write”开始烧录。

### 启动树莓派
烧录完毕后，无需格式化SD卡。将SD卡插入树莓派，连接显示器、鼠标和键盘，然后通电启动。初始用户名和密码通常是`pi/raspberry`。

## CentOS安装指南

对于偏爱CentOS的用户，请访问特定的[CentOS镜像下载页面](http://mirror.centos.org/altarch/7/isos/armhfp/)，根据需求选择GNOME、KDE或Minimal版本。下载完成后，按照与Raspbian相似的步骤格式化SD卡并使用Win32DiskImager烧录镜像。

### 配置与启动
CentOS烧录后，首次启动可能涉及网络配置。默认用户名和密码为`root/centos`。您可能需要通过SSH无显示器设置来配置网络，或在连接显示器的情况下手动调整。

## 注意事项
- 烧录过程中确保使用正确的SD卡盘符，避免误操作影响其他存储设备。
- 对于无屏幕启动，创建`ssh`文件于SD卡的boot分区，并配置Wi-Fi以实现远程访问。

## 结论

通过上述步骤，您不仅能够轻松地为树莓派准备Raspbian和CentOS系统镜像，还能开始探索这两个操作系统各自的特性和潜力。无论是教育、开发还是物联网项目，树莓派搭配合适的系统都将为您开启无限可能。开始您的树莓派之旅吧！

---

此文档旨在为用户提供清晰、简洁的指引，帮助用户顺利进行树莓派的操作系统安装过程。祝您学习愉快！

## 下载链接

[树莓派入门一-下载安装系统镜像Raspbian与CentOS指南分享](https://pan.quark.cn/s/3a2f4dd4396c)