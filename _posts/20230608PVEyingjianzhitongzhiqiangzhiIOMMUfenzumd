---
layout: post
title: "PVE硬件直通之强制IOMMU分组"
date:   2023-12-08
tags: [IOMMU,分组,内核,PVE,配置]
comments: true
author: admin
---
# PVE硬件直通之强制IOMMU分组

本资源文件提供了关于如何在Proxmox VE（PVE）环境中强制配置IOMMU分组的详细指南。通过强制IOMMU分组，可以提高PCIe设备的安全性，防止非法的P2P通信，保护系统免受潜在攻击。

## 内容概述

1. **检查是否直接支持IOMMU分组**
   - 通过`lspci -vv`命令检查PCI设备是否直接支持IOMMU分组。
   - 如果设备支持ACS（Access Control Services），则可以直接配置IOMMU分组。

2. **配置IOMMU分组**
   - 编辑`/etc/modules`文件，添加必要的模块。
   - 修改`/etc/default/grub`文件，添加`amd_iommu=on pcie_acs_override=downstream,multifunction`参数。
   - 更新GRUB引导和initramfs。

3. **更新内核**
   - 对于不直接支持ACS的设备，需要更新内核以启用IOMMU分组。
   - 提供编译好的PVE内核文件，用户可以通过更新内核来实现IOMMU分组。

## 使用说明

1. **下载资源文件**
   - 下载本仓库中的资源文件，包含必要的配置文件和内核更新包。

2. **配置IOMMU分组**
   - 按照指南中的步骤，编辑相关配置文件并更新内核。
   - 重启系统以应用更改。

3. **验证配置**
   - 使用`lspci -vv`命令检查设备是否已正确配置IOMMU分组。

## 注意事项

- 在配置IOMMU分组前，请确保备份重要数据。
- 更新内核可能会影响系统稳定性，建议在测试环境中进行操作。

通过本指南，您可以有效地配置PVE环境中的IOMMU分组，提升系统的安全性和稳定性。

## 下载链接

[PVE硬件直通之强制IOMMU分组](https://pan.quark.cn/s/6d641d4ca0a1)