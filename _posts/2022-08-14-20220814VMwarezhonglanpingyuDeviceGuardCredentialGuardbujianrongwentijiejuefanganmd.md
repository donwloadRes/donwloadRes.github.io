---
layout: post
title: "VMware中蓝屏与Device Guard-Credential Guard不兼容问题解决方案"
date:   2020-04-10
tags: [Guard,Device,VMware,Credential,解决方案]
comments: true
author: admin
---
# VMware中蓝屏与Device Guard/Credential Guard不兼容问题解决方案

## 简介
本资源文件旨在解决在VMware中配置Linux系统时遇到的蓝屏问题，以及与Device Guard/Credential Guard不兼容的问题。通过本文提供的解决方案，您可以顺利解决这些问题，确保VMware虚拟机的正常运行。

## 问题描述
1. **蓝屏问题**：在VMware中配置Linux系统后，开机安装时电脑直接蓝屏。
2. **Device Guard/Credential Guard不兼容问题**：在解决蓝屏问题后，可能会出现Device Guard/Credential Guard与VMware不兼容的情况。

## 解决方案

### 问题一：蓝屏问题
1. **启用虚拟机平台**：
   - 在Windows搜索栏中输入“启用或关闭Windows功能”。
   - 打开后，勾选“虚拟机平台”选项。

### 问题二：Device Guard/Credential Guard不兼容问题
1. **传统解决方案（不推荐）**：
   - 参考方案一：禁用Device Guard的方法一。
   - 参考方案二：禁用Device Guard的方法二。
   - 关闭设备保护（Device Guard）和Hyper-V，但成功率较低，尤其是在Windows 10家庭版中，可能找不到Device Guard的入口，也没有Hyper-V的选项。

2. **终极解决方案（推荐）**：
   - 使用Geek或CClean卸载并清理旧版本的VMware，确保卸载干净。
   - 安装VMware 16版本。
   - 成功原因：VMware 16版本中加入了对电脑系统的Device Guard的检测，并提供了一步到位的解决方案。

## 注意事项
- 在执行任何操作前，请确保备份重要数据。
- 禁用Device Guard/Credential Guard可能会降低系统的安全性，请谨慎操作。

通过以上步骤，您应该能够解决VMware中蓝屏与Device Guard/Credential Guard不兼容的问题，确保虚拟机的正常运行。

## 下载链接

[VMware中蓝屏与DeviceGuardCredentialGuard不兼容问题解决方案](https://pan.quark.cn/s/0a157b117a37)