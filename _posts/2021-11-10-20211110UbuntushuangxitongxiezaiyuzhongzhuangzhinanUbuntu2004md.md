---
layout: post
title: "Ubuntu双系统卸载与重装指南（Ubuntu 20.04）"
date:   2023-05-14
tags: [Ubuntu,U盘,卸载,系统,分区]
comments: true
author: admin
---
# Ubuntu双系统卸载与重装指南（Ubuntu 20.04）

本指南详细介绍了如何在Windows和Ubuntu双系统环境下，彻底卸载旧的Ubuntu系统并重新安装Ubuntu 20.04。无论您是因为系统环境混乱、磁盘空间不足还是不再需要Ubuntu系统，本指南都将帮助您安全、高效地完成卸载和重装过程。

## 背景

在使用Ubuntu进行开发时，可能会不小心搞乱系统环境，或者因为其他原因需要重新安装系统。本指南将记录卸载和重装过程中遇到的常见问题和解决方案，供大家参考。

## 彻底卸载原系统

### 1. 重新分配磁盘

如果您是双系统用户，首先需要在Windows系统中删除Ubuntu系统所使用的磁盘分区。具体步骤如下：

- 右键点击“此电脑”，选择“管理”。
- 在左侧选择“磁盘管理”，进入磁盘管理界面。
- 确定Ubuntu系统使用的磁盘分区，将其完全删除。
- 使用排除法，排除Windows系统所使用的C、D、E等分区，以及启动（EFI）分区、保留分区和恢复分区等特殊功能分区。
- 选中Ubuntu系统使用的分区，右键点击“删除卷”，删除后磁盘会自动回到未分配状态。

### 2. 更改EFI设置

电脑开机时首先进入的系统选择界面是EFI界面，因此我们还需要在EFI中删除Ubuntu的启动选择项。具体步骤如下：

- 参考相关教程，在EFI中删除Ubuntu的启动选择项。
- 完成后，重启系统时如果看不到之前的系统选择界面，说明双系统中的Ubuntu卸载成功。

## 安装新系统

### 1. 制作U盘系统盘

- 准备一个至少4GB的U盘。
- 使用Rufus软件制作系统盘。
- 下载Ubuntu 20.04系统的ISO光盘镜像文件。
- 插入U盘，选择设备为U盘，镜像文件选择下载的ISO文件，点击开始制作。

### 2. 安装系统

- U盘制作完成后不要拔出，重启电脑。
- 开机时进入BIOS设置为U盘启动，选择刚才做好的U盘，开始安装Ubuntu 20.04。
- 按照系统引导完成安装过程，注意分区设置，建议将/和/home对半分。
- 安装完成后选择立即重启，重启后进入开机界面，拔出U盘再重启。

## 注意事项

- 在卸载和重装过程中，请确保备份所有重要数据和文件，以免数据丢失。
- 安装过程中，请注意及时拔出U盘，避免系统启动后黑屏。

通过以上步骤，您可以安全、彻底地卸载旧的Ubuntu系统并重新安装Ubuntu 20.04。希望本指南对您有所帮助！

## 下载链接

[Ubuntu双系统卸载与重装指南Ubuntu20.04分享](https://pan.quark.cn/s/47345029ee0b)