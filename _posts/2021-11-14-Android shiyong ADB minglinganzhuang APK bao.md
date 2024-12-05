---
layout: post
title: "Android 使用 ADB 命令安装 APK 包"
date:   2024-08-19
tags: [adb,bash,ADB,shell,Android]
comments: true
author: admin
---
# Android 使用 ADB 命令安装 APK 包

本文将详细介绍如何使用 ADB（Android Debug Bridge）命令在 Android 设备上安装 APK 包。ADB 是一个功能强大的命令行工具，允许开发者与 Android 设备进行通信，进行应用的安装、调试等操作。

## 使用步骤

### 1. 下载并安装 ADB 工具

首先，你需要下载并安装 ADB 工具。如果你已经安装了 ADB，可以跳过此步骤。

### 2. 检查 ADB 工具是否安装成功

在命令行中输入以下命令，检查 ADB 工具是否安装成功：

```bash
adb version
```

如果显示版本号，则表示安装成功。

### 3. 检查连接设备

1. 使用数据线连接手机，并在手机中打开 USB 调试模式。不同手机的设置路径可能不同，通常在：设置 → 开发者选项 → USB 调试和 USB 安装、USB 调试（安全设置）。
2. 在命令行窗口中输入以下命令，检查设备是否连接成功：

```bash
adb devices
```

如果显示设备编号，则表示连接成功。

### 4. 使用命令行安装 APK 包

1. 如果连接了多个设备，需要指定设备：

```bash
adb -s 设备编号 install apk的完整路径
```

如果是单设备，可以直接输入：

```bash
adb install apk的完整路径
```

例如：

```bash
adb install C:\Users\31210\Downloads\XXX.apk
```

2. 覆盖安装：

```bash
adb install -r xxxx.apk
```

3. 卸载包：

```bash
adb uninstall 安装包包名
```

## 彩蛋

- 显示第三方应用：

```bash
adb shell pm list package -3
```

- 降级安装 APK：

```bash
adb install -d apk的完整路径
```

- 查看运行 APK 的包名：

```bash
adb shell dumpsys window | grep mCurrentFocus
```

- 查看 Activity 任务栈：

```bash
adb shell dumpsys activity activities
```

- 查看堆的分配情况：

```bash
adb shell dumpsys meminfo <package_name>
```

- 查看应用信息：

```bash
adb shell dumpsys package <package_name>
```

- 获取设备型号：

```bash
adb shell getprop ro.product.model
```

- 获取设备的 Android 系统版本：

```bash
adb shell getprop ro.build.version.release
```

- 获取设备屏幕分辨率：

```bash
adb shell wm size
```

- 获取设备屏幕密度（单位：dpi）：

```bash
adb shell wm density
```

- 使用 ADB 在手机和电脑间传输文件：

```bash
adb pull <手机路径> <本机路径> （从手机中拉取信息到本地电脑上）
adb push <本机路径> <手机路径> （从本地电脑推送信息到手机上）
```

通过以上步骤，你可以轻松使用 ADB 命令在 Android 设备上安装和管理 APK 包。

## 下载链接

[Android使用ADB命令安装APK包分享](https://pan.quark.cn/s/1437ec917e7a)