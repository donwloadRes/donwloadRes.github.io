---
layout: post
title: "QuectelQConnectManagerLinuxV164 开源仓库"
date:   2023-08-01
tags: [Linux,Quectel,QConnectManager,V1.6,拨号]
comments: true
author: admin
---
# Quectel-QConnectManager-Linux-V1.6.4 开源仓库

## 简介

Quectel-QConnectManager-Linux-V1.6.4 是移远通信提供的一款网卡拨号工具，支持多种拨号协议和驱动，旨在为 Linux 用户提供强大的网络连接管理功能。该工具不仅支持 QMI 和 MBIM 协议拨号，还支持 AT+QNETDEVCTL 拨号方式，适用于多种移远通信的硬件设备。

## 功能特点

- **多协议支持**：支持 QMI、MBIM 和 AT+QNETDEVCTL 拨号协议。
- **广泛的驱动兼容性**：兼容移远通信的 qmi_wwan_q、GobiNet、pcie_mhi、pcie_mhi_mbim 驱动，以及 Linux 内核中的 qmi_wwan、cdc_mbim、cdc_ncm、RNDIS 和 ECM 驱动。
- **高级网络功能**：支持网络聚合、多路 PDN 拨号和网桥等高级网络管理功能。

## 安装与使用

### 安装步骤

1. **克隆仓库**：
   ```bash
   git clone https://github.com/your-repo/Quectel-QConnectManager-Linux-V1.6.4.git
   ```

2. **进入目录**：
   ```bash
   cd Quectel-QConnectManager-Linux-V1.6.4
   ```

3. **编译安装**：
   ```bash
   make
   sudo make install
   ```

### 使用方法

详细的使用方法和命令行参数请参考 `docs/usage.md` 文件。

## 贡献

我们欢迎社区的贡献和反馈。如果您有任何建议或发现了问题，请提交 Issue 或 Pull Request。

## 许可证

本项目采用 [MIT 许可证](LICENSE)。

## 联系我们

如有任何疑问或需要支持，请联系移远通信的技术支持团队。

---

感谢您对 Quectel-QConnectManager-Linux-V1.6.4 的关注和支持！

## 下载链接

[Quectel-QConnectManager-Linux-V1.6.4开源仓库](https://pan.quark.cn/s/060a78ef791b)