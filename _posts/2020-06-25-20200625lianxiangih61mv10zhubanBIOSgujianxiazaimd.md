---
layout: post
title: "联想ih61m v10 主板BIOS固件下载"
date:   2020-02-29
tags: [BIOS,固件,刷写,ih61m,v1.0]
comments: true
author: admin
---
# 联想ih61m v1.0 主板BIOS固件下载

## 资源描述

本仓库提供联想ih61m v1.0主板的BIOS固件下载，版本为9QKT39A。该固件已添加Nvme驱动，适用于所有BIOS版本信息以9qkt开头的联想ih61m v1.0主板。

## 固件特性

- **版本号**: 9QKT39A
- **Nvme驱动**: 已添加Nvme驱动支持
- **兼容性**: 适用于所有BIOS版本信息以9qkt开头的联想ih61m v1.0主板

## 更新日志

- **9QKT37A/9QJT37A**: 修复了在没有USB ODD时卡在启动画面的问题。
- **9QKT38A/9QJT38A**: 更新了CPU微码，从206A7更新到28h。
- **9QKT39A/9QJT39A**: 防止在连接某些USB设备时等待时间过长。

## 刷写步骤

1. 在Windows或PE环境下运行`afuwingui.exe`。
2. 点击`Open`，选择`nvrom.rom`文件。
3. 点击`Flash`开始刷写BIOS。
4. 等待几分钟，刷写完成后点击`Exit`退出。

**注意**: 刷写过程最多可能需要3分钟，请勿在此期间关机或重启。

## 重要提示

- **Nvme固态仅支持UEFI启动**。
- 刷写过程中请勿断电或重启，以免造成主板损坏。

## 免责声明

刷写BIOS存在一定风险，请确保您了解相关操作并自行承担风险。本仓库提供的固件仅供学习和研究使用，不承担任何因使用本固件造成的损失。

## 下载链接

[联想ih61mv1.0主板BIOS固件下载](https://pan.quark.cn/s/d85d88563e59)