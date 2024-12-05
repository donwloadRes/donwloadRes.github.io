---
layout: post
title: "USB权限申请工具"
date:   2021-09-15
tags: [USB,intent,权限,putExtra,app]
comments: true
author: admin
---
# USB权限申请工具

## 简介

`usb-permission-issuer.apk` 是一个用于简化Android设备USB权限申请的工具。通过将该APK文件拷贝到设备的`/system/prv-app`目录下并授予文件权限777，你可以在你的应用程序中向`usb-permission-issuer`发送广播，从而自动获取USB权限，避免在使用USB设备时弹出授权对话框。

## 使用方法

### 1. 安装与授权

1. 将 `usb-permission-issuer.apk` 文件拷贝到设备的 `/system/prv-app` 目录下。
2. 使用命令行工具或文件管理器，将该文件的权限设置为 `777`。

### 2. 发送广播申请USB权限

在你的应用程序中，通过发送广播来申请USB权限。以下是两种发送广播的方式：

#### 方式一：通过设备类和子类申请

```java
Intent intent = new Intent();
intent.setAction("ACTION_USB_PERMISSION_ISSUER");
intent.putExtra("packageName", "你的app-package");
intent.putExtra("deviceClass", 1569); // device_filter.xml 里的字段
intent.putExtra("deviceSubclass", 8963);
// 发送广播
sendBroadcast(intent);
```

#### 方式二：通过供应商ID和产品ID申请

```java
Intent intent = new Intent();
intent.setAction("ACTION_USB_PERMISSION_ISSUER");
intent.putExtra("packageName", "你的app-package");
intent.putExtra("vendorId", 1569); // device_filter.xml 里的字段
intent.putExtra("productId", 8963);
// 发送广播
sendBroadcast(intent);
```

### 3. 使用USB设备

在成功申请USB权限后，你的应用程序在使用USB设备时将不再弹出授权对话框，可以直接进行USB操作。

## 注意事项

- 确保 `usb-permission-issuer.apk` 文件已正确拷贝到 `/system/prv-app` 目录下，并且权限设置为 `777`。
- 在发送广播时，确保 `packageName` 字段填写正确，即你的应用程序的包名。
- `deviceClass`、`deviceSubclass`、`vendorId` 和 `productId` 字段需要根据你的设备配置进行填写，具体值可以从 `device_filter.xml` 文件中获取。

## 适用场景

该工具适用于需要在Android设备上频繁使用USB设备的应用程序，特别是在自动化测试、设备管理等场景中，可以有效减少用户手动确认USB权限的步骤，提升用户体验。

## 下载链接

[USB权限申请工具](https://pan.quark.cn/s/90270ac74085)