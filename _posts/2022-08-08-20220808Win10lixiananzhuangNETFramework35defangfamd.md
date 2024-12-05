---
layout: post
title: "Win10离线安装NET Framework 35的方法"
date:   2023-11-18
tags: [NET,Framework,3.5,Windows,安装]
comments: true
author: admin
---
# Win10离线安装.NET Framework 3.5的方法

本文介绍了如何在Windows 10系统中离线安装.NET Framework 3.5的方法，并附带了2022年3月22日的离线安装包。

## 背景

在Windows 10系统中，某些软件可能需要.NET Framework 3.5的运行环境。如果系统默认安装的是4.0以上的版本，当软件需要.NET Framework 3.5时，安装过程中可能会发生报错。本文提供了一种离线安装.NET Framework 3.5的方法，以解决此类问题。

## 安装步骤

### 1. 下载离线安装包

首先，需要下载.NET Framework 3.5的离线安装包。该安装包包含了安装.NET Framework 3.5所需的所有文件。

### 2. 关闭杀毒软件和电脑管理工具

在安装过程中，建议关闭所有杀毒软件和电脑管理工具，如360安全卫士，以避免安装过程中出现干扰。

### 3. 打开Windows Update服务

确保Windows Update服务处于运行状态，以便系统能够正常更新和安装所需的组件。

### 4. 关闭.NET Framework 4.7高级服务（可选）

在安装.NET Framework 3.5之前，可以关闭.NET Framework 4.7高级服务，以避免可能的冲突。

### 5. 使用命令行安装

以管理员身份打开命令提示符（CMD），输入以下命令进行安装：

```
dism.exe /online /enable-feature /featurename:netfx3 /Source:C:\Windows\sxs
```

其中，`C:\Windows\sxs`是离线安装包的存放路径。等待安装进度达到100%，显示“操作成功完成”即可。

### 6. 完成安装

安装成功后，可以重新打开之前关闭的.NET Framework 4.7高级服务。

## 常见错误及解决方法

- **错误代码0x8024500c**：可能是Windows Update服务损坏，建议重新安装Windows Update服务。
- **错误代码0x80240440**：参考相关文档进行修复。
- **错误代码0x80240438**：由于Windows账户加入了域，参考相关文档进行解决。
- **错误代码0x80096004**：DISM工具失败，参考相关文档进行修复。

## 总结

通过以上步骤，您可以在Windows 10系统中成功离线安装.NET Framework 3.5，解决软件安装过程中可能遇到的依赖问题。

## 下载链接

[Win10离线安装.NETFramework3.5的方法](https://pan.quark.cn/s/c50a815c5e28)