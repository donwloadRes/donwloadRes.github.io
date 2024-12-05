---
layout: post
title: "STM32G4xx系列官方固件库驱动库板级支持包 for Keil MDK 5"
date:   2022-10-26
tags: [Keil,STM32G4xx,MDK,固件,库板级]
comments: true
author: admin
---
# STM32G4xx系列官方固件库驱动库板级支持包 for Keil MDK 5

## 简介

本仓库提供了一个用于Keil MDK 5的STM32G4xx系列官方固件库驱动库板级支持包（DFP），版本为1.2.0。该资源文件可以直接运行，加载到Keil MDK 5中，方便开发者快速集成STM32G4xx系列的开发环境。

## 资源文件信息

- **文件名**: Keil.STM32G4xx_DFP.1.2.0.pack
- **版本**: 1.2.0
- **发布日期**: 2020-08-03

## 更新内容

- **新增设备**:
  - STM32G491xxxx
  - STM32G4A1xxxx
  - STM32G483xx系列
  - STM32G474Px/STM32G484Px/STM32G473Px/STM32G483Px BGA121变体
  - STM32G431MBTx
  - STM32G441MBTx变体

- **更新内容**:
  - 更新STM32CubeG4固件包至V1.3.0
  - 更新SVD文件
  - 修复STM32G4xxxC设备的Flash编程算法问题，支持双/单Bank配置
  - 更新Flash类别3（512kB），支持D/S Bank配置
  - 更新框架CubeMX_gpdsc.ftl，增加对Timebase Source TIMx的支持
  - 更新示例代码，使用osThreadExit()终止app_main线程，避免无限循环

## 使用方法

1. 下载本仓库中的`Keil.STM32G4xx_DFP.1.2.0.pack`文件。
2. 打开Keil MDK 5开发环境。
3. 双击下载的`.pack`文件，系统将自动加载并安装该板级支持包。
4. 安装完成后，您可以在Keil MDK 5中使用STM32G4xx系列的开发资源。

## 注意事项

- 请确保您的Keil MDK 5版本与该板级支持包兼容。
- 如果在安装过程中遇到问题，请参考Keil官方文档或联系技术支持。

## 许可证

本资源文件遵循STMicroelectronics的许可证协议。请在使用前仔细阅读相关许可证条款。

## 联系我们

如有任何问题或建议，请通过GitHub Issues联系我们。

---

**感谢您使用STM32G4xx系列官方固件库驱动库板级支持包！**

## 下载链接

[STM32G4xx系列官方固件库驱动库板级支持包forKeilMDK5](https://pan.quark.cn/s/045f48f73225)