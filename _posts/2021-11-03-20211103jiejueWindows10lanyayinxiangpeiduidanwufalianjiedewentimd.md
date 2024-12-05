---
layout: post
title: "解决Windows 10蓝牙音箱配对但无法连接的问题"
date:   2024-03-28
tags: [蓝牙,连接,音箱,配对,Windows]
comments: true
author: admin
---
# 解决Windows 10蓝牙音箱配对但无法连接的问题

本文介绍了一种解决Windows 10系统中蓝牙设备只能配对无法成功连接的问题。通过下载并使用Bluetooth Command Line Tools，在命令行中运行特定指令，然后重新尝试添加和连接蓝牙设备，以实现正常连接。此方法适用于遇到类似困扰的用户。

## 系统环境
- Windows 10 专业版
- 操作系统内部版本：19043.899

## 问题描述
蓝牙点连接，一直显示已配对，删除设备，再添加进来还是这样。正常情况是，连接后，会听到音箱说“蓝牙已连接”，显示为“已连接的音乐”。

## 解决方法
1. 下载Bluetooth Command Line Tools。
2. 在命令行（win+r-cmd-回车）中输入 `btpair -u`。
3. 点击“添加蓝牙或其他设备”，然后点击连接。

通过以上步骤，您应该能够成功连接蓝牙音箱。如果问题仍然存在，请参考相关技术支持或进一步的故障排除指南。

## 下载链接

[解决Windows10蓝牙音箱配对但无法连接的问题分享](https://pan.quark.cn/s/5ac893ca1576)