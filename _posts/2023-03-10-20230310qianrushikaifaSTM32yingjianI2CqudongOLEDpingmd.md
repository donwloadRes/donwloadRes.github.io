---
layout: post
title: "嵌入式开发-STM32硬件I2C驱动OLED屏"
date:   2020-09-26
tags: [工程,I2C,硬件,STM32,文件]
comments: true
author: admin
---
# 嵌入式开发-STM32硬件I2C驱动OLED屏

## 资源描述

本仓库提供了一个完整的嵌入式开发工程，主要内容为使用STM32的硬件I2C接口驱动OLED显示屏。该工程包含了CubeMX配置文件和Keil工程文件，方便开发者快速上手和调试。

## 工程特点

- **硬件I2C驱动**：本工程展示了如何使用STM32的硬件I2C接口来驱动OLED显示屏，打破了坊间关于STM32硬件I2C不可用的传言。
- **完整工程**：工程文件完整，包含了CubeMX配置和Keil工程，开发者可以直接下载并进行编译和调试。
- **错误处理**：工程中包含了针对硬件I2C通讯过程中可能出现的错误处理机制，确保即使出现错误，硬件也不会卡死。

## 使用说明

1. **下载工程**：点击仓库页面右上角的“Code”按钮，选择“Download ZIP”下载整个工程文件。
2. **解压文件**：将下载的ZIP文件解压到本地目录。
3. **打开工程**：使用Keil uVision打开解压后的工程文件，进行编译和调试。
4. **配置CubeMX**：如果需要修改硬件配置，可以使用CubeMX打开工程中的.ioc文件进行配置。

## 注意事项

- 本工程适用于STM32系列微控制器，具体型号请参考工程文件中的配置。
- 在使用过程中，如果遇到硬件I2C通讯问题，可以参考工程中的错误处理机制进行调试。

## 贡献

欢迎开发者对本工程进行改进和优化，可以通过提交Pull Request的方式贡献代码。

## 联系我们

如果有任何问题或建议，欢迎通过GitHub的Issues功能进行反馈。

## 下载链接

[嵌入式开发-STM32硬件I2C驱动OLED屏](https://pan.quark.cn/s/b900946d5f28)