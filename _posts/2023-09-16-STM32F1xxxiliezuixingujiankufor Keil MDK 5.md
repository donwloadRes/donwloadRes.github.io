---
layout: post
title: "STM32F1xx系列最新固件库for Keil MDK 5"
date:   2021-01-20
tags: [Keil,STM32F1xx,MDK,文件,示例]
comments: true
author: admin
---
# STM32F1xx系列最新固件库for Keil MDK 5

## 资源文件介绍

本仓库提供了一个用于Keil MDK 5的STM32F1xx系列最新固件库资源文件：`Keil.STM32F1xx_DFP.2.3.0.pack`。该资源文件包含了STM32F1xx系列芯片的驱动程序、CMSIS库、示例代码以及其他必要的支持文件，方便用户在Keil MDK 5开发环境中进行STM32F1xx系列芯片的开发。

## 安装方法

1. **下载资源文件**：从本仓库下载`Keil.STM32F1xx_DFP.2.3.0.pack`文件。
2. **双击安装**：直接双击下载的`.pack`文件，系统将自动启动Keil MDK 5的安装程序，并提示您完成安装过程。
3. **验证安装**：安装成功后，打开Keil MDK 5，在创建或打开工程时，您可以在“Device”选项中选择STM32F1xx系列芯片。

## 版本信息

- **版本号**：2.3.0
- **发布日期**：2018-11-05

## 更新内容

- **DBGMCU INI文件**：添加了用于设置调试配置的DBGMCU INI文件。
- **设备头文件包含修复**：修复了设备头文件在Linux系统上因大小写敏感导致的构建错误。
- **CMSIS驱动更新**：
  - **CAN驱动**：修正了`MessageSend`函数，使其仅访问发送所需的数据；修正了中止消息发送功能；修正了`SetBitrate`函数。
  - **EMAC驱动**：修正了ETH DMA初始化，现在在MAC发送器或接收器启用时进行初始化（解决了`netInitialize/netUnnitialize/netInitialize`问题）。
  - **USB Host和Device**：添加了对CMSIS-RTOS2的支持。
  - **USART驱动**：修正了ARM_USART_SET_IRDA_PULSE控制。
- **板级驱动更新**：更新了板级支持的LED_*.c文件。
- **示例代码更新**：
  - 更新了emWin示例代码至emWin V5.46e版本。
  - 更新了USB Host示例代码的线程堆栈设置。

## 注意事项

- 请确保您的Keil MDK 5版本与该固件库兼容。
- 如果在安装或使用过程中遇到任何问题，请参考Keil官方文档或联系技术支持。

## 许可证

本资源文件遵循Keil MDK 5的许可证协议，请在使用前仔细阅读相关许可证条款。

---

希望本资源文件能够帮助您顺利进行STM32F1xx系列芯片的开发工作！如有任何问题或建议，欢迎在仓库中提出Issue。

## 下载链接

[STM32F1xx系列最新固件库forKeilMDK5](https://pan.quark.cn/s/1642fd8da93b)