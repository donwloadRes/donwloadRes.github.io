---
layout: post
title: "GCC 4.8.5 离线安装包"
date:   2024-10-26
tags: [rpm,x86,64,el7,sudo]
comments: true
author: admin
---
# GCC 4.8.5 离线安装包

本仓库提供了一个用于离线安装的 GCC 4.8.5 及相关依赖包的资源文件。该资源文件适用于 CentOS 7 系统，包含以下 RPM 包：

- `cpp-4.8.5-28.el7.x86_64.rpm`
- `gcc-4.8.5-28.el7.x86_64.rpm`
- `glibc-devel-2.17-222.el7.x86_64.rpm`
- `glibc-headers-2.17-222.el7.x86_64.rpm`
- `kernel-headers-3.10.0-862.el7.x86_64.rpm`
- `libmpc-1.0.1-3.el7.x86_64.rpm`
- `mpfr-3.1.1-4.el7.x86_64.rpm`

## 使用说明

1. **下载资源文件**：
   你可以直接下载本仓库中的所有 RPM 包，或者选择单独下载所需的包。

2. **安装 RPM 包**：
   在目标机器上，使用以下命令安装下载的 RPM 包：
   ```bash
   sudo rpm -ivh *.rpm
   ```
   或者逐个安装：
   ```bash
   sudo rpm -ivh cpp-4.8.5-28.el7.x86_64.rpm
   sudo rpm -ivh gcc-4.8.5-28.el7.x86_64.rpm
   sudo rpm -ivh glibc-devel-2.17-222.el7.x86_64.rpm
   sudo rpm -ivh glibc-headers-2.17-222.el7.x86_64.rpm
   sudo rpm -ivh kernel-headers-3.10.0-862.el7.x86_64.rpm
   sudo rpm -ivh libmpc-1.0.1-3.el7.x86_64.rpm
   sudo rpm -ivh mpfr-3.1.1-4.el7.x86_64.rpm
   ```

3. **验证安装**：
   安装完成后，可以通过以下命令验证 GCC 是否安装成功：
   ```bash
   gcc --version
   ```

## 注意事项

- 请确保目标机器的操作系统为 CentOS 7，并且架构为 x86_64。
- 如果系统中已经安装了其他版本的 GCC，可能会导致冲突，建议在安装前进行备份或卸载现有版本。
- 本资源文件适用于离线环境，如果可以访问互联网，建议直接使用 `yum` 或 `dnf` 进行在线安装。

## 联系我们

如果在使用过程中遇到任何问题，欢迎通过 GitHub 的 Issues 功能联系我们。

## 下载链接

[GCC4.8.5离线安装包分享](https://pan.quark.cn/s/8fc8b0e6366e)