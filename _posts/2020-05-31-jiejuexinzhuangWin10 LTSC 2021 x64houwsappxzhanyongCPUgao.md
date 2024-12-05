---
layout: post
title: "解决新装Win10 LTSC 2021 x64后wsappx占用CPU高"
date:   2023-10-01
tags: [x64,wsappx,CPU,运行库,文件]
comments: true
author: admin
---
# 解决新装Win10 LTSC 2021 x64后wsappx占用CPU高

## 简介

本仓库提供了一个资源文件，用于解决在新安装的Windows 10 LTSC 2021 x64系统中，wsappx进程占用CPU过高的问题。该问题通常是由于系统缺少必要的运行库文件导致的。

## 问题描述

在安装Windows 10 LTSC 2021 x64系统后，用户可能会发现wsappx进程占用CPU资源过高，导致系统运行缓慢，风扇持续高速运转。这通常是由于系统缺少Microsoft VCLibs 140.00运行库文件所致。

## 解决方案

通过安装缺失的运行库文件，可以有效解决wsappx进程占用CPU过高的问题。本仓库提供的资源文件包含了所需的运行库文件，用户只需按照以下步骤操作即可：

1. 下载本仓库中的资源文件。
2. 以管理员身份运行PowerShell。
3. 运行以下命令安装运行库文件：
   ```powershell
   Add-AppxPackage -Path "路径\Microsoft.VCLibs.140.00_14.0.30704.0_x64__8wekyb3d8bbwe.Appx"
   ```
4. 重启电脑。

## 注意事项

- 请确保以管理员身份运行PowerShell，否则命令可能无法执行。
- 安装完成后，建议重启电脑以确保更改生效。

## 参考文章

有关该问题的详细描述和解决方案，请参考以下文章：
[解决新装win10-LTSC-2021-x64后wsappx占用CPU高](https://blog.csdn.net/xwoodwu/article/details/140037759)

## 贡献

如果您有任何改进建议或发现了新的解决方案，欢迎提交Issue或Pull Request。

## 许可证

本仓库中的资源文件遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接和本声明。