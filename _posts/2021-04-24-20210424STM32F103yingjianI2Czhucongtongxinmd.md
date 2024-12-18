---
layout: post
title: "STM32F103硬件I2C主从通信"
date:   2020-01-10
tags: [I2C,开发板,从机,硬件,主机]
comments: true
author: admin
---
# STM32F103硬件I2C主从通信

本仓库提供了一个基于STM32F103ZET6开发板的硬件I2C主从通信示例。该示例程序兼容正点原子精英开发板，展示了如何在两块开发板之间通过硬件I2C进行通信。

## 资源内容

- **主机Keil MDK工程**：包含主机的I2C通信代码，负责发送数据。
- **从机Keil MDK工程**：包含从机的I2C通信代码，负责接收数据并在中断中处理数据。

## 功能描述

两块STM32F103ZET6开发板通过硬件I2C进行通信。主机负责发送数据，从机在接收到数据后，通过中断处理数据，并通过串口1打印出来。

## 使用方法

1. **硬件连接**：
   - 将两块开发板的I2C引脚（SCL和SDA）连接在一起。
   - 确保两块开发板的电源和地线连接正确。

2. **软件配置**：
   - 使用Keil MDK打开主机和从机的工程文件。
   - 编译并下载主机和从机的程序到对应的开发板上。

3. **运行测试**：
   - 上电后，主机按下复位按钮。
   - 从机将通过串口1打印接收到的数据。

## 注意事项

- 本示例程序兼容正点原子精英开发板，但请确保硬件连接正确。
- 从机在中断中处理数据，因此数据处理速度较快，请确保串口波特率设置合理。

## 贡献

欢迎提交问题和改进建议。如果您有更好的实现方法或优化建议，请提交Pull Request。

## 许可证

本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 下载链接

[STM32F103硬件I2C主从通信](https://pan.quark.cn/s/414d0245ba39)