---
layout: post
title: "VMware 中的 MacOS 初始化问题和处理"
date:   2024-10-19
tags: [MacOS,虚拟机,VMware,https,CD]
comments: true
author: admin
---
# VMware 中的 MacOS 初始化问题和处理

本文档旨在帮助用户解决在 VMware 虚拟机中安装和初始化 MacOS 时可能遇到的问题。通过详细的步骤和解决方案，用户可以顺利完成 MacOS 的安装和配置。

## 操作环境
- 虚拟机VMware版本：15.5
- MacOS版本：CD Install MacOS Catalina 10.15.7 (19H2)
- 宿主机：Windows 10 22H2

## 问题和处理

### 问题1：VMTools工具栏是灰色的
**处理方式：**
1. 打开虚拟机设置。
2. 将名为“CD/DVD”和“软盘”的虚拟设备的连接方式全改成“自动检测”。
3. 如果有多个同类型的虚拟设备，全都要修改。

### 问题2：无法在更新服务器上找到组件
**处理方式：**
1. 关闭虚拟机。
2. 设备 -> CD/DVD(SATA) -> 硬件 -> CD/DVD(SATA)。
3. 选择使用 ISO 镜像文件，选中下载解压后的 darwin.iso，并勾选启动时连接，再点击“确定”。

### 问题3：通过系统设置更新 MacOS 系统时，可能会出现 MacOS 存储空间不够
**处理方式：**
1. 先关闭虚拟机，设置虚拟机磁盘大小（比如：100G，虚拟机内存大小不影响宿主机内存）。
2. 进入 MacOS 虚拟机设置 -> 硬盘(SATA) -> 扩展 -> 输入需要扩展的磁盘大小，点击扩展即可。
3. 打开 MacOS 虚拟机进入 Recovery 模式。
   - 进入 MacOS 虚拟机设置 -> 打开电源时进入固件 -> Enter setup -> Boot from a file -> Recovery -> 点击 -> boot.efi

**注：** 该方法可能会引起其它兼容性问题，请谨慎使用。升级系统时，可以考虑重新安装新版 MacOS 系统。

## 相关链接
- darwin.iso下载链接：[链接](https://pan.baidu.com/s/1y0HOZ0IAVv4XcvrXtAY0Pw) 提取码：5kh3

## 参考文献
- [参考文献1](https://blog.csdn.net/qq_15321533/article/details/114052417)
- [参考文献2](https://blog.csdn.net/Frank_dwx/article/details/107852311)
- [参考文献3](https://www.cnblogs.com/abeam/p/11872917.html)

通过以上步骤，用户可以有效地解决在 VMware 中安装和初始化 MacOS 时遇到的问题。希望本文档能对您有所帮助。

## 下载链接

[VMware中的MacOS初始化问题和处理](https://pan.quark.cn/s/aaedd148a597)