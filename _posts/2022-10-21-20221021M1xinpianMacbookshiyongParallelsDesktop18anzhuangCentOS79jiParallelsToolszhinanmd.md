---
layout: post
title: "M1芯片Macbook使用Parallels Desktop 18安装CentOS 79及Parallels Tools指南"
date:   2023-03-27
tags: [Parallels,CentOS,安装,M1,Desktop]
comments: true
author: admin
---
# M1芯片Macbook使用Parallels Desktop 18安装CentOS 7.9及Parallels Tools指南

## 概述

本文档提供了详细步骤，指导如何在配备M1芯片的Macbook上利用Parallels Desktop 18虚拟机软件安装CentOS 7.9操作系统，并成功集成Parallels Tools工具。通过此教程，用户能够获得更佳的虚拟机性能，实现更顺畅的跨平台体验。

## 准备阶段

- **下载资源**：确保已获取CentOS 7.9的ISO镜像文件，官方镜像或通过推荐渠道下载。
- **软件准备**：安装最新的Parallels Desktop 18 for Mac。

## 步骤详解

### 1. 创建虚拟机与安装CentOS

1. **启动Parallels Desktop**，新建虚拟机。
2. **选择安装来源**，使用先前下载的CentOS 7.9 ISO文件。
3. **自定义配置**，根据需求设置虚拟机硬件参数。
4. **安装过程**，跟随CentOS的图形安装向导操作，注意设置正确的时区、用户名和密码。

### 2. 安装Parallels Tools

安装CentOS 7.9后，接下来是关键步骤——集成Parallels Tools。

1. **升级GCC**：由于M1芯片的特殊性，需确保GCC版本在8以上，通过SCL启用devtoolset-8。
   ```bash
   yum install -y centos-release-scl
   yum install -y devtoolset-8-gcc*
   scl enable devtoolset-8 bash
   ```
   
2. **挂载CDROM**，从虚拟光驱中安装Parallels Tools：
   ```bash
   mkdir /media/cdrom; mount /dev/cdrom /media/cdrom/
   cp -r /media/cdrom/* /mnt/ptools
   cd /mnt/ptools
   ./install
   ```

3. **配置共享文件夹与优化**：
   - 按照向导配置Parallels Desktop中的共享文件夹选项。
   - 确保系统更新与兼容性设置正确。

## 注意事项

- **系统兼容性**：确保所用的CentOS版本与Parallels Desktop版本兼容。
- **网络配置**：安装后可能需要调整网络设置以适应M1芯片的环境。
- **性能调优**：根据实际使用情况，优化虚拟机的CPU和内存分配。

## 结论

遵循上述步骤，开发者与技术人员能在他们的M1芯片Macbook上成功搭建一个高效的CentOS 7.9开发或测试环境，充分利用Parallels Tools带来的便利，比如无缝的剪贴板共享、同步时间以及优化的图形表现，大大提高工作效率。记得在安装过程中留意系统提示，适时查阅官方文档以解决特定问题。

## 下载链接

[M1芯片Macbook使用ParallelsDesktop18安装CentOS7.9及ParallelsTools指南分享](https://pan.quark.cn/s/911c05a0f5d9)