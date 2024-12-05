---
layout: post
title: "ST电机FOC控制库546完整版"
date:   2022-01-04
tags: [STM32Cube,FW,5.4,版本,完整版]
comments: true
author: admin
---
# ST电机FOC控制库5.4.6完整版

## 资源文件介绍

**文件名**: EN.X-CUBE-MCSDK-FUL_5.4.6完整版.zip

**描述**: 

该资源文件包含了ST电机FOC控制库5.4.6的完整源代码，于2021年3月更新至V5.4.6版本。此版本主要修复了X-Cube-MCSDK v5.4.5中的一些错误，并增加了对STM32CubeMx版本6.2.0的支持。具体更新内容如下：

- **新增支持**: 
  - 增加了对STM32CubeMx版本6.2.0的支持。
  - Motor Control Workbench现在嵌入了Liberica 8 JRE，与STM32CubeMx开始使用的JRE相同。

- **更新内容**:
  - 更新了STM32G4在Motor Control Workbench中的支持，以适应STM32CubeMx的更改。
  - 更新了B-G431-ESC1示例，以适应上述更改。

- **错误修复**:
  - 修复了版本5.4.5的SDK发布说明中关于STM32G4设备上注入ADC转换使用的错误描述。
  - 修复了发布说明中的一个拼写错误，将EVSPIN32F0601S1错误地命名为STSPIN32F0601S1。

**注意**: 此版本的X-Cube-MCSDK仍然支持IAR EWARM 7.x。

## 内容概览

- **Components**:
  - Version
  - License Terms
  - Release Note

- **Utilities/PC_Software**:
  - STMotorProfiler 1.3.2
  - STMCWB 5.4.6.21068-1.2.3.template-21-02-18

- **Middlewares/ST/MotorControl**:
  - 5.4.6 Ultimate Liberty

- **STM32Cube Environment**:
  - STM32CubeMX v6.2.0
  - STM32Cube_FW_F0_V1.11.2
  - STM32Cube_FW_F1_V1.8.3
  - STM32Cube_FW_F3_V1.11.2
  - STM32Cube_FW_F4_V1.26.0
  - STM32Cube_FW_F7_V1.16.0
  - STM32Cube_FW_G0_V1.4.0
  - STM32Cube_FW_G4_V1.4.0
  - STM32Cube_FW_L4_V1.17.0
  - STM32Cube_FW_H7_V1.9.0

- **Development Toolchains**:
  - IAR Embedded Workbench for ARM (IAR Systems AB) v7.80.4 和 v8.20.2
  - μVision® IDE for Arm® (Keil® MDK) v5.24.2
  - STM32CubeIDE v1.5.0
  - STM32CubeProgrammer 2.6.0

## 使用说明

1. **下载文件**: 点击下载按钮获取`EN.X-CUBE-MCSDK-FUL_5.4.6完整版.zip`文件。
2. **解压文件**: 解压下载的ZIP文件到本地目录。
3. **安装依赖**: 根据需要安装相应的开发工具链和STM32Cube环境。
4. **导入项目**: 使用STM32CubeIDE或其他支持的IDE导入项目，并根据需要进行配置和编译。

## 注意事项

- 确保使用的开发工具链和STM32Cube环境版本与资源文件中的版本兼容。
- 在导入和编译项目时，请仔细阅读相关的Release Notes和文档，以确保正确配置和使用。

## 联系我们

如有任何问题或建议，请通过GitHub的Issues功能联系我们。

## 下载链接

[ST电机FOC控制库5.4.6完整版](https://pan.quark.cn/s/8766ac28760b)