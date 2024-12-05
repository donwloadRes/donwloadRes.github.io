---
layout: post
title: "FastReport企业版源代码6617 支持104 FastReport 简化管理工具20"
date:   2020-10-14
tags: [文件夹,FastReport,文件,bat,res]
comments: true
author: admin
---
# FastReport企业版源代码6.6.17 支持10.4+ FastReport 简化管理工具2.0

## 资源描述

本仓库提供FastReport 6.6.17企业版源代码，适用于Delphi 7和Delphi 27（10.4 Sydney）。此外，还包含FastReport简化管理工具2.0版本，由xander.xiao@gmail.com开发，发布于2020年5月27日。

### 什么是包简化管理？

FastReport包含一系列设计包文件，手动安装这些包文件非常繁琐。为了简化这一过程，我们提供了一个解决方案，该方案不仅适用于FastReport，还可以应用于任何包管理。

### 解决方案概述

将所有包文件复制到一个由环境变量`%ProjectHome%`命名的文件夹中，其结构如下：

- `%ProjectHome%\Bin`：存放所有包的BPL文件（运行时和设计时文件）
- `%ProjectHome%\LibD7`：存放Delphi 7编译的单元文件和资源文件（如dcu、dcp、dfm、res等）
- `%ProjectHome%\LibD26`：存放Delphi XE 10 Rio编译的单元文件和资源文件（如dcu、dcp、dfm、res等）

每个Delphi版本相关的文件夹可能包含平台（如Win32、Win64等）和配置（如release或debug）指定的子文件夹。之后，双击REG文件以导入Delphi已知的设计时包。

### 工具包包含内容

1. **资源翻译**：
   - 由`res\FR4Trans.exe`、`res\frccEx.exe`和`res\Chinese\@Deploy.bat`提供。
   - 除了中文，还可以支持其他语言。

2. **包简化管理**：
   - 由`@DelUnUsedFiles.bat`、`@Deploy.bat`、`@BuildAllPackages.bat`和`quickInstall`文件夹中的REG文件实现。

### 使用说明

**步骤0**：备份您的FastReport源代码，然后将本文件夹中的所有文件复制到FastReport主文件夹中。

**步骤1**：执行`recompile.exe`以生成指定版本相关的文件夹和文件（首先重新编译所有包，然后更改语言为中文或其他语言）。

**步骤2**：执行`@DelUnUsedFiles.bat`以删除步骤1生成的文件夹中的未使用文件。

**步骤3**：执行`@Deploy.bat`将所有文件部署到项目主文件夹中。

**步骤4**：双击`quickInstall`文件夹中的reg文件，在Delphi IDE中安装设计时BPLs（假设您的`ProjectHome`是`D:\Projects`，您可以根据需要更改）。

**步骤5**（可选）：如果修改了步骤1生成的文件夹中的任何文件，可以执行自定义的`@BuildAllPackages.bat`重新编译所有包文件，而不是使用`recompile.exe`重新编译所有包。

**步骤6**（可选）：如果需要格式化的中文资源代码文件，可以执行`res\chinese\@deploy.bat`，在此之前可以执行`res\FR4Trans.exe`以您喜欢的方式进行翻译。您可以将`res\chinese\@deploy.bat`复制到其他语言文件夹中。

### 注意事项

所有源代码均包含在内，您可以自由修改。

## 下载链接

[FastReport企业版源代码6.6.17支持10.4FastReport简化管理工具2.0](https://pan.quark.cn/s/29a057c7cfb8)