---
layout: post
title: "arm64(aarch64)安装CentOS 7.5.1804 指南"
date:   2020-05-05
tags: [CentOS,1804,7.5,ISO,YUM]
comments: true
author: admin
---
# arm64(aarch64)安装CentOS 7.5.1804 指南

## 简介

本资源提供了详细的指南，专为那些寻找如何在ARM64架构（aarch64）设备上安装CentOS 7.5.1804的用户准备。自从CentOS 7.5.1804版本之后，官方发布的ISO镜像取代了以往的rootfs tarball，这对使用Uboot的传统嵌入式开发者来说带来了挑战。本指南将指导您如何从ISO镜像中提取文件系统，并在不支持EFI引导的情况下利用uboot成功部署系统。

## 步骤概览

1. **下载ISO**：首先，从官方网站或镜像站点下载CentOS-7-aarch64-Minimal-1804.iso或者Everything版本。
   
2. **提取rootfs**：挂载下载的ISO文件，并从中提取LiveOS目录下的`squashfs.img`文件，这实际上是CentOS的压缩文件系统。

3. **进一步提取与配置**：将`squashfs.img`再次挂载以获取内部`rootfs.img`文件，再进一步处理以便uboot能够正确引导。

4. **系统调整**：移除`default.target`，建立指向`multi-user.target`的符号链接，确保系统启动到多用户模式而非图形界面。

5. **启用YUM**：由于初始系统不含完整的YUM环境，需手动从ISO中提取相关rpm包并安装，确保YUM能正常使用。记得更新`CentOS-Base.repo`中的$releasever为7。

6. **网络配置与软件安装**：配置IP地址，使用YUM安装必要的工具，如`passwd`, `sudo`, `openssh-server`, `telnet`, 和 `net-tools`等。

7. **代理设置**（如有需要）：在`/etc/yum.conf`添加代理信息，以便通过代理服务下载软件包。

8. **注意事项**：自行编译内核以支持特定第三方软件的内核需求。

## 注意

文章提供的步骤经过验证，确保按部就班可顺利完成CentOS 7.5.1804在ARM64设备上的安装。此外，文中还提及了一个预先制作好的系统镜像的百度网盘链接，供参考和直接使用，但请注意时效性和安全性。

**警告**：实际操作时，确保备份重要数据，避免硬件损坏或数据丢失。

---

此 README.md 文件旨在帮助用户快速理解并实施在ARM64平台上搭建CentOS 7.5.1804的整个过程。遵循上述步骤，您应能成功在您的ARM架构设备上部署CentOS系统。如果有任何疑问，推荐查阅原始文章获取更详尽的信息和解决可能遇到的问题。

## 下载链接

[arm64aarch64安装CentOS7.5.1804指南分享](https://pan.quark.cn/s/3307fa27562b)