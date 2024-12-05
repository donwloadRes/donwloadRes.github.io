---
layout: post
title: "三国志11原版在Windows 11上的成功运行指南"
date:   2021-11-21
tags: [11,Windows,secdrv,cmd,bcdedit]
comments: true
author: admin
---
# 三国志11原版在Windows 11上的成功运行指南

本文详细介绍了如何在Windows 11系统上成功运行原版三国志11的步骤。通过以下步骤，您可以解决游戏在Windows 11上的兼容性问题，确保游戏能够顺利运行。

## 主要步骤

### 1. 安装游戏
- **文件夹命名**：安装游戏时，文件夹的名字最好使用英文，以避免潜在的兼容性问题。
- **恢复启动程序**：安装完成后，游戏可能会隐藏启动程序。您可以通过右键属性，选择兼容性，并设置兼容模式为Windows 7，禁用全屏模式，并以管理员身份运行。

### 2. 引入驱动程序secdrv.sys
- **放置驱动文件**：将下载的secdrv.sys文件放到 `C:\WINDOWS\system32\drivers` 文件夹中。
- **启动驱动程序**：以管理员身份启动命令提示符（cmd），输入以下代码：
  ```
  sc config secdrv start= auto
  ```
  您还可以输入 `sc start secdrv` 确认服务是否已成功打开，或输入 `sc stop secdrv` 关闭服务。

### 3. 处理数字签名问题
- **禁用驱动程序强制签名**：如果遇到数字签名问题，可以在cmd中输入以下命令禁用驱动程序强制签名：
  ```
  bcdedit.exe /set nointegritychecks on
  ```
  取消禁用命令为：
  ```
  bcdedit.exe /set nointegritychecks off
  ```

### 4. 关闭测试模式
- **关闭测试模式**：如果桌面左下角显示测试模式，可能会导致其他游戏无法运行。您可以在cmd中输入以下代码关闭测试模式：
  ```
  bcdedit /set testsigning off
  ```
  开启测试模式的命令为：
  ```
  bcdedit /set testsigning on
  ```

## 注意事项
- **管理员权限**：所有cmd命令都需要以管理员身份运行。
- **路径设置**：在修改InstallInfo文件时，确保路径设置正确。

通过以上步骤，您应该能够在Windows 11上成功运行原版三国志11。如果在过程中遇到任何问题，请参考原文或寻求进一步的技术支持。

## 下载链接

[三国志11原版在Windows11上的成功运行指南分享](https://pan.quark.cn/s/f331a488e12c)