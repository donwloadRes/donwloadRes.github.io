---
layout: post
title: "STM32F103串口IAP + Ymodem 升级"
date:   2024-06-02
tags: [BootLoader,串口,固件,App,开发板]
comments: true
author: admin
---
# STM32F103串口IAP + Ymodem 升级

## 项目描述
本项目提供了一个基于STM32F103ZET6开发板的串口IAP（In-Application Programming）和Ymodem协议的固件升级方案。代码包含BootLoader和App程序，可直接编译下载使用。

## 环境配置
- **单片机**: 正点原子STM32F103ZET6开发板
- **工具**: 
  - STM32CubeMX 5.1
  - Pack: stm32cube_fw_f4_v1240
  - SecureCRT 8.5.3

## 功能介绍
1. **BootLoader**: 负责通过串口接收Ymodem协议传输的固件数据，并将其写入Flash中。
2. **App程序**: 用户应用程序，可通过BootLoader进行升级。

## 使用说明
1. **编译与下载**:
   - 使用STM32CubeMX生成工程文件。
   - 使用Keil或其他编译工具编译BootLoader和App程序。
   - 将BootLoader程序下载到开发板中。
   - 将App程序下载到开发板中。

2. **固件升级**:
   - 使用SecureCRT连接开发板的串口。
   - 在SecureCRT中选择Ymodem协议，发送新的App固件文件。
   - BootLoader将自动接收并写入新的固件。

## 注意事项
- 确保BootLoader和App程序的Flash地址分配正确，避免覆盖。
- 在升级过程中，请勿断电或中断串口通信，以免造成固件损坏。

## 贡献
欢迎提交Issue和Pull Request，共同完善本项目。

## 许可证
本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 下载链接

[STM32F103串口IAPYmodem升级](https://pan.quark.cn/s/ed386bc0a6b8)