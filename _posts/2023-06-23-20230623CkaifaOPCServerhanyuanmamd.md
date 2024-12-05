---
layout: post
title: "C开发OPC Server含源码"
date:   2024-02-29
tags: [C#,OPC,Server,WtOPCSvr,文件]
comments: true
author: admin
---
# C#开发OPC Server含源码

## 资源描述

本资源提供了一个完整的C#开发OPC Server的源码和相关文档，适用于32位和64位操作系统。通过本资源，您可以学习如何使用C#开发一个OPC Server，并了解相关的配置和使用方法。

## 资源内容

- **OPC Server源码**：包含一个完整的C#工程，使用VS2005编写，支持更高版本的Visual Studio。
- **WtOPCSvr.dll**：OPC Server的核心DLL文件，需要拷贝到执行目录中。
- **文档**：
  - `WTOPCSvr+使用手册.doc`：详细介绍了WtOPCSvr的使用方法。
  - `WTOPCSVRDLL使用说明中文.doc`：介绍了如何在VB中使用WtOPCSvr，并提供了转换为C#的示例。
- **批处理文件**：`setupxp.bat`，用于在32位操作系统上安装OPCdist库文件。如果是64位系统，需要手动修改该文件。
- **注册码**：`SerialNumber.txt`，包含WtOPCSvr.dll的注册码，但未提供注册方法，建议上网搜索相关信息。

## 使用步骤

1. **环境准备**：
   - 如果是32位操作系统，直接执行`opcdist`目录下的`setupxp.bat`文件。
   - 如果是64位操作系统，请手动修改`setupxp.bat`文件以适应64位环境。

2. **工程准备**：
   - 创建一个新的C#工程，并将`Wtopcsvr9.0\Wtopcsvr9.0\WtOPCSvr.dll`拷贝到工程的执行目录中。

3. **导入工程**：
   - 打开压缩包中的`opcservertest`工程，该工程使用VS2005编写，支持更高版本的Visual Studio。

4. **注册与取消注册**：
   - `UpdateRegistry`函数用于注册服务。
   - `UnregisterServer`函数用于取消注册。

5. **注意事项**：
   - C#生成的可执行文件必须是32位，否则无法正常加载DLL文件。
   - 工程中已经定义并使用了常用的函数，您可以参考`WTOPCSVRDLL使用说明中文.doc`将VB的示例转换为C#。

## 其他说明

- 本资源中的大部分文件来自CSDN网站，WtOPCSvr.dll应该是注册版的，注册码在`SerialNumber.txt`中，但未提供注册方法，建议上网搜索相关信息。
- 如果您在使用过程中遇到问题，可以参考文档或在网上搜索相关解决方案。

## 致谢

感谢原作者的辛勤工作和分享，希望本资源能够帮助您顺利开发C# OPC Server。

## 下载链接

[C开发OPCServer含源码](https://pan.quark.cn/s/0b541fe5c3a8)