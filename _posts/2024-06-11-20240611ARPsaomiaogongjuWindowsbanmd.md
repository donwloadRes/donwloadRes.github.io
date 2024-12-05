---
layout: post
title: "ARP扫描工具  Windows版"
date:   2021-08-25
tags: [ARP,Windows,arp,scan,扫描]
comments: true
author: admin
---
# ARP扫描工具 - Windows版

## 简介

本仓库提供了一个适用于Windows操作系统的ARP扫描工具，名为`arp-scan-windows`。该工具能够向整个特定局域网发送ARP请求，帮助用户快速识别局域网内的设备。

## 功能特点

- **支持平台**：适用于Windows操作系统，支持x86和x64架构。
- **目标指定**：可以通过指定目标IP地址或IP段来发送ARP请求。
- **简单易用**：命令行操作，方便快捷。

## 使用方法

### 命令格式

```bash
arp-scan -t [目标IP/斜线] 或 [目标IP]
```

### 示例

1. 扫描整个`192.168.1.0/24`网段：

   ```bash
   arp-scan -t 192.168.1.1/24
   ```

2. 扫描单个IP地址`172.20.10.1`：

   ```bash
   arp-scan -t 172.20.10.1
   ```

## 注意事项

- 请确保在使用该工具时遵守相关法律法规，不要用于非法用途。
- 该工具仅适用于Windows操作系统，不支持其他平台。

## 下载

请在仓库中找到相应的资源文件进行下载。

## 反馈与支持

如果您在使用过程中遇到任何问题或有任何建议，欢迎通过仓库的Issues功能进行反馈。我们将尽快为您提供支持。

## 下载链接

[ARP扫描工具-Windows版](https://pan.quark.cn/s/e91d02286dda)