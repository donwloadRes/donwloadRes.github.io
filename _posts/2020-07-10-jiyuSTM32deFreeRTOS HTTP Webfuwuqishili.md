---
layout: post
title: "基于STM32的FreeRTOS HTTP Web服务器示例"
date:   2021-09-25
tags: [示例,DHCP,以太网,页面,服务器]
comments: true
author: admin
---
# 基于STM32的FreeRTOS HTTP Web服务器示例

## 项目描述

本项目提供了一个基于STM32 HAL和FreeRTOS的HTTP Web服务器示例，适用于Nucleo-F746ZG开发板。该示例使用了LwIP Netconn API，并包含了两个HTML页面：

1. **主页**：这是一个静态页面，提供了有关STM32F7和LwIP堆栈的基本信息。
2. **动态页面**：该页面每1秒钟刷新一次，显示运行时的RTOS统计信息。

## 功能特性

- **DHCP支持**：如果网络中存在DHCP服务器，可以通过启用DHCP进程来分配动态IP地址（在`main.h`中定义`USE_DHCP`）。默认情况下，使用DHCP。
- **以太网状态指示**：通过LED灯来指示以太网电缆的连接状态：
  - **LED1**：连接以太网电缆时亮起。
  - **LED3**：未连接以太网电缆时亮起。

## 注意事项

- 该示例代码改编自ST Microelectronics提供的“LwIP HTTP Server Netconn RTOS”示例。
- 构建此示例需要使用Make工具。

## 使用说明

1. 将项目代码下载到本地。
2. 根据需要修改`main.h`中的配置，例如是否启用DHCP。
3. 使用Make工具编译项目。
4. 将生成的二进制文件烧录到Nucleo-F746ZG开发板中。
5. 连接以太网电缆，并通过浏览器访问开发板的IP地址，查看Web服务器页面。

## 贡献

欢迎提交问题和改进建议，帮助我们完善这个示例项目。

## 下载链接

[基于STM32的FreeRTOSHTTPWeb服务器示例](https://pan.quark.cn/s/9cccd99228d8)