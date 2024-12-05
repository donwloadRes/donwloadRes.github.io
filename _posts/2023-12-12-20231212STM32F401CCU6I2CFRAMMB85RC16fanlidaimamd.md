---
layout: post
title: "STM32F401CCU6 I2C FRAM MB85RC16 范例代码"
date:   2022-01-14
tags: [FRAM,MB85RC16,代码,I2C,范例]
comments: true
author: admin
---
# STM32F401CCU6 I2C FRAM MB85RC16 范例代码

本仓库提供了一个基于STM32 HAL库的范例代码，用于访问2K字节存储空间的FRAM MB85RC16。该代码采用STM32CUBEIDE开发平台，并且适用于其他型号的2K字节FRAM的访问。

## 资源文件

- **STM32F401CCU6-I2C-FRAM-MB85RC16.rar**

## 描述

该资源文件包含了使用STM32 HAL库访问2K字节存储空间FRAM MB85RC16的范例代码。代码基于STM32CUBEIDE开发平台，并且可以轻松移植到其他型号的2K字节FRAM设备上。

## 使用说明

1. **下载资源文件**：下载并解压 `STM32F401CCU6-I2C-FRAM-MB85RC16.rar` 文件。
2. **导入项目**：将解压后的项目导入到STM32CUBEIDE中。
3. **配置硬件**：根据实际硬件连接配置I2C总线。
4. **编译与下载**：编译项目并将代码下载到STM32F401CCU6开发板上。
5. **运行与调试**：运行代码并调试，确保FRAM MB85RC16的读写操作正常。

## 注意事项

- 确保硬件连接正确，特别是I2C总线的连接。
- 如果使用其他型号的FRAM，请根据具体型号调整代码中的寄存器地址。

## 相关文章

有关该范例代码的详细介绍，请参考CSDN博文《STM32存储左右互搏 I2C总线读写FRAM MB85RC16》。

---

希望本范例代码能够帮助您快速上手STM32 HAL库访问FRAM MB85RC16。如有任何问题，欢迎在仓库中提出Issue。

## 下载链接

[STM32F401CCU6I2CFRAMMB85RC16范例代码](https://pan.quark.cn/s/ac7a2ffe1819)