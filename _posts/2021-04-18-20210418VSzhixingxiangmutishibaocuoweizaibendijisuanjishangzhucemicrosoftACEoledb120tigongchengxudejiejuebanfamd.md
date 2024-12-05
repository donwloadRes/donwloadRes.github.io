---
layout: post
title: "VS执行项目提示报错未在本地计算机上注册microsoftACEoledb120提供程序的解决办法"
date:   2024-12-01
tags: [ACE,microsoft,oledb.12,Access,32]
comments: true
author: admin
---
# VS执行项目提示报错“未在本地计算机上注册“microsoft.ACE.oledb.12.0”提供程序”的解决办法

## 问题描述
在使用Visual Studio执行项目时，可能会遇到以下错误提示：
```
未在本地计算机上注册“microsoft.ACE.oledb.12.0”提供程序
```
此错误通常发生在尝试使用Microsoft Access数据库引擎（ACE OLEDB 12.0）访问数据库文件时。

## 解决办法
以下是解决该问题的详细步骤：

### 1. 下载并安装AccessDatabaseEngine
首先，需要下载并安装Microsoft Access Database Engine。根据你的系统位数（32位或64位），选择相应的版本进行下载。

- **64位系统**：下载并安装`AccessDatabaseEngine_X64.exe`。
- **32位系统**：下载并安装`AccessDatabaseEngine_X86.exe`。

### 2. 设置项目目标平台
在Visual Studio中，右键点击你的项目，选择“属性”，然后将“目标平台”设置为与你的系统位数一致。例如，如果你的系统是64位的，则将目标平台设置为“x64”。

### 3. 配置安装程序（可选）
如果你正在制作安装程序，还需要在安装文件的项目属性中，将`TargetPlatform`设置为与系统位数一致，并重新生成安装文件。

### 4. 重启Visual Studio
完成上述步骤后，关闭并重新启动Visual Studio，然后再次尝试执行项目。

## 注意事项
- 确保下载的Access Database Engine版本与你的系统位数匹配。
- 如果你使用的是64位系统，但项目是32位的，可能需要安装32位版本的Access Database Engine。

通过以上步骤，你应该能够解决“未在本地计算机上注册‘microsoft.ACE.oledb.12.0’提供程序”的问题。

## 下载链接

[VS执行项目提示报错未在本地计算机上注册microsoft.ACE.oledb.12.0提供程序的解决办法分享](https://pan.quark.cn/s/595006c6d4fd)