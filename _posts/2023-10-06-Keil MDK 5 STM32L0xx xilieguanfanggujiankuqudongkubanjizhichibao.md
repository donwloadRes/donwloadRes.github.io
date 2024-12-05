---
layout: post
title: "Keil MDK 5 STM32L0xx 系列官方固件库驱动库板级支持包"
date:   2020-01-22
tags: [Keil,STM32L0xx,MDK,固件,文件]
comments: true
author: admin
---
# Keil MDK 5 STM32L0xx 系列官方固件库驱动库板级支持包

## 简介

本仓库提供了一个资源文件：`Keil.STM32L0xx_DFP.2.1.0.pack`，这是针对 Keil MDK 5 的 STM32L0xx 系列官方固件库驱动库板级支持包。该资源文件可以直接运行，以便在 Keil MDK 5 中加载 STM32L0xx 系列的固件库和驱动库。

## 版本信息

- **版本**: 2.1.0
- **发布日期**: 2020-07-20

## 更新内容

### STM32CubeMX 集成

- 增加了对使用 Timebase Source TIMx 的支持（FrameworkCubeMX_gpdsc.ftl）。
- 增加了在 Flash 下载后启动 Option Byte Loading 的功能。

### 设备支持

- 更新了 STM32L0xx 系列设备。
- 更新了 STM32Cube 固件库至 STM32Cube_FW_L0_V1.11.2（HAL V1.10.2）。
- 更新了 SVD 文件。
- 更新了文档。

### CMSIS-Driver

- **SPI**: 修正了驱动源代码中的编译警告。
- **USB Device**: 修正了 USBD_EndpointConfigure 函数（检查请求的最大数据包大小是否适合配置的 FIFO）。

### 示例项目

- 终止 app_main 线程时使用 osThreadExit() 以避免无限循环。
- **USB Device 示例**: 在 USB Device 示例中增加了 Event Recorder（适用于 STM32L073Z-EVAL 开发板）。
- 更新了用户代码模板，来自 MDK-Middleware v7.11.1。

## 使用说明

1. 下载本仓库中的 `Keil.STM32L0xx_DFP.2.1.0.pack` 文件。
2. 在 Keil MDK 5 中直接运行该文件，即可加载 STM32L0xx 系列的固件库和驱动库。

## 注意事项

- 请确保您的 Keil MDK 5 版本与该资源文件兼容。
- 如果在使用过程中遇到任何问题，请参考 Keil 官方文档或联系技术支持。

## 许可证

本资源文件遵循 Keil 官方的许可证协议。请在使用前仔细阅读相关许可证条款。

## 贡献

如果您有任何改进建议或发现了问题，欢迎提交 Issue 或 Pull Request。

## 联系我们

如有任何疑问或需要进一步的帮助，请通过 GitHub 仓库的 Issues 页面联系我们。

## 下载链接

[KeilMDK5STM32L0xx系列官方固件库驱动库板级支持包](https://pan.quark.cn/s/530c08a826f5)