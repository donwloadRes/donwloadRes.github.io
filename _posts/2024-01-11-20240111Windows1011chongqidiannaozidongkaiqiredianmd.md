---
layout: post
title: "Windows 1011 重启电脑自动开启热点"
date:   2023-11-30
tags: [开启,Windows,热点,快捷方式,手动]
comments: true
author: admin
---
# Windows 10/11 重启电脑自动开启热点

## 简介

本资源文件旨在帮助用户在Windows 10或Windows 11系统中设置电脑在重启后自动开启热点功能。通过使用提供的脚本文件，用户可以轻松实现这一功能，无需每次手动开启热点。

## 使用步骤

### 1. 下载文件

下载提供的两个脚本文件，并将其放置在任意磁盘路径下。

### 2. 打开系统运行PS1文件限制

由于Windows默认关闭了PowerShell脚本文件（.ps1）的运行权限，需要手动开启。具体步骤如下：

1. 在开始菜单中搜索“PowerShell”，并以管理员身份运行。
2. 输入以下命令并确认：
   ```
   set-executionpolicy remotesigned
   ```

### 3. 创建桌面快捷方式

为`wifi.bat`文件创建桌面快捷方式，方便后续操作。

### 4. 测试热点开启

1. 先手动关闭热点。
2. 双击`wifi.bat`文件的快捷方式，观察是否有黑框闪现。
3. 检查热点是否成功开启。

### 5. 将快捷方式加入开机自启

将创建的快捷方式放入以下路径，以实现开机自启：
```
C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Startup
```

## 注意事项

- 确保电脑支持开启热点功能。
- 密码设置至少需要8位。

通过以上步骤，用户可以在每次重启电脑后自动开启热点，无需手动操作。

## 下载链接

[Windows1011重启电脑自动开启热点](https://pan.quark.cn/s/1eb6f6a9f4af)