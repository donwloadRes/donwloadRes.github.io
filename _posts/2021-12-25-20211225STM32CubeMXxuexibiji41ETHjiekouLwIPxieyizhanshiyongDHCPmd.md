---
layout: post
title: "STM32CubeMX学习笔记41ETH接口LwIP协议栈使用DHCP"
date:   2022-11-11
tags: [LwIP,DHCP,配置,STM32CubeMX,ETH]
comments: true
author: admin
---
# STM32CubeMX学习笔记（41）——ETH接口+LwIP协议栈使用（DHCP）

本资源文件深入介绍了如何在STM32F4系列微控制器上配置以太网（ETH）接口，并结合LwIP轻量级TCP/IP协议栈实现DHCP动态主机配置协议的功能。该教程适合嵌入式开发者，尤其是那些致力于STM32平台网络功能开发的工程师。

## 概览

文章详细解释了STM32F4的以太网外设特性，包括其MAC层的运作方式和RMII接口的使用。此外，还涵盖了LwIP协议栈的基本概念及其在无操作系统环境下的配置技巧。通过本教程，读者将学会：

- 如何使用STM32CubeMX配置STM32F4的Ethernet接口至RMII模式。
- LwIP协议栈的基本配置，包括DHCP模块启用，以便让设备能在网络中自动获取IP地址。
- 与LAN8720A PHY芯片的配合使用，包括正确的引脚配置和时钟设置。
- 如何在主循环中添加必要的代码来处理DHCP过程，以及如何打印出动态分配的IP地址、子网掩码和默认网关等信息。

## 实践步骤概览

1. **环境准备**：启动STM32CubeMX，选择相应的MCU和项目设置，重点调整时钟配置以满足以太网工作的需要。
2. **ETH配置**：在Connectivity选项里，配置ETH接口为RMII模式，确保与外部PHY芯片LAN8720A兼容，并设置适当的自适应速度和全双工模式。
3. **GPIO和PHY引脚配置**：正确映射ETH相关引脚至STM32的特定GPIO。
4. **LwIP配置**：在Middleware部分启用LwIP协议栈，并详细配置以适应无操作系统环境，特别是DHCP模块的启用和网络接口的初始化。
5. **代码生成与修改**：通过STM32CubeMX生成基础代码框架，在主函数中加入LwIP的处理循环和代码来显示DHCP获得的网络信息。
6. **编译与验证**：完成以上步骤后，编译工程并在实际硬件上验证，确认设备能成功获取IP并通过ping命令验证网络连通性。

通过跟随本教程的指南，开发者可以快速上手STM32平台上的以太网编程和网络协议栈配置，为构建网络化的嵌入式系统奠定坚实的基础。

## 下载链接

[STM32CubeMX学习笔记41ETH接口LwIP协议栈使用DHCP](https://pan.quark.cn/s/e611bb3889d7)