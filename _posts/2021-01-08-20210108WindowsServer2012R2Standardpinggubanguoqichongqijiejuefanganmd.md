---
layout: post
title: "Windows Server 2012 R2 Standard 评估版过期重启解决方案"
date:   2024-04-21
tags: [激活,过期,Standard,评估,重启]
comments: true
author: admin
---
# Windows Server 2012 R2 Standard 评估版过期重启解决方案

本文档旨在提供关于Windows Server 2012 R2 Standard评估版过期后自动重启的解决方案。评估版在安装后有10天的激活时间，过期后每隔一个小时会自动关机。通过将评估版转换为正式版并进行KMS激活，可以解决这一问题。

## 解决方案步骤

### 1. 查看当前系统版本
以管理员权限运行命令提示符（cmd），输入以下命令查看当前系统版本：
```
DISM /online /Get-CurrentEdition
```

### 2. 转换为正式版
获取一个Standard版本的Product Key，然后在命令提示符中输入以下命令进行转换：
```
DISM /online /Set-Edition:ServerStandard /ProductKey:yourkey /AcceptEula
```

### 3. KMS激活
转换完成后，使用KMS激活工具进行激活。双击激活工具，点击激活，等待激活完成。

### 4. 重启计算机
操作完成后，按照命令提示符中的指示重启计算机，系统将正常运行。

通过以上步骤，您可以将Windows Server 2012 R2 Standard评估版转换为正式版，并解决过期后自动重启的问题。

## 下载链接

[WindowsServer2012R2Standard评估版过期重启解决方案分享](https://pan.quark.cn/s/a99da9570c94)