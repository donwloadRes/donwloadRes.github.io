---
layout: post
title: "Win10安装NET Framework 35的离线文件sxs"
date:   2021-01-07
tags: [NET,Framework,3.5,sxs,安装]
comments: true
author: admin
---
# Win10安装.NET Framework 3.5的离线文件sxs

## 简介

在Windows 10系统中，安装某些软件时可能会提示需要.NET Framework 3.5的运行环境。这是因为这些软件依赖于.NET Framework 3.5（包括.NET 2.0和3.0）来正常运行。本仓库提供了一个离线文件sxs，帮助用户在Windows 10系统中安装.NET Framework 3.5。

## 资源文件说明

- **文件名称**: `sxs.cab`
- **文件类型**: 离线安装包
- **适用系统**: Windows 10
- **功能**: 提供.NET Framework 3.5的离线安装文件，方便用户在没有网络连接的情况下安装.NET Framework 3.5。

## 使用方法

1. **下载文件**: 从本仓库下载`sxs.cab`文件。
2. **打开命令提示符**: 以管理员身份运行命令提示符。
3. **输入命令**: 在命令提示符中输入以下命令：
   ```
   dism /online /enable-feature /featurename:NetFX3 /All /Source:C:\path\to\sxs /LimitAccess
   ```
   其中，`C:\path\to\sxs`是`sxs.cab`文件的实际路径。
4. **等待安装完成**: 命令执行后，系统会自动安装.NET Framework 3.5，安装完成后会提示成功。

## 注意事项

- 请确保以管理员身份运行命令提示符，否则可能会导致安装失败。
- 如果系统已经安装了.NET Framework 3.5，再次运行该命令不会产生任何影响。
- 如果在安装过程中遇到问题，请检查命令路径是否正确，并确保文件完整无损。

## 适用场景

- 当Windows 10系统提示需要安装.NET Framework 3.5时。
- 在没有网络连接的情况下，需要安装.NET Framework 3.5。

## 其他说明

本资源文件仅供学习和研究使用，请勿用于商业用途。如有任何问题或建议，欢迎在仓库中提出。

## 下载链接

[Win10安装.NETFramework3.5的离线文件sxs](https://pan.quark.cn/s/1be84f54a26a)