---
layout: post
title: "STM32G071 USBPD Sink 源码下载"
date:   2021-08-13
tags: [USBPD,源码,STM32G071,开发板,Discover]
comments: true
author: admin
---
# STM32G071 USBPD Sink 源码下载

## 资源介绍

本仓库提供了一个名为 `STM32G071_USBPD_SINK.zip` 的资源文件下载。该文件包含了基于 STM32G071 Discover 官方开发板的纯净 USBPD 源码。源码仅保留了 USBPD 协议的核心文件，方便用户进行修改和优化，并添加自定义功能。

## 资源特点

- **纯净源码**：仅保留了 USBPD 协议的核心文件，去除了与开发板其他外设（如 LCD、按键等）相关的代码，方便用户专注于 USBPD 协议的开发。
- **二次开发友好**：源码仅依赖于开发板的 TYPE C 连接器、VBUS、CC1、CC2 控制电路以及功率传感器，与其他外设无任何关联，用户可以放心进行二次开发。
- **官方支持**：基于 STM32G071 Discover 官方开发板，确保代码的可靠性和兼容性。

## 适用场景

- 需要对 USBPD 协议进行深入研究和优化的开发者。
- 希望在 STM32G071 平台上实现自定义 USBPD 功能的开发者。
- 需要一个干净、简洁的 USBPD 源码作为基础进行二次开发的开发者。

## 使用说明

1. 下载 `STM32G071_USBPD_SINK.zip` 文件。
2. 解压文件到本地目录。
3. 使用 STM32CubeIDE 或其他 STM32 开发工具打开项目。
4. 根据需要进行代码的修改和优化。
5. 编译并烧录到 STM32G071 Discover 开发板上进行测试。

## 注意事项

- 本源码仅适用于 STM32G071 Discover 开发板，其他型号的开发板可能需要进行适配。
- 源码中不包含与 LCD、按键等外设相关的代码，用户在添加这些功能时需要自行实现。

## 贡献与反馈

如果您在使用过程中遇到任何问题或有改进建议，欢迎提交 Issue 或 Pull Request。我们期待您的反馈和贡献！

## 下载链接

[STM32G071USBPDSink源码下载](https://pan.quark.cn/s/79a9d0831ae8)