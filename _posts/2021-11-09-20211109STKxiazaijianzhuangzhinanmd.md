---
layout: post
title: "STK 下载及安装指南"
date:   2022-12-26
tags: [STK,Matlab,安装,文件,下载]
comments: true
author: admin
---
# STK 下载及安装指南

本文档旨在提供STK（Satellite Tool Kit）软件的下载及安装指南。STK是一款用于航天、卫星等领域的商业软件，广泛应用于航天任务的规划、分析和仿真。

## 一、STK 下载

STK软件的下载包可以通过多种渠道获取，本文以STK 11.0版本为例进行说明。请确保下载的版本与您的系统兼容。

## 二、STK 安装

### 1. 安装顺序

- **Matlab 安装**：如果您计划在后续使用STK与Matlab进行互联，建议先安装Matlab，然后再安装STK。这样可以确保STK在安装时自动配置Matlab的相关文件和数据。
- **STK 安装**：根据您的系统选择32位或64位版本进行安装。本文以64位版本为例。

### 2. 安装步骤

1. **下载安装包**：下载完成后，双击`STK1101OneClickInstall.exe`应用程序进行安装。
2. **配置文件复制**：
   - 将`STK 11\bin`目录下的所有文件复制到`C:\Program Files\AGI\STK 11\bin`，并替换相同文件。
   - 将`STK_11.0.lic`文件复制到`C:\ProgramData\AGI\LicenseData`。
   - 将`AglicVbinterface.dll`文件从`LicenseManager\bin`复制到`C:\Program Files (x86)\AGI\License Manager\bin`。
3. **配置许可证**：
   - 双击`STK 11`应用程序，选择`Manage Licenses`。
   - 在`License Directories`中点击添加文件，选择`C:\ProgramData\AGI\LicenseData`。
   - 添加完成后点击`Exit`。

### 3. 注意事项

- **隐藏文件夹**：如果找不到`C:\ProgramData`文件夹，可以通过`文件管理器` -> `查看` -> `选项` -> `查看` -> `隐藏文件和文件夹`，选择`显示隐藏的文件、文件夹和驱动器`。

### 4. STK 与 Matlab 互联

1. **安装Matlab连接器**：打开下载的安装包，点击`Matlab_Connectors`，双击`setup.exe`应用程序，一路点击确定。
2. **配置互联**：打开STK，新建一个文件页面，选择`Edit` -> `Preferences`，选择`Matlab`，观察`Connectable Version`和`Version with installed Connectors`，确保版本匹配。

## 三、总结

本文档详细介绍了STK软件的下载及安装过程，包括与Matlab的互联配置。希望对您的安装过程有所帮助。

## 下载链接

[STK下载及安装指南](https://pan.quark.cn/s/0d37311ca7d9)