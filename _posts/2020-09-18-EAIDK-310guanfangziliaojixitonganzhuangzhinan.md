---
layout: post
title: "EAIDK-310官方资料及系统安装指南"
date:   2021-04-29
tags: [EAIDK,310,rootfs,镜像,官方]
comments: true
author: admin
---
# EAIDK-310官方资料及系统安装指南

## 简介
本资源文件提供了EAIDK-310开发板的官方资料，以及如何在EAIDK-310上安装Ubuntu和Debian系统的详细指南。EAIDK-310是一款基于RK3228H（即RK3328）的嵌入式开发板，支持多种操作系统，包括Fedora 28、Ubuntu 16.04（桌面环境，内核版本4.4）以及安卓8.1。

## 资源内容
1. **官方资料**：包括EAIDK-310的硬件规格、原理图、驱动程序等。
2. **系统安装指南**：详细介绍了如何在EAIDK-310上安装Ubuntu和Debian系统。

## 安装步骤
1. **下载rootfs镜像**：使用SD card imges网站提供的最新Debian和Ubuntu系统的rootfs镜像，选择Leez P720型号的镜像，实测兼容。
2. **创建镜像文件**：通过命令`dd if=/dev/zero of=my_rootfs.img bs=1M count=7000`创建自己的镜像文件，并将下载的img文件复制到该镜像中。
3. **无线和蓝牙驱动**：从EAIDK官方提供的rootfs镜像中复制/system文件夹到自己制作的rootfs镜像中，以驱动无线和蓝牙功能。
4. **刷写系统**：参考官方资料中的文档介绍，进行系统刷写。

## 注意事项
- EAIDK-310相关的支持“没有被并入主线内核”，因此建议使用官方自带的4.4内核。
- 安装过程中可能需要替换rootfs.img文件，请确保操作正确。

## 其他资源
- **用户名和密码**：默认用户名和密码均为`openailab`。
- **调试工具**：提供了USB转TTL串口线的连接方法，以及通过SecureCRT登录开发板的详细步骤。

## 联系我们
如有任何问题或建议，请联系我们。

---

希望这份README.md文件能帮助您顺利使用EAIDK-310开发板。

## 下载链接

[EAIDK-310官方资料及系统安装指南](https://pan.quark.cn/s/dc898f497113)