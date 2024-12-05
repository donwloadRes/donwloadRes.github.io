---
layout: post
title: "OpenStack KVM虚拟机镜像 - Windows Server 2022"
date:   2022-08-04
tags: [镜像,虚拟机,OpenStack,2022,iso]
comments: true
author: admin
---
# OpenStack KVM虚拟机镜像 - Windows Server 2022

## 资源文件描述

本仓库提供两个Windows Server 2022的KVM虚拟机镜像，适用于OpenStack环境。以下是两个镜像的详细信息：

### 1. `win2022_35g.qcow2`
- **安装源**: 使用 `zh-cn_windows_server_2022_updated_dec_2022_x64_dvd_444e9e55.iso`（2022年12月）进行安装。
- **Virtio驱动**: 使用 `virtio-win-0.1.225.iso` 中的WIN2022驱动。
- **测试环境**: 在OpenStack的Q版、T版、Y版中测试可用。
- **磁盘容量**: 34G
- **分区**: 
  - C盘: 24G
  - D盘: 10G
- **管理员密码**: Qwer1234

### 2. `win2022_20g.qcow2`
- **安装源**: 使用 `zh-cn_windows_server_2022_updated_may_2023_x64_dvd_659778fe.iso`（2023年5月）进行安装。
- **Virtio驱动**: 使用 `virtio-win-0.1.225.iso` 中的WIN2022驱动。
- **测试环境**: 在OpenStack的Q版、T版、Y版中测试可用。
- **磁盘容量**: 20G
- **分区**: 
  - C盘: 16G
  - D盘: 4G
- **管理员密码**: Qwer1234

## 使用说明

1. **下载镜像**: 请从本仓库下载所需的镜像文件。
2. **导入OpenStack**: 将下载的镜像导入到OpenStack环境中。
3. **创建虚拟机**: 使用导入的镜像创建虚拟机实例。
4. **登录**: 使用管理员账户 `administrator` 和密码 `Qwer1234` 登录虚拟机。

## 注意事项

- 本镜像仅供测试使用，不得用于商业用途。
- 请确保在合法的环境中使用本镜像，遵守相关法律法规。

## 联系我们

如有任何问题或建议，请联系我们。

## 下载链接

[OpenStackKVM虚拟机镜像-WindowsServer2022分享](https://pan.quark.cn/s/8d4dddb84afa)