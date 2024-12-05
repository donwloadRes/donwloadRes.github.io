---
layout: post
title: "基于STM32F103C8T6的Bootloader程序源码 README"
date:   2024-06-09
tags: [Bootloader,源码,STM32F103C8T6,APP,烧录]
comments: true
author: admin
---
# 基于STM32F103C8T6的Bootloader程序源码 README

---

## 项目简介

本资源提供了专门针对STM32F103C8T6微控制器设计的Bootloader源码，实现了通过串口的在线应用程序更新功能（IAP - In Application Programming）。此Bootloader允许开发者在无需外部编程器的情况下，通过USART1接口上传新的固件镜像，并自动烧录至特定Flash区域。

## 主要特性

- **兼容芯片**: STM32F103C8T6，具有128KByte Flash和20KByte SRAM。
- **波特率设置**: 默认波特率为115200 bps。
- **升级机制**: 程序运行后会在3秒内监听串口，接收.bin文件进行自动烧写。
- **空间划分**: Bootloader占用了0x08000000 - 0x0800FFFF地址范围，而APP空间从0x08010000 - 0x0801FFFF。
- **文件大小限制**: APP程序最大为15KByte。
- **环境需求**: 适用于Keil uVision5 IDE开发环境。
- **源码包含**: `main.c`, `delay.h`, `delay.c`, `iap.h`等，以及必要的配置文件。
- **下载链接**: 提供百度网盘链接，包含工程源码与XCOM V2.6工具，便于用户快速导入与测试。

## 使用指南

1. **配置开发环境**: 确保使用Keil uVision5或更高版本，并配置相应的STM32F103系列CPU。
2. **编译与烧录**: 首次使用需将Bootloader程序烧录到指定的Flash地址。
3. **APP烧录**: 更新APP时，通过串口发送.bin文件至单片机，Bootloader将在接收到信号后自动处理。
4. **注意事项**: APP程序需要调整中断向量表的位置，以适应Bootloader的布局要求。

## 文档与支持

详细实现过程和使用说明，请查阅随资源配套的文章[《基于STM32F103C8T6 的 Bootloder 程序源码（另附百度网盘下载链接）》](https://blog.csdn.net/qq_34854793/article/details/106505794)。文章中包含了技术细节、编译指导以及可能遇到的问题解答，确保您能够顺利集成与应用此Bootloader。

## 版权声明

该资源基于CC 4.0 BY-SA许可协议分享。使用本源码需遵循相应版权规定，并保留原文链接及作者信息。

---

使用此Bootloader前，请仔细阅读上述指南和原始文章内容，以充分发挥其功能并遵守开源协议条款。祝您的开发工作顺利！

## 下载链接

[基于STM32F103C8T6的Bootloader程序源码README分享](https://pan.quark.cn/s/9974de6e8258)