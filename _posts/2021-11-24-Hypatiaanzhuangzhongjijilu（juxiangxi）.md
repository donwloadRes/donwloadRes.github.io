---
layout: post
title: "Hypatia安装终极记录（巨详细）"
date:   2021-02-22
tags: [安装,Hypatia,Ubuntu,18.04,sh]
comments: true
author: admin
---
# Hypatia安装终极记录（巨详细）

本仓库提供了一个详细的Hypatia安装指南，旨在帮助用户在Ubuntu 18.04系统上顺利安装Hypatia。Hypatia是一个网络仿真平台，适用于卫星网络等复杂网络环境的仿真研究。

## 内容概述

本指南详细记录了在Ubuntu 18.04上安装Hypatia的全过程，包括以下步骤：

1. **系统准备**：
   - 安装VMware Workstation 16 Pro和Ubuntu 18.04。
   - 使用conda创建Python环境。

2. **依赖库安装**：
   - 解决cartopy安装问题。
   - 安装必要的依赖库，如numpy、astropy、ephem等。

3. **Hypatia安装**：
   - 下载Hypatia源码并安装环境依赖。
   - 构建和测试Hypatia模块。

4. **论文实验复现**：
   - 复现相关论文实验的步骤。

## 安装步骤

### 1. 系统准备

- **VMware Workstation 16 Pro + Ubuntu 18.04**：
  - 安装VMware Workstation 16 Pro和Ubuntu 18.04系统。
  - 使用conda创建Python环境，选择Python 3.8版本。

- **更换清华源**：
  - 提高下载速度，更换为清华源。

### 2. 依赖库安装

- **安装anaconda**：
  - 下载并安装anaconda，方便管理虚拟环境。

- **安装cartopy**：
  - 使用conda安装cartopy，解决pip安装失败问题。

- **安装其他依赖库**：
  - 使用pip安装numpy、astropy、ephem等依赖库。

### 3. Hypatia安装

- **下载Hypatia源码**：
  - 从GitHub克隆Hypatia源码。

- **安装环境依赖**：
  - 执行`hypatia_install_dependencies.sh`脚本，安装所有依赖库。

- **构建和测试**：
  - 执行`hypatia_build.sh`脚本，构建Hypatia模块。
  - 运行测试脚本`hypatia_run_tests.sh`，确保安装成功。

### 4. 论文实验复现

- **生成LEO卫星网络动态状态**：
  - 在`satellite_networks_state`目录下运行`generate_all_local.sh`脚本。

- **构建ns-3模拟器**：
  - 执行`build.sh --debug_all`脚本，构建ns-3模拟器。

- **执行分析和实验**：
  - 使用satgenpy进行分析，运行ns-3实验。

## 注意事项

- 在安装过程中，可能会遇到各种问题，建议参考CSDN博客中的详细记录，逐一解决。
- 对于长时间运行的程序，建议设置为只读模式，避免意外中断。

通过本指南，您将能够顺利在Ubuntu 18.04系统上安装并运行Hypatia，进行网络仿真研究。

## 下载链接

[Hypatia安装终极记录巨详细](https://pan.quark.cn/s/7bbb018b7a3d)