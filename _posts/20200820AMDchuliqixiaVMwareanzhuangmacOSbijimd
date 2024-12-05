---
layout: post
title: "AMD处理器下VMware安装macOS笔记"
date:   2021-11-25
tags: [macOS,VMware,安装,虚拟机,AMD]
comments: true
author: admin
---
# AMD处理器下VMware安装macOS笔记

本仓库包含详细的指南，专为计划在配备AMD处理器的计算机上使用VMware虚拟机安装macOS系统的用户设计。文章原址已由CSDN博主分享，以下是精简版的步骤概述，帮助您顺利进行安装过程。

## 准备工作：

1. **VMware Workstation 16 Pro**：由于兼容性问题，避免使用旧版本，特别是15.5 Pro，建议选用16.x或以上版本。
2. **Unlocker解锁工具**：这是使VMware支持macOS的关键工具。
3. **macOS映像文件**：选择合适的macOS版本ISO文件用于安装。

## 步骤概览：

### 1. 安装VMware Workstation 16 Pro
- 官方下载地址或通过其他途径获取安装包。
- 完成安装程序。

### 2. 使用Unlocker解锁工具
- 下载Unlocker V3.0，并解压至与VMware同一目录，避免中文路径。
- 关闭所有VMware相关服务和进程。
- 以管理员身份运行`win-install.cmd`以解锁macOS支持和更新darwin.iso。

### 3. 下载并准备macOS映像文件
- 根据个人需求选择合适的macOS版本。

### 4. 创建macOS虚拟机
- 在VMware中新建虚拟机，选择“典型”安装，指定刚下载的macOS映像文件。
- 操作系统类型选择“Apple Mac OS X”相应的版本。

### 5. 配置虚拟机以适应AMD处理器
- 编辑虚拟机设置，确保USB控制器设为2.0。
- 修改.vmx文件，添加特定的CPU ID配置行和smc.version="0"以绕过检测。

### 6. 开启并引导安装
- 在启动前可能需要手动启动VMware服务。
- 通过磁盘工具抹掉磁盘，开始macOS安装流程。

### 7. 安装VMware Tools
- 虚拟机运行macOS后，挂载VMware Tools光盘，安装以获得更好的兼容性和性能，包括全屏功能。

### 注意事项：
- 确保你的AMD处理器支持并已开启虚拟化技术(VT-x)。
- 遵循版权规定，使用合法获取的macOS映像文件。
- 解锁和安装过程中可能会遇到特定的错误，需根据实际情况查找解决办法，如文章中提到的附录部分。

这份指南旨在帮助您顺利完成AMD平台下的macOS虚拟机搭建，但请注意操作前备份重要数据，以免意外损失。祝您安装顺利！

## 下载链接

[AMD处理器下VMware安装macOS笔记](https://pan.quark.cn/s/8681b1c389df)