---
layout: post
title: "KeilSTM32F1xxdfp230 固件包"
date:   2020-06-10
tags: [固件,Keil,STM32F1xx,驱动,更新]
comments: true
author: admin
---
# Keil.STM32F1xx-dfp.2.3.0 固件包

## 资源描述

该资源文件为 Keil.STM32F1xx-dfp.2.3.0 固件包，版本号为 2.3.0，发布日期为 2018-11-05。此固件包包含了一系列针对 STM32F1xx 系列微控制器的设备支持文件和驱动程序，适用于 Keil MDK 开发环境。

### 主要更新内容

- **DBGMCU INI 文件**：新增了用于设置调试配置的 DBGMCU INI 文件。
- **设备头文件包含修复**：修复了设备头文件在 Linux 系统上因大小写敏感导致的编译错误。
- **CMSIS 驱动更新**：
  - **CAN 驱动**：修正了 MessageSend 函数，使其仅访问发送所需的数据；修正了中止消息发送功能；修正了 SetBitrate 函数。
  - **EMAC 驱动**：修正了 ETH DMA 初始化，现在在 MAC 发送器或接收器启用时进行初始化（解决了 netInitialize/netUnnitialize/netInitialize 问题）。
  - **USB Host 和 Device 驱动**：增加了对 CMSIS-RTOS2 的支持。
  - **USART 驱动**：修正了 ARM_USART_SET_IRDA_PULSE 控制。
- **板级驱动更新**：更新了板级支持的 LED_*.c 文件。
- **示例更新**：更新了 emWin 示例至 emWin V5.46e；更新了 USB Host 示例的线程堆栈设置。

## 版权声明

版权归原作者所有，此处为了方便国内用户下载。

## 使用说明

1. 下载该固件包。
2. 在 Keil MDK 开发环境中导入该固件包。
3. 根据需要选择相应的设备和驱动进行开发。

## 注意事项

- 请确保您的开发环境为 Keil MDK，并且版本兼容。
- 使用前请仔细阅读固件包中的更新日志和文档。

---

希望该固件包能够帮助您顺利进行 STM32F1xx 系列的开发工作。如有任何问题，请参考官方文档或联系技术支持。

## 下载链接

[Keil.STM32F1xx-dfp.2.3.0固件包](https://pan.quark.cn/s/e7106c99891e)