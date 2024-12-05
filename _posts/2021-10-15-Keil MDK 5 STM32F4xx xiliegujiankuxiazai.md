---
layout: post
title: "Keil MDK 5 STM32F4xx 系列固件库下载"
date:   2020-01-19
tags: [Keil,MDK,STM32F4xx,安装,固件]
comments: true
author: admin
---
# Keil MDK 5 STM32F4xx 系列固件库下载

## 资源介绍

本仓库提供了一个资源文件的下载，该文件为 **Keil.STM32F4xx-DFP.2.14.0.pack**，是 Keil MDK 5 官方提供的最新 STM32F4xx 系列固件库。

## 资源描述

- **文件名**: Keil.STM32F4xx-DFP.2.14.0.pack
- **版本**: 2.14.0 (发布日期: 2019-07-24)
- **适用环境**: 电脑需先安装 Keil MDK 5。

### 安装说明

1. **安装前提**: 确保您的电脑上已经安装了 Keil MDK 5。
2. **安装步骤**: 直接双击 `Keil.STM32F4xx-DFP.2.14.0.pack` 文件进行安装。
3. **安装成功后**: 在 MDK 5 工程的 Device 中可以选择 STM32F4xx 系列的 ARM 芯片。

### 更新内容

- **版本 2.14.0 更新**:
  - 不再通过设备描述强制执行 C99 标准，请在 Options for Target 对话框的 C/C++ 选项卡中启用 C99 模式。
  - 更新了 Pack 以包含 STM32Cube_FW_F4 固件包版本 V1.24.1 的一部分，使用 HAL 驱动程序 V1.7.6。
  - 修正了 RTE_Device.h 中 UART5 引脚配置的问题。
  - 更新了 MX_Device_h.ftl 中 USART 虚拟模式的解析。
  - 更新了生成器以支持新的功能。

## 注意事项

- 请确保在安装此固件库之前，您的 Keil MDK 5 已经正确安装并配置。
- 安装过程中如有任何问题，请参考 Keil 官方文档或联系技术支持。

## 贡献与反馈

如果您在使用过程中遇到任何问题或有任何建议，欢迎通过 GitHub 的 Issues 功能提交反馈。我们非常乐意听取您的意见并进行改进。

感谢您的使用与支持！

## 下载链接

[KeilMDK5STM32F4xx系列固件库下载](https://pan.quark.cn/s/b7d6528abef5)