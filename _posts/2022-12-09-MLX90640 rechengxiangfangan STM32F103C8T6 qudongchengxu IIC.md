---
layout: post
title: "MLX90640 热成像方案 STM32F103C8T6 驱动程序 IIC"
date:   2022-07-13
tags: [MLX90640,STM32F103C8T6,模块,连接,驱动程序]
comments: true
author: admin
---
# MLX90640 热成像方案 STM32F103C8T6 驱动程序 IIC

## 简介
本仓库提供了一个基于STM32F103C8T6微控制器的MLX90640热成像模块的驱动程序，通过IIC接口实现数据通信。该方案适用于需要进行非接触式温度检测的应用场景。

## 硬件设置
1. **购买测温模块**：请访问[淘宝链接](https://item.taobao.com/item.htm?spm=a230r.1.14.61.53f77712T7toli&id=684052577888&ns=1&abbucket=15#detail)购买所需的测温模块。
2. **硬件连接**：
   - **电源连接**：
     - 电脑USB转串口线 -> STM32F103C8T6模块 -> MLX90640测温模块
     - USB口红 -> 5V -> 5V
     - 黑线 -> GND -> GND
   - **信号连接**：
     - 绿线 -> A9
     - 白线 -> A10
     - B6 -> SDA
     - B7 -> SCL
   - **调试连接**：
     - USB口 -> ST_LINK
     - 3V3 -> SWIO
     - SWCLK -> GND
     - PS接地

## 软件设置
1. **安装开发环境**：在电脑上安装MDK Keil软件及STM32相关支持文件。
2. **运行热力图软件**：下载并运行热力图软件，观察是否输出图像数据。热力图软件下载链接：[CSDN下载](https://download.csdn.net/download/scurobot/87667941)

## 调试与测试
- 如果热力图软件没有输出图像数据，请尝试调换SDA和SCL，或者调换RXD和TXD重新测试。

## 注意事项
- 确保所有硬件连接正确无误。
- 在调试过程中，注意检查电源和信号线的连接是否稳定。

## 贡献
欢迎大家贡献代码和提出改进建议，共同完善这个项目。

## 许可证
本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 下载链接

[MLX90640热成像方案STM32F103C8T6驱动程序IIC](https://pan.quark.cn/s/41d6df315973)