---
layout: post
title: "STM32课程设计：洗衣机控制器（源代码及Proteus仿真）"
date:   2020-12-28
tags: [仿真,源代码,STM32,Proteus,洗衣机]
comments: true
author: admin
---
# STM32课程设计：洗衣机控制器（源代码及Proteus仿真）

## 项目描述

本资源文件包含了基于STM32单片机的洗衣机控制器课程设计，包括源代码和Proteus仿真文件。该项目旨在模拟一个自动洗衣机的控制系统，通过单片机实现水位选择、程序选择、启动/停止等功能，并通过Proteus仿真平台进行验证。

## 功能概述

1. **水位选择**：用户可以通过一个按键选择6个不同的水位之一，每个水位对应一个水位检测点。在仿真中，水位检测点用六个开关表示。

2. **程序选择**：用户可以通过另一个按键选择8个不同的洗衣程序之一，包括标准洗和轻柔洗。

3. **启动/停止**：用户可以通过一个启动/停止键来控制洗衣机的运行状态。一旦启动，洗衣机将按照所选的程序自动执行洗衣过程。

4. **洗衣过程模拟**：在仿真中，项目模拟了标准洗和轻柔洗两个自动洗衣程序的执行过程。当洗衣机启动后，会打开进水电磁阀（用一个LED灯模拟），并按照预设的程序进行洗衣。

## 文件结构

- `src/`：包含STM32的源代码文件。
- `sim/`：包含Proteus仿真文件。

## 使用说明

1. **源代码**：将`src/`目录下的源代码文件导入到STM32开发环境中，编译并下载到STM32单片机中。

2. **仿真**：打开`sim/`目录下的Proteus仿真文件，运行仿真以验证洗衣机的控制逻辑。

## 注意事项

- 在仿真中，水位检测点用六个开关表示，用户可以通过这些开关模拟不同的水位状态。
- 仿真中的LED灯用于模拟进水电磁阀的开关状态。

## 贡献

欢迎对该项目进行改进和扩展。如果您有任何建议或发现了问题，请提交Issue或Pull Request。

## 许可证

本项目采用MIT许可证，详情请参阅`LICENSE`文件。

## 下载链接

[STM32课程设计洗衣机控制器源代码及Proteus仿真分享](https://pan.quark.cn/s/e64c56141c79)