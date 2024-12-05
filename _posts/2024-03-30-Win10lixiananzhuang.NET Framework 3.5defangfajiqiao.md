---
layout: post
title: "Win10离线安装.NET Framework 3.5的方法技巧"
date:   2020-12-11
tags: [NET,3.5,离线,Framework,安装]
comments: true
author: admin
---
# Win10离线安装.NET Framework 3.5的方法技巧

本文将详细介绍如何在Windows 10系统中离线安装.NET Framework 3.5的方法。由于某些办公环境可能没有外网连接，而Windows 10系统默认不自带.NET Framework 3.5，导致一些依赖于.NET 2.0、3.0或3.5的程序无法正常运行。因此，掌握离线安装.NET Framework 3.5的技巧显得尤为重要。

## 步骤一：下载.NET Framework 3.5离线包

首先，您需要下载.NET Framework 3.5的离线安装包。确保下载的安装包版本与您的系统位数匹配。

## 步骤二：重命名文件

下载完成后，将文件重命名为`netfx3.cab`。

## 步骤三：拷贝文件到系统目录

将重命名后的文件拷贝到系统盘的`C:\Windows`目录下。

## 步骤四：以管理员身份运行命令提示符

打开命令提示符，并以管理员身份运行。输入以下命令：

```
dism.exe /online /add-package /packagepath:C:\WINDOWS\netfx3.cab
```

命令中的`netfx3.cab`为离线安装包的文件名，请确保路径和文件名正确。

## 步骤五：等待安装完成

执行命令后，等待进度达到100%，即表示安装完成。

## 验证安装

安装完成后，您可以通过控制面板中的“程序和功能”选项，查看.NET Framework 3.5是否已成功安装。

通过以上步骤，您可以在Windows 10系统中成功离线安装.NET Framework 3.5，从而确保依赖于该框架的旧版程序能够正常运行。

## 下载链接

[Win10离线安装.NETFramework3.5的方法技巧分享](https://pan.quark.cn/s/052682b5d47d)