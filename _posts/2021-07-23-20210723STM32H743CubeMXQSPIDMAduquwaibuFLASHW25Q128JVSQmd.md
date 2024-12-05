---
layout: post
title: "STM32H743CubeMXQSPIDMA读取外部FLASHW25Q128JVSQ"
date:   2022-08-21
tags: [FLASH,读取,STM32H743,CubeMX,QSPI]
comments: true
author: admin
---
# STM32H743+CubeMX-QSPI+DMA读取外部FLASH(W25Q128JVSQ)

本资源文件提供了一个完整的示例代码和配置文件，用于在STM32H743微控制器上通过CubeMX配置QSPI接口，并使用DMA方式读取外部FLASH（W25Q128JVSQ）。

## 项目概述

该项目展示了如何在STM32H743微控制器上使用CubeMX工具配置QSPI接口，并通过DMA方式高效地读取外部FLASH（W25Q128JVSQ）。通过本示例，您可以学习到如何配置硬件电路、使用CubeMX生成项目代码、添加自定义代码到工程中，并通过DEBUG模式验证读取操作的正确性。

## 主要内容

1. **硬件电路配置**：
   - 详细描述了STM32H743与外部FLASH（W25Q128JVSQ）的硬件连接方式。

2. **CubeMX配置**：
   - 使用CubeMX工具进行QSPI接口的参数设置、GPIO设置和MDMA设置。
   - 生成项目代码并进行必要的调整。

3. **例程代码**：
   - 提供了完整的示例代码，包括读取外部FLASH的ID、擦除FLASH扇区、写入数据到FLASH以及从FLASH读取数据。
   - 通过DEBUG模式验证读取操作的正确性。

4. **DMA设置**：
   - 详细介绍了如何配置MDMA以实现高效的数据传输。

## 使用说明

1. **下载资源文件**：
   - 下载本资源文件，解压后包含所有必要的代码和配置文件。

2. **导入工程**：
   - 使用STM32CubeIDE或其他支持的开发环境导入生成的工程文件。

3. **配置硬件**：
   - 根据提供的硬件电路图连接STM32H743与外部FLASH（W25Q128JVSQ）。

4. **编译与调试**：
   - 编译工程并下载到目标板。
   - 使用DEBUG模式验证读取操作的正确性。

## 注意事项

- 在配置MDMA时，请参考《STM32H7x3编程参考手册》第14章，了解MDMA控制器的详细信息。
- 在移植例程代码时，确保工程已具备“重定向printf”功能，以便正确使用bsp文件。

## 联系我们

如有任何问题或建议，请通过CSDN博客联系作者Wallace Zhang。

---

通过本资源文件，您将能够快速掌握在STM32H743上使用QSPI和DMA读取外部FLASH的方法，并将其应用到实际项目中。

## 下载链接

[STM32H743CubeMX-QSPIDMA读取外部FLASHW25Q128JVSQ分享](https://pan.quark.cn/s/72f7083f1de6)