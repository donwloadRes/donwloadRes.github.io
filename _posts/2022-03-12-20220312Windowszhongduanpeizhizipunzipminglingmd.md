---
layout: post
title: "Windows终端配置zipunzip命令"
date:   2021-08-22
tags: [zip,unzip,exe,终端,Windows]
comments: true
author: admin
---
# Windows终端配置zip、unzip命令

## 资源描述

本资源文件提供了在Windows终端中配置`zip`和`unzip`命令的方法，使其与Linux中的`zip`命令一致。通过配置后，您可以在Windows终端中直接使用`zip`和`unzip`命令，方便进行文件的压缩和解压缩操作。

## 配置方法

### 方法一

1. **将`zip.exe`和`unzip.exe`加入到环境变量的Path中**：
   - 将`zip.exe`和`unzip.exe`文件复制到任意目录，例如`C:\zip`。
   - 打开系统环境变量设置，将`C:\zip`添加到系统的`Path`变量中。

2. **打开cmd终端，即可使用zip、unzip命令**：
   - 重新打开命令提示符（cmd），输入`zip`或`unzip`命令，即可正常使用。

### 方法二

1. **把`zip.exe`和`unzip.exe`文件复制到目录中**：
   - 将`zip.exe`和`unzip.exe`文件复制到`C:\Program Files\Git\mingw64\bin`目录中。

2. **重新打开终端Git Bash**：
   - 重新打开Git Bash终端，输入`zip -help`命令，确认配置成功。

## 预祝成功

通过以上两种方法，您可以在Windows终端中顺利配置并使用`zip`和`unzip`命令。预祝您的配置过程顺利，享受便捷的文件压缩和解压缩体验！

## 下载链接

[Windows终端配置zipunzip命令](https://pan.quark.cn/s/990632868a10)