---
layout: post
title: "KITTI数据集不翻墙下载到Ubuntu 18.04的详细过程"
date:   2020-08-02
tags: [文件夹,共享,KITTI,Ubuntu,下载]
comments: true
author: admin
---
# KITTI数据集不翻墙下载到Ubuntu 18.04的详细过程

## 简介
本文档详细介绍了如何在不翻墙的情况下，将KITTI数据集下载并导入到Ubuntu 18.04系统中。KITTI数据集是自动驾驶领域广泛使用的数据集，包含了多种传感器数据，如图像、激光雷达和GPS数据。通过本文档，您可以轻松地将KITTI数据集下载到您的Ubuntu系统中，并进行后续的开发和研究工作。

## 步骤

### 1. 在Windows系统中下载KITTI数据集
- 首先，在Windows系统中使用百度网盘下载KITTI数据集。下载速度较快，大几十个G的文件只需半天时间。

### 2. 共享文件夹设置
- 下载完成后，右键点击保存的文件夹，选择“属性” -> “共享”。如果没有共享选项，点击“高级共享”，勾选“共享此文件夹”，然后确定。
- 在上一级目录中，点击“共享”，设置共享权限为“读取/写入”。

### 3. 查看共享文件夹
- 在Windows桌面上右键点击“此电脑”，选择“管理” -> “共享文件夹”，查看已共享的文件夹。
- 确认共享文件夹已设置成功，并记录下电脑的IPv4地址。

### 4. 在VirtualBox中设置共享文件夹
- 在VirtualBox中打开虚拟机的设置（确保虚拟机未运行），选择“共享文件夹”，点击“添加共享文件夹”。
- 选择刚刚共享的文件夹，勾选“自动挂载”，然后确定。

### 5. 在Ubuntu中挂载共享文件夹
- 在Ubuntu命令行中创建一个文件夹用于挂载共享文件夹：`mkdir /mnt/my_share`。
- 安装Samba和CIFS工具：`sudo apt-get install smbclient` 和 `sudo apt-get install cifs-utils`。
- 挂载共享文件夹：`sudo mount -t cifs -o username=win电脑的用户名 //IP地址/共享文件夹名称 /mnt/my_share`。
- 输入Windows主机的用户密码（如果设置了密码），完成挂载。

### 6. 验证挂载
- 打开`/mnt/my_share`文件夹，确认文件已成功从Windows拷贝到Ubuntu中。

## 总结
通过以上步骤，您可以轻松地将KITTI数据集下载并导入到Ubuntu 18.04系统中，无需翻墙，操作简单快捷。希望本文档能帮助您顺利完成数据集的下载和导入工作。

## 下载链接

[KITTI数据集不翻墙下载到Ubuntu18.04的详细过程分享](https://pan.quark.cn/s/d172d5f2d44c)