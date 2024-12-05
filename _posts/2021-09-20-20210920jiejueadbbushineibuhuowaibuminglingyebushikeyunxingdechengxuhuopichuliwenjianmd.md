---
layout: post
title: "解决‘adb‘ 不是内部或外部命令，也不是可运行的程序或批处理文件"
date:   2020-10-02
tags: [adb,exe,文件,环境变量,路径]
comments: true
author: admin
---
# 解决‘adb‘ 不是内部或外部命令，也不是可运行的程序或批处理文件

## 简介

在使用Android开发工具时，经常会遇到“adb不是内部或外部命令，也不是可运行的程序或批处理文件”的错误提示。这个问题通常是由于系统环境变量未正确配置导致的。本文将详细介绍如何解决这个问题，并提供相应的资源文件下载。

## 问题原因

当在命令行中输入`adb`命令时，如果系统无法找到`adb.exe`文件，就会出现上述错误提示。这通常是因为`adb.exe`文件所在的路径没有添加到系统的环境变量中。

## 解决方法

1. **找到adb.exe文件路径**：首先，你需要知道`adb.exe`文件所在的路径。通常，`adb.exe`文件位于Android SDK的`platform-tools`目录下。

2. **配置环境变量**：
   - 右键点击“此电脑”或“我的电脑”，选择“属性”。
   - 点击“高级系统设置”。
   - 在“系统属性”窗口中，点击“环境变量”。
   - 在“系统变量”部分，找到并选择`Path`变量，然后点击“编辑”。
   - 点击“新建”，将`adb.exe`文件所在的路径添加到环境变量中。例如，如果`adb.exe`文件位于`C:\Program Files\Android\sdk\platform-tools`，则添加该路径。
   - 点击“确定”保存更改。

3. **重新打开命令行窗口**：配置完成后，重新打开命令行窗口，再次输入`adb`命令，应该可以正常运行。

## 资源文件下载

为了帮助你快速解决这个问题，我们提供了一个包含`adb.exe`文件的资源文件包。你可以通过以下步骤下载并使用该资源文件：

1. 下载资源文件包。
2. 解压文件包，找到`adb.exe`文件。
3. 按照上述步骤配置环境变量，将`adb.exe`文件所在的路径添加到系统环境变量中。

## 注意事项

- 确保你下载的资源文件包来自可信的来源。
- 如果你已经安装了Android SDK，但仍然遇到这个问题，建议检查SDK的安装路径是否正确，并确保`adb.exe`文件存在于`platform-tools`目录下。

通过以上步骤，你应该能够成功解决“adb不是内部或外部命令，也不是可运行的程序或批处理文件”的问题。如果你有任何疑问或遇到其他问题，欢迎在评论区留言。

## 下载链接

[解决adb不是内部或外部命令也不是可运行的程序或批处理文件](https://pan.quark.cn/s/e33105011884)