---
layout: post
title: "PCAN PRO-PRO FD USB2CAN固件实现"
date:   2023-10-09
tags: [固件,PCAN,FD,PRO,View]
comments: true
author: admin
---
# PCAN PRO/PRO FD USB2CAN固件实现

## 描述

本资源文件提供了一个适用于基于STM32F4的廉价硬件的PCAN PRO/PRO FD USB2CAN固件实现。该固件旨在用于任何具有8MHz振荡器的基于STM32F407/405的开发板。

### 目标硬件
- 基于STM32F407/405的开发板
- 8MHz振荡器

### 引脚排列
- **PC10**: 状态指示灯
- **PA2 / PA3**: TX / RX CAN1 LED
- **PC6 / PC7**: TX / RX CAN2 LED
- **PB8 / PB9**: CAN1 接收/发送
- **PB5 / PB6**: CAN2 接收/发送
- **PB14 / PB15**: USB DM / DP

### 功能特性
- 在Linux中开箱即用
- 与Linux PCAN-View兼容（需要安装）
- 在Windows中与PCAN-View和PCAN-Explorer一起使用

### 限制
- PRO FD固件不支持FD帧，因为bxCAN不支持FD帧，但可以与经典CAN一起使用
- 某些协议特定消息尚未实现
- 确保将PB14/PB15引脚用于USB

### 工具链
- GNU Arm嵌入式工具链（最新版本）

## 使用说明

1. **硬件准备**: 确保使用具有8MHz振荡器的STM32F407/405开发板。
2. **固件烧录**: 使用GNU Arm嵌入式工具链将固件烧录到目标硬件。
3. **连接**: 按照引脚排列连接硬件。
4. **操作系统支持**:
   - **Linux**: 固件开箱即用，确保安装PCAN-View以进行通信。
   - **Windows**: 使用PCAN-View或PCAN-Explorer进行通信。

## 注意事项
- 确保PB14/PB15引脚用于USB连接。
- 由于bxCAN不支持FD帧，PRO FD固件仅支持经典CAN。

## 贡献
欢迎提交问题和改进建议，帮助完善此固件实现。

## 下载链接

[PCANPROPROFDUSB2CAN固件实现](https://pan.quark.cn/s/3ddd9c0b77ef)