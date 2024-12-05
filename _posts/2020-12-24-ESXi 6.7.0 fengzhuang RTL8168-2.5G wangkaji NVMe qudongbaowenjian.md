---
layout: post
title: "ESXi 6.7.0 封装 RTL8168-2.5G 网卡及 NVMe 驱动包文件"
date:   2021-02-08
tags: [ESXi,驱动,网卡,文件,NVMe]
comments: true
author: admin
---
# ESXi 6.7.0 封装 RTL8168/2.5G 网卡及 NVMe 驱动包文件

本仓库提供了一个资源文件，用于在 ESXi 6.7.0 系统中封装 RTL8168 和 RTL8125BG 网卡驱动，以及 NVMe 驱动。通过使用这些驱动包文件，您可以确保在 ESXi 6.7.0 环境中正常使用这些硬件设备。

## 资源文件列表

- **ESXi-Customizer-PS-v2.6.0.ps1**：操作文件，用于自定义 ESXi 镜像。
- **net55-r8168-8.045a-napi.x86_64.vib**：RTL8168 网卡驱动文件。
- **Realtek_bootbank_net-r8125_9.007.01-1.vib**：RTL8125BG 2.5G 网卡驱动文件。
- **VMware_bootbank_vmware-esx-esxcli-nvme-plugin_1.2.0.32-0.0.8169922.vib**：NVMe 驱动文件。

## 使用说明

1. **下载资源文件**：请从本仓库下载所需的驱动包文件。
2. **运行 ESXi-Customizer-PS-v2.6.0.ps1**：使用该脚本自定义 ESXi 镜像，将下载的驱动文件集成到 ESXi 安装镜像中。
3. **安装 ESXi 系统**：使用自定义后的 ESXi 镜像进行系统安装。
4. **验证驱动**：安装完成后，验证 RTL8168、RTL8125BG 网卡及 NVMe 驱动是否正常工作。

## 注意事项

- 请确保在操作前备份重要数据，以防操作失误导致数据丢失。
- 操作过程中请严格按照步骤进行，避免出现错误。
- 如有任何问题，请参考相关文档或寻求专业人士的帮助。

## 更新日志

- **2023-10-01**：初始版本发布，包含 RTL8168、RTL8125BG 及 NVMe 驱动文件。

## 联系我们

如有任何问题或建议，请通过 GitHub 仓库的 Issues 页面联系我们。

## 下载链接

[ESXi6.7.0封装RTL81682.5G网卡及NVMe驱动包文件](https://pan.quark.cn/s/9bae5582667b)