---
layout: post
title: "飞腾FT20004开发板Ubuntu18045移植及内核更换教程"
date:   2020-02-09
tags: [开发板,内核,飞腾,18.04,教程]
comments: true
author: admin
---
# 飞腾FT-2000-4开发板Ubuntu18.04.5移植及内核更换教程

## 资源描述

本资源文件提供了在飞腾FT-2000-4开发板上移植Ubuntu 18.04.5操作系统，并更换为飞腾内核4.19.8的详细教程。以下是教程的主要内容和注意事项：

### 1. 必备硬件
- **PCIe显卡**：飞腾开发板本身没有显示输出，因此需要自行配备显卡。建议选择AMD主流显卡。
- **有流量的安卓手机**：系统安装完成后，开发板上没有网络接口，唯一的上网方式是通过安卓手机的“USB共享网络”功能。

### 2. 系统选择
- **Ubuntu Server版本**：由于Ubuntu在ARM平台上只支持Server版本，因此需要选择Ubuntu Server 18.04.5。
- **HWE内核**：在18.04系列中，只有18.04.5版本包含HWE内核，其他版本可能无法安装。如果手中有其他18.04版本，请确认是否包含HWE内核。

### 3. UEFI固件
- **UEFI固件**：本教程不涉及UEFI固件的获取和安装，默认认为您已经拥有UEFI固件，并能够将其加载到开发板中。

### 4. 其他注意事项
- 本教程详细介绍了如何在飞腾FT-2000-4开发板上完成Ubuntu 18.04.5的移植，并更换为飞腾内核4.19.8。
- 教程中包含了网络配置、内核更换等关键步骤的详细说明。

通过本教程，您将能够在飞腾FT-2000-4开发板上成功运行Ubuntu 18.04.5，并使用飞腾内核4.19.8进行开发和调试。

## 下载链接

[飞腾FT-2000-4开发板Ubuntu18.04.5移植及内核更换教程](https://pan.quark.cn/s/3a96c490f94f)