---
layout: post
title: "为Server 2019或LTSC版安装Windows Store应用商店"
date:   2022-09-27
tags: [Windows,安装,LTSC,商店,Server]
comments: true
author: admin
---
# 为Server 2019或LTSC版安装Windows Store应用商店

## 简介
本资源文件旨在帮助用户在Windows Server 2019或LTSC（长期服务通道）版本上安装Windows Store应用商店。通过本资源文件，用户可以轻松恢复或安装应用商店，以便在服务器环境中使用各种UWP（通用Windows平台）应用。

## 使用方法
本资源文件提供了两种安装方法，用户可以根据自己的需求选择其中一种进行操作。

### 方法一：手动安装
1. 打开指定的网址，以PackageFamilyName方式搜索Microsoft.WindowsStore_8wekyb3d8bbwe。
2. 根据系统选择对应的包，下载每一栏分类的APPX文件。
3. 在桌面上新建一个文件夹，如“123”，将下载的安装包放入文件夹。
4. 以管理员身份运行“Powershell”，CD到“123”文件夹，并执行以下命令：
   ```powershell
   Add-AppxPackage *
   ```

### 方法二：使用工具安装
1. 下载一体化安装包，下载地址为提供的文件。
2. 下载完成后直接运行安装，运行过程中可能会报错，忽略即可。

## 注意事项
- 安装过程中可能需要管理员权限。
- 安装完成后，建议重启或注销系统以确保应用商店正常运行。

## 适用版本
本资源文件适用于Windows Server 2019和LTSC版本。

## 贡献与反馈
如果您在使用过程中遇到任何问题或有改进建议，欢迎通过相关渠道进行反馈。

---

通过以上步骤，您可以在Windows Server 2019或LTSC版本上成功安装Windows Store应用商店，享受更多应用带来的便利。

## 下载链接

[为Server2019或LTSC版安装WindowsStore应用商店分享](https://pan.quark.cn/s/41ea42b537b1)