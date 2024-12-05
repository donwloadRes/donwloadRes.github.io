---
layout: post
title: "Win10环境下安装Net Framework35亲测可用"
date:   2020-03-03
tags: [Win10,Net,Framework,3.5,cab]
comments: true
author: admin
---
# Win10环境下安装.Net Framework3.5（亲测可用）

## 简介

在Windows 10系统中，虽然自带了.Net Framework 4，但有时我们仍然需要安装.Net Framework 3.5。然而，直接尝试安装.Net Framework 3.5时，可能会遇到“文件找不到”等错误。即使在Windows的“添加程序及服务”中尝试添加.Net Framework 3.5，也可能会遇到错误。本资源文件提供了一种简单有效的解决方案，帮助你在Win10环境下成功安装.Net Framework 3.5。

## 解决方案

### 步骤一：解压资源文件

1. 下载并解压本仓库中的压缩包，将其放置在C盘根目录下。解压后的目录结构应如下所示：
   ```
   C:\sources\sxs\microsoft-windows-netfx3-ondemand-package.cab
   ```

### 步骤二：执行命令

1. 使用管理员权限打开CMD或PowerShell窗口。
2. 在CMD或PowerShell中执行以下命令：
   ```
   Dism /online /enable-feature /featurename:NetFX3 /All /Source:C:\sources\sxs /LimitAccess
   ```

### 解析

Windows在添加.Net Framework 3.5服务时，最终会执行Dism命令并寻找指定的cab文件。这个cab文件通常存在于原版Win10安装包中，因此添加服务时需要挂载Win10原版安装包。然而，这需要下载和准备Win10安装包，较为麻烦。本方法通过让Dism命令指向我们事先准备的cab文件，省去了下载Win10.iso的步骤，简化了安装过程。

## 注意事项

- 请确保以管理员权限运行CMD或PowerShell。
- 确保解压后的文件路径正确，否则命令可能无法执行。

## 贡献

如果你有任何改进建议或发现了问题，欢迎提交Issue或Pull Request。

## 许可证

本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 下载链接

[Win10环境下安装.NetFramework3.5亲测可用](https://pan.quark.cn/s/85090a8e9cad)