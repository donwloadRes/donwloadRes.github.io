---
layout: post
title: "LittleVGL LVGL 移植到 STM32F429IG 野火开发板"
date:   2022-01-12
tags: [开发板,演示,移植,LittleVGL,STM32F429IG]
comments: true
author: admin
---
# LittleVGL (LVGL) 移植到 STM32F429IG 野火开发板

## 资源介绍

本仓库提供了一个将 LittleVGL (LVGL) 图形库移植到 STM32F429IG 野火 STM32F429 至尊开发板的资源文件。该资源包含了官方演示程序，展示了如何在开发板上实现各种小控件的演示，并移植了触摸以及 LTDC 驱动。

## 主要内容

- **开发板型号**: STM32F429IGTx
- **开发板品牌**: 野火 STM32F429 至尊开发板
- **LVGL 版本**: v7.5
- **开发环境**: MDK-ARM Keil5
- **库类型**: STD 库
- **显示屏**: 800*480 的 RGB 显示屏
- **驱动**: 移植了触摸驱动和 LTDC 驱动
- **DMA2D**: 已开启 DMA2D 打印机例程，但由于 Flash 内存不足，无法演示

## 功能特点

- **图形库移植**: 成功将 LittleVGL (LVGL) 图形库移植到 STM32F429IG 开发板上。
- **触摸支持**: 移植了触摸驱动，支持触摸屏操作。
- **LTDC 驱动**: 移植了 LTDC 驱动，支持 800*480 的 RGB 显示屏。
- **官方演示程序**: 包含了 LittleVGL 官方的演示程序，展示了各种小控件的使用。
- **DMA2D 支持**: 开启了 DMA2D 打印机例程，但由于 Flash 内存不足，无法完整演示。

## 使用说明

1. **下载资源**: 下载本仓库中的资源文件。
2. **导入工程**: 使用 MDK-ARM Keil5 打开工程文件。
3. **编译运行**: 编译工程并下载到 STM32F429IG 开发板上。
4. **查看演示**: 运行程序后，可以在显示屏上查看 LittleVGL 的官方演示程序。

## 注意事项

- 由于 Flash 内存不足，DMA2D 打印机例程无法完整演示，请注意内存使用情况。
- 确保开发板连接正确，特别是触摸屏和显示屏的连接。

## 贡献与反馈

如果您在使用过程中遇到问题或有改进建议，欢迎提交 Issue 或 Pull Request。

## 下载链接

[LittleVGLLVGL移植到STM32F429IG野火开发板](https://pan.quark.cn/s/d6702687315e)