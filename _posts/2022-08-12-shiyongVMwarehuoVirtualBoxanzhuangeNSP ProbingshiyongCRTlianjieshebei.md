---
layout: post
title: "使用VMware或VirtualBox安装eNSP Pro并使用CRT连接设备"
date:   2024-02-26
tags: [eNSP,Pro,VMware,网络,CRT]
comments: true
author: admin
---
# 使用VMware或VirtualBox安装eNSP Pro并使用CRT连接设备

本文档旨在指导您如何在VMware或VirtualBox虚拟环境中安装eNSP Pro，以及后续如何使用CRT等终端软件进行设备管理。eNSP Pro是由华为提供的一款强大网络仿真平台，适用于模拟多种华为网络设备，适合网络工程师进行学习和实验。

## VMware安装步骤概述：

1. **下载eNSP Pro镜像文件**：首先从官方或授权渠道获取最新的eNSP Pro镜像，确保您拥有`.vdi`文件。
   
2. **转换文件格式**：如果您计划在VMware中使用，需要将`.vdi`文件转换为`.vmdk`格式。利用VirtualBox的管理命令行工具`VBoxManage`执行转换。

3. **创建虚拟机**：在VMware中新建虚拟机，选择“稍后安装操作系统”，操作系统类型设为Linux的相应64位版本。

4. **配置虚拟机硬件**：
   - **磁盘**：使用转换后的`.vmdk`文件作为虚拟机硬盘。
   - **网络适配器**：至少配置两块网卡，一块用于管理，另一块用于互联网接入。可通过VMware的虚拟网络编辑器配置对应的网络模式（如VMnet1用于仅主机，VMnet8用于NAT）。

5. **带外管理网络**：若需通过CRT管理，需额外配置第三块网卡，并设置特定的仅主机网络。

## VirtualBox安装指南简述：

1. **相同镜像文件使用**：直接使用eNSP Pro的`.vdi`文件创建新虚拟机。
   
2. **网络配置**：遵循与VMware类似的原则配置网络设置，使用“仅主机”网络用于管理，必要时添加额外网卡以供带外管理使用。

## 使用CRT连接设备：

- 安装完eNSP Pro并正确配置网络后，通过CRT建立SSH或Telnet连接至设备。
- 配置设备的管理IP地址，确保这些地址与您的网络配置相匹配。
- 在CRT中设置相应的会话参数，例如端口号（默认22用于SSH，23用于Telnet），以及设备的IP地址。

## 注意事项：

- **账户与权限**：eNSP Pro可能需要华为账号登录，并且首次登录后会与当前环境绑定。
- **网络规划**：合理规划带外管理网络的IP范围，避免冲突。
- **版本兼容性**：确保您的VMware或VirtualBox版本与eNSP Pro兼容。
- **环境搭建**：确保物理机的网络配置不会干扰虚拟环境的网络访问。

以上步骤仅为概括，详细操作和可能出现的问题解决方案请参考原文链接提供的详细指南。

## 下载链接

[使用VMware或VirtualBox安装eNSPPro并使用CRT连接设备](https://pan.quark.cn/s/0eeeb22876d2)