---
layout: post
title: "小米CR880X路由刷不死合并分区再刷OPENWRT系统"
date:   2024-02-29
tags: [路由器,CR880X,OPENWRT,刷机,小米]
comments: true
author: admin
---
# 小米CR880X路由刷不死合并分区再刷OPENWRT系统

## 简介
本资源文件详细记录了如何将小米CR880X路由器通过不死UBOOT合并分区，增加系统空间至88M，并刷入OPENWRT系统的过程。文章包括硬件准备、固件下载、硬件连接、刷机步骤等内容，旨在帮助用户顺利完成刷机操作。

## 注意事项
- 刷机有风险，操作需谨慎。
- 请确保在操作前备份重要数据。
- 刷机过程中请勿断电或重启路由器。

## 硬件准备
1. 小米CR880X路由器（如CR8806）
2. CH340 TTL线
3. 电脑一台（需有USB口）

## 软件固件准备
1. 小米路由器修复工具 MIWIFIRepairTool
2. CR8806 官方固件 miwifi_cr8806_firmware_fe70b_6.2.14.bin
3. 第三方不死UBoot带Web CR880X合并分区并刷带web 4.1
4. OpenWrt AI固件 Xiaomi CR880X
5. 大佬纯净固件（最简化，后期需要自己完善）ipq50xx-qsdk-kernel-5.4-openwrt-21.02-qsdk-11.5.05.841.1029
6. tftpd、putty 或 MobaXterm 文件服务与登录操作

## 刷机步骤
1. 硬件连接：按照脚位参考图连接路由器和电脑。
2. 刷入不死UBoot：使用小米路由器修复工具刷入不死UBoot。
3. 合并分区：通过不死UBoot合并分区，增加系统空间至88M。
4. 刷入OPENWRT系统：使用tftpd、putty 或 MobaXterm工具刷入OPENWRT固件。
5. 完成刷机：等待刷机完成，路由器将自动重启并运行OPENWRT系统。

## 总结
通过本资源文件的指导，用户可以顺利将小米CR880X路由器刷入OPENWRT系统，并获得更大的系统空间，以便安装更多插件和功能。刷机过程中请务必谨慎操作，确保设备安全。

## 下载链接

[小米CR880X路由刷不死合并分区再刷OPENWRT系统](https://pan.quark.cn/s/30a1864d90bc)