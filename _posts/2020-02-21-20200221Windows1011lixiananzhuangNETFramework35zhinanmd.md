---
layout: post
title: "Windows 1011 离线安装 NET Framework 35 指南"
date:   2020-09-29
tags: [Windows,离线,安装,NET,Framework]
comments: true
author: admin
---
# Windows 10/11 离线安装 .NET Framework 3.5 指南

本仓库提供了一个资源文件，用于在 Windows 10 和 Windows 11 系统中离线安装 .NET Framework 3.5，包括 .NET 2.0 和 3.0。以下是详细的安装步骤和注意事项。

## 资源文件说明

- **文件名称**: Windows 10/11 离线安装 .NET Framework 3.5
- **文件内容**: 包含离线安装所需的 .NET Framework 3.5 组件

## 安装步骤

1. **下载资源文件**: 从本仓库下载资源文件。
2. **解压文件**: 将下载的文件解压到任意目录。
3. **打开命令提示符**: 以管理员身份打开命令提示符。
4. **运行安装命令**: 在命令提示符中输入以下命令：
   ```
   dism /online /enable-feature /featurename:NetFx3 /All /Source:<解压路径> /LimitAccess
   ```
   将 `<解压路径>` 替换为实际的解压路径。
5. **等待安装完成**: 系统将自动安装 .NET Framework 3.5，安装完成后会提示成功。

## 注意事项

- **管理员权限**: 确保以管理员身份运行命令提示符。
- **网络连接**: 离线安装不需要网络连接，但需要确保系统已连接到互联网以验证安装。
- **系统兼容性**: 该方法适用于 Windows 10 和 Windows 11 系统。

通过以上步骤，您可以在 Windows 10 和 Windows 11 系统中成功离线安装 .NET Framework 3.5。

## 下载链接

[Windows1011离线安装.NETFramework3.5指南](https://pan.quark.cn/s/528276560f58)