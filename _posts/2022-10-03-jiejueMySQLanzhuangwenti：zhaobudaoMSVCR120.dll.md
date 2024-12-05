---
layout: post
title: "解决MySQL安装问题：找不到MSVCR120.dll"
date:   2021-11-19
tags: [MySQL,安装,dll,MSVCR120,Microsoft]
comments: true
author: admin
---
# 解决MySQL安装问题：找不到MSVCR120.dll

## 简介

在安装MySQL时，有时会遇到以下错误提示：

```
由于找不到MSVCR120.dll, 无法继续执行代码，重新安装程序可能会解决此问题
```

此错误通常是由于系统缺少必要的Microsoft Visual C++ Redistributable文件引起的。本资源文件提供了解决此问题的详细步骤和所需文件。

## 问题描述

在MySQL初始化过程中，可能会遇到以下错误信息：

- “由于找不到MSVCR120.dll, 无法继续执行代码，重新安装程序可能会解决此问题”
- “由于找不到VCRUNTIME140_1.dll, 无法继续执行代码，重新安装程序可能会解决此问题”

## 问题原因

这种错误是由于电脑系统缺少部分配置文件引起的。安装MySQL时需要这些配置文件，但系统中未安装或缺失这些文件。

## 解决办法

### 1. 下载并安装Microsoft Visual C++ Redistributable

- 访问Microsoft官方网站，下载并安装适用于您操作系统的Microsoft Visual C++ Redistributable包。
- 下载地址：[Microsoft Visual C++ Redistributable](https://www.microsoft.com/zh-CN/download/details.aspx?id=40784)

### 2. 安装步骤

1. 下载完成后，运行安装程序。
2. 按照提示完成安装过程。
3. 安装完成后，重新尝试初始化MySQL。

### 3. 其他解决方法

如果上述方法未能解决问题，您还可以尝试以下步骤：

- 从其他已安装MySQL的电脑上复制缺失的DLL文件到您的系统中。
- 使用系统文件检查工具（如sfc /scannow）扫描并修复系统文件错误。

## 结论

通过安装Microsoft Visual C++ Redistributable包，您可以解决MySQL安装过程中由于找不到MSVCR120.dll文件而导致的错误。希望本资源文件能帮助您顺利完成MySQL的安装。

---

**注意**：如果问题仍然存在，请参考相关技术文档或寻求专业技术支持。

## 下载链接

[解决MySQL安装问题找不到MSVCR120.dll分享](https://pan.quark.cn/s/598327dd13e4)