---
layout: post
title: "ESXI 和 VMware 安装 MacOS 系统资源下载"
date:   2020-11-28
tags: [MacOS,VMware,虚拟机,ESXI,ISO]
comments: true
author: admin
---
# ESXI 和 VMware 安装 MacOS 系统资源下载

本仓库提供了一系列资源文件，帮助用户在 ESXI 和 VMware 环境中安装 MacOS 系统。资源包括 MacOS 10.14、MacOS 10.13、MacOS 10.12 的 ISO 镜像文件，以及 unlocker 工具，用于解锁 VMware 以支持 MacOS 虚拟机的安装。

## 资源列表

1. **MacOS 10.14 ISO 镜像**
   - 适用于 MacOS Mojave 系统。

2. **MacOS 10.13 ISO 镜像**
   - 适用于 MacOS High Sierra 系统。

3. **MacOS 10.12 ISO 镜像**
   - 适用于 MacOS Sierra 系统。

4. **unlocker 工具**
   - 用于解锁 VMware，使其支持 MacOS 虚拟机的安装。

## 安装步骤

1. **连接远程 ESXI 服务器**
   - 使用 VMware Workstation 连接远程 ESXI 服务器。

2. **上传 ISO 文件和 unlocker 工具**
   - 将 MacOS ISO 镜像文件和 unlocker 工具上传至 ESXI 服务器。

3. **给 VMware 打补丁**
   - 使用 unlocker 工具为 VMware 打补丁，以支持 MacOS 虚拟机的安装。

4. **创建 MacOS 虚拟机**
   - 在 VMware 中创建新的虚拟机，选择 MacOS 系统类型，并挂载相应的 ISO 镜像文件。

5. **安装 MacOS 系统**
   - 启动虚拟机，按照提示完成 MacOS 系统的安装。

## 注意事项

- 确保 ESXI 服务器已开启 SSH 功能，以便上传和执行 unlocker 工具。
- 在安装过程中，可能需要调整虚拟机的硬件配置，如内存和处理器数量。
- 安装完成后，建议安装 VMware Tools 以优化虚拟机的性能和用户体验。

## 联系我们

如有任何问题或建议，请通过 [联系我们] 页面与我们联系。

---

**版权声明**：本资源仅供学习和研究使用，请勿用于商业用途。

## 下载链接

[ESXI和VMware安装MacOS系统资源下载](https://pan.quark.cn/s/161d2c8233ac)