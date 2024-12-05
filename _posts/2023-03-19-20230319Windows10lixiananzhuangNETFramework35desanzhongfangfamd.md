---
layout: post
title: "Windows 10 离线安装 .NET Framework 3.5 的三种方法"
date:   2023-04-26
tags: [Windows,NET,Framework,3.5,离线]
comments: true
author: admin
---
# Windows 10 离线安装 .NET Framework 3.5 的三种方法

本文介绍了在 Windows 10 系统中离线安装 .NET Framework 3.5 的三种方法。这些方法适用于在没有网络连接的情况下，需要安装 .NET Framework 3.5 的用户。

## 方法一：使用 NetFx3.cab 文件

1. 下载 NetFx3.cab 文件，并将其放置在 Windows 10 系统盘的 C:\Windows\ 文件夹中。
2. 以管理员身份运行命令提示符，输入以下命令并回车：
   ```
   dism /online /Enable-Feature /FeatureName:NetFx3 /Source:"%windir%" /LimitAccess
   ```
3. 等待部署进度达到 100%，无报错即可。
4. 在“程序和功能”-“Windows 功能”中查看，确认 .NET Framework 3.5 选项已被勾选。

## 方法二：使用 Windows ISO 镜像

1. 下载一个包含 source/sxs 目录的 Windows ISO 镜像文件。
2. 右键点击 ISO 镜像文件并选择“挂载”。
3. 打开“我的电脑”，查看挂载后的盘符。
4. 以管理员身份运行命令提示符，执行以下命令：
   ```
   dism.exe /online /enable-feature /featurename:netfx3 /Source:E:\sources\sxs
   ```
   注意：将 `/Source:E` 中的 E 替换为挂载镜像的盘符。

## 方法三：使用 sxs 文件夹

1. 下载包含 sxs 文件夹的资源文件，并将其解压到 C 盘根目录。
2. 以管理员身份打开命令提示符，执行以下命令：
   ```
   Dism /online /enable-feature /featurename:NetFX3 /All /Source:c:\sxs /LimitAccess
   ```
3. 等待命令执行完成，确认 .NET Framework 3.5 已成功安装。

通过以上三种方法，您可以在 Windows 10 系统中离线安装 .NET Framework 3.5，确保您的应用程序能够正常运行。

## 下载链接

[Windows10离线安装.NETFramework3.5的三种方法](https://pan.quark.cn/s/4ec4776c83b4)