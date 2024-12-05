---
layout: post
title: "小米路由器R2D安装Misstar Tools2.0教程"
date:   2021-07-13
tags: [路由器,R2D,小米,插件,misstar]
comments: true
author: admin
---
# 小米路由器R2D安装Misstar Tools2.0教程

## 简介
本资源文件提供了小米路由器R2D安装Misstar Tools2.0的详细教程。Misstar Tools是一个功能强大的第三方插件集合，能够为小米路由器增加多种实用功能，如广告过滤、离线下载、FTP服务器等。

## 支持的路由器型号
- 小米路由器1代硬盘版（R1D）
- 小米路由器mini（R1CM）
- 全新小米路由器硬盘版（R2D）
- 小米路由器3（R3）
- 小米路由器3G（R3G）
- 小米路由器Pro（R3P）
- 小米路由器HD（R3D）

## 安装步骤

### 1. 准备工作
- 确保路由器已开启SSH功能。
- 下载对应路由器型号的压缩包和misstar.zip文件。

### 2. 安装方法
提供两种安装方法，根据自身条件选择：

#### 方法一：利用U盘安装
1. 将解压后的相应目录（如小米路由器R2D文件夹为R2D）和offline_install.sh放到U盘根目录，并插入路由器USB口。
2. 在SSH命令行中执行以下命令：
   ```bash
   cd /extdisks/sde1  # 进入U盘根目录
   ls  # 查看当前目录文件
   chmod +x offline_install.sh  # 赋予offline_install.sh文件执行权限
   ./offline_install.sh  # 执行offline_install.sh安装
   ```

#### 方法二：利用自有空间或服务器安装
1. 在SSH命令行中执行以下命令：
   ```bash
   cd /extdisks  # 切换到extdisks目录
   mkdir mt  # 创建mt文件夹
   cd mt  # 切换到mt目录
   wget http://www.****.com/R2D.zip  # 从服务器下载R2D.zip
   wget http://www.****.com/misstar.zip  # 从服务器下载misstar.zip
   ls  # 查看当前目录文件
   unzip R2D.zip  # 解压R2D.zip到当前目录
   unzip misstar.zip  # 解压misstar.zip到当前目录
   chmod +x offline_install.sh  # 赋予offline_install.sh文件执行权限
   ./offline_install.sh  # 执行offline_install.sh安装
   ```

### 3. 安装插件
1. 在SSH命令行中执行以下操作：
   ```bash
   cd /  # 回到根目录
   ls /etc/misstar/mt  # 查看插件目录
   chmod +x /etc/misstar/mt/*  # 赋予mt目录下所有插件文件执行权限
   ```
2. 使用appmanager命令安装或卸载插件，例如：
   ```bash
   /etc/misstar/scripts/appmanager add adm  # 安装adm插件
   /etc/misstar/scripts/appmanager del adm  # 卸载adm插件
   ```

## 注意事项
- 安装过程中请确保网络连接稳定。
- 安装成功后，刷新小米路由器WEB管理界面即可看到MT工具箱。
- 如需其他插件，可前往GitHub搜索相关Misstar Tools插件。

## 结语
通过本教程，您可以轻松为小米路由器R2D安装Misstar Tools2.0，并根据需要安装各种实用插件，提升路由器的功能和使用体验。

## 下载链接

[小米路由器R2D安装MisstarTools2.0教程分享](https://pan.quark.cn/s/ece3842dfccf)