---
layout: post
title: "STM32工程从Keil迁移到IAR环境指南"
date:   2020-11-02
tags: [IAR,Keil,文件,STM32,文件夹]
comments: true
author: admin
---
# STM32工程从Keil迁移到IAR环境指南

本资源文档详细指导了如何将基于STM32F103C8的项目从Keil MDK开发环境成功迁移至IAR Workbench环境。适合那些希望在不同IDE间切换或扩展其开发工具链的开发者。以下是六个关键步骤，确保平滑过渡：

## 步骤一：环境准备与文件结构
- **安装IAR编译器**：首先确保安装了适用于您的STM32系列的IAR Embedded Workbench。
- 创建项目文件夹`LED_CTRL`，并在其中设立子文件夹：
    - `CMSIS`用于存放系统启动文件。
    - `FWLIB`用于库文件。
    - `USER`用于用户编写的应用代码。

## 步骤二：文件迁移
- 从Keil项目中复制对应的文件到上述创建的文件夹中，包括CMSIS、FWLIB和USER目录下的所有必要文件，以及任何自定义文件。

## 步骤三：新建IAR工程
- 在IAR中新建一个名为`led_temp`的工程，保存于`LED_CTRL`目录。

## 步骤四：组织与添加文件
- 分别向相应的文件夹（CMSIS、FWLIB、USER）添加对应的源文件至工程中。通过“Add Group”来管理逻辑模块，再逐一添加文件。

## 步骤五：工程配置
- 设置正确的芯片型号（STM32F103C8T6），并调整编译器选项以支持Full Library配置，以便使用printf等函数。
- 添加必要的包含路径和宏定义，确保链接正确，且根据硬件配置调试选项。

## 步骤六：编译与错误解决
- 完成初步构建后，可能会遇到特定错误，如核心文件冲突或编译器差异引起的警告。
    - 重命名或处理`core_cm3.h`文件冲突。
    - 更改启动文件中段定义解决编译警告，例如，将`SECTION .text:CODE:REORDER`改为`SECTION .text:CODE:NOROOT:REORDER`。
- 最终，确保编译无误、无警告，完成移植过程。

---

此指南针对的是具体的项目迁移案例，开发者需根据实际项目情况适当调整步骤。通过遵循以上步骤，您可以高效地将STM32项目从Keil环境迁移到IAR环境，拓宽您的开发选项。

## 下载链接

[STM32工程从Keil迁移到IAR环境指南分享](https://pan.quark.cn/s/5bef69a06c9b)