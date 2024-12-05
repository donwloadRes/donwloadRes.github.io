---
layout: post
title: "Visio 2021 安装指南及常见问题解答"
date:   2020-07-19
tags: [Office,安装,Microsoft,Visio,Program]
comments: true
author: admin
---
# Visio 2021 安装指南及常见问题解答

本仓库提供了一个详细的指南，帮助用户安装 Visio 2021 并解决在安装过程中可能遇到的问题。特别是，本文档还介绍了如何更改 Office 的默认安装位置。

## 内容概述

1. **Visio 2021 安装步骤**
   - 下载 Visio 2021 安装包
   - 双击安装包并按照提示完成安装
   - 安装中文语言包（可选）

2. **更改 Office 安装位置**
   - 删除 C 盘中的 Microsoft Office 文件夹
   - 在 D 盘或 E 盘创建新的安装路径
   - 使用符号链接将默认安装路径指向新位置

3. **常见问题及解决方案**
   - 安装路径修改不正确导致的软件启动错误
   - 插入图表时出现的错误
   - 软件版本兼容性问题

## 安装步骤详解

### 1. 下载 Visio 2021 安装包

首先，从官方网站或可信的第三方平台下载 Visio 2021 的安装包。确保下载的版本与您的操作系统兼容（32 位或 64 位）。

### 2. 安装 Visio 2021

双击下载的安装包，启动安装程序。按照屏幕上的提示完成安装过程。安装过程中，您可以选择安装位置，但默认情况下，Office 不允许自定义安装路径。

### 3. 更改 Office 安装位置

如果您希望将 Office 安装到非默认位置（如 D 盘或 E 盘），可以按照以下步骤操作：

- 删除 C 盘中的 `Microsoft Office` 和 `Microsoft Office 15` 文件夹（前提是已经卸载了 Windows 自带的 Office 365）。
- 在 D 盘或 E 盘创建新的文件夹路径，例如 `D:\Program Files\Microsoft Office` 和 `D:\Program Files\Microsoft Office 15`。
- 以管理员身份打开命令提示符，输入以下命令创建符号链接：
  ```
  MKLINK /J "C:\Program Files\Microsoft Office" "D:\Program Files\Microsoft Office"
  MKLINK /J "C:\Program Files\Microsoft Office 15" "D:\Program Files\Microsoft Office 15"
  ```

### 4. 安装完成

完成上述步骤后，重新启动安装程序，Office 将会安装到您指定的新位置。

## 常见问题及解决方案

### 1. 安装路径修改不正确导致的软件启动错误

如果修改后的安装路径不正确，可能会导致软件无法启动。解决方法是卸载软件后重新修改路径，并确保路径在 `Program Files` 文件夹下。

### 2. 插入图表时出现的错误

在某些情况下，插入图表时可能会出现错误。可以尝试在路径下新建一个 Excel 文件，将数据复制进去后再插入图表，然后复制到 Word 中。

### 3. 软件版本兼容性问题

确保 Visio 版本与 Office 版本兼容。如果遇到兼容性问题，可以尝试安装不同版本的 Visio 或 Office。

## 结语

通过本指南，您应该能够顺利安装 Visio 2021 并解决常见的安装问题。如果在安装过程中遇到其他问题，欢迎在评论区留言，我们会尽力提供帮助。

## 下载链接

[Visio2021安装指南及常见问题解答](https://pan.quark.cn/s/f37249f23c68)