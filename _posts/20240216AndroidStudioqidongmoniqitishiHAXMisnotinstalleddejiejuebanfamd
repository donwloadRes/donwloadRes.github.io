---
layout: post
title: "Android Studio启动模拟器提示“HAXM is not installed”的解决办法"
date:   2022-01-16
tags: [HAXM,Android,模拟器,Studio,installed]
comments: true
author: admin
---
# Android Studio启动模拟器提示“HAXM is not installed”的解决办法

## 简介
在使用Android Studio开发Android项目时，启动自带的模拟器时可能会遇到“HAXM is not installed”的错误提示。本文将详细介绍如何解决这一问题，确保模拟器能够正常运行。

## 问题描述
当尝试在Android Studio中启动模拟器时，可能会遇到以下错误提示：
- No USB devices or running emulator detected
- Intel HAXM is required to run this AVD
- HAXM is not installed

## 解决步骤

### 1. 检查虚拟化技术是否开启
首先，确保你的电脑已经开启了虚拟化技术。可以通过以下步骤检查和开启：
- 重启电脑并进入BIOS界面
- 找到Virtual Technology或VT-x字样，将其设置为Enable

### 2. 检查HAXM插件是否已下载
在Android Studio中，打开Settings界面，搜索SDK，然后在SDK Tools中检查是否存在HAXM插件。如果没有，请下载并安装。

### 3. 手动安装HAXM
如果自动下载失败，可以手动安装HAXM插件：
- 找到SDK安装路径，通常在`sdk\extras\intel\Hardware_Accelerated_Execution_Manager\`目录下
- 双击运行`IntelHaxm.exe`，按照提示完成安装

### 4. 检查CPU类型
HAXM插件只支持Intel CPU类型。如果你的电脑使用的是AMD CPU，将无法使用HAXM。可以通过以下步骤检查CPU类型：
- 打开计算机——>属性，查看CPU类型

### 5. 添加代理
如果下载过程中遇到网络问题，可以尝试添加代理，支持访问Google等国外网站。

## 总结
通过以上步骤，你应该能够解决Android Studio启动模拟器时提示“HAXM is not installed”的问题。如果仍然无法解决，建议检查电脑硬件配置或尝试使用真机进行测试。

## 下载链接

[AndroidStudio启动模拟器提示HAXMisnotinstalled的解决办法分享](https://pan.quark.cn/s/b3cd2de31222)