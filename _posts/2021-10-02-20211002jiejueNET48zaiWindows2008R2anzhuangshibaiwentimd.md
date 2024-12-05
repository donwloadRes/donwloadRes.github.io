---
layout: post
title: "解决NET 48 在 Windows 2008 R2 安装失败问题"
date:   2024-05-17
tags: [安装,NET,4.8,补丁,安装包]
comments: true
author: admin
---
# 解决.NET 4.8 在 Windows 2008 R2 安装失败问题

在尝试于 Windows Server 2008 R2 系统上安装 .NET Framework 4.8 时，用户可能会遇到两个常见的安装失败情况。本文将指导您如何解决这两个问题，确保成功安装。

## 问题一：下载组件超时

初次尝试通过 `.NET 4.8 的 web 安装包` (如 [ndp48-web.exe](https://download.visualstudio.microsoft.com/download/pr/2d6bb6b2-226a-4baa-bdec-798822606ff1/9b7b8746971ed51a1770ae4293618187/ndp48-web.exe)) 进行安装时，可能会因为网络问题导致下载组件超时而失败。

### 解决方案：
- 使用 **离线安装包** (例如，[从这里获取](https://go.microsoft.com/fwlink/?linkid=2088631)) 避免在线依赖性问题。

## 问题二：时间戳签名和证书验证失败

当切换到使用离线安装包进行安装时，可能会遇到错误提示：“时间戳签名和%2F或证书无法验证或已损坏。” 错误代码提及的是 `0x80096005`。

### 原因及解决方案：
此问题通常是因为系统缺少必要的安全更新。需要先应用特定补丁，补丁信息如下：
- **补丁名**：Windows6.1-KB2813430-x64.msu
- **获取方式**：请直接搜索并下载 [Windows6.1-KB2813430-x64.msu](https://download.microsoft.com/download/F/D/B/FDB0E76D-2C15-45D1-A49B-BFB405008569/Windows6.1-KB2813430-x64.msu)，这是一个适用于 Windows 2008 R2 的关键更新，能够修复证书验证问题。

### 完整步骤总结：
1. **下载并安装补丁**：首先确保系统已安装最新的更新，特别关注 KB2813430 补丁。
2. **重新安装 .NET Framework 4.8**：在补丁安装并重启计算机后，再次尝试使用离线安装包安装 .NET 4.8。

按照上述步骤操作后，应能顺利解决安装过程中的问题，并成功部署 .NET Framework 4.8 到您的 Windows 2008 R2 服务器上。

## 下载链接

[解决.NET4.8在Windows2008R2安装失败问题](https://pan.quark.cn/s/b8f9ad7ebcb5)