---
layout: post
title: "基于STM32F401的温湿度检测显示1602加仿真"
date:   2024-10-15
tags: [GPIO,温湿度,1602,STM32F401,aaa]
comments: true
author: admin
---
# 基于STM32F401的温湿度检测显示1602加仿真

## 项目描述

本项目基于STM32F401微控制器，实现了一个温湿度检测与显示系统。系统通过传感器采集环境中的温度和湿度数据，并在1602液晶显示屏上实时显示。此外，项目还包含了仿真功能，方便用户在开发过程中进行调试和验证。

## 功能特点

- **温湿度检测**：通过传感器实时采集环境中的温度和湿度数据。
- **1602液晶显示**：将采集到的温湿度数据实时显示在1602液晶屏上。
- **预警功能**：当温度或湿度超过预设的预警值时，系统会触发LED警报。
- **仿真支持**：提供仿真功能，方便用户在开发过程中进行调试和验证。

## 硬件需求

- STM32F401微控制器
- 温湿度传感器
- 1602液晶显示屏
- LED灯
- 按键

## 软件需求

- Keil uVision 或其他支持STM32开发的IDE
- STM32CubeMX（可选，用于配置硬件资源）

## 代码说明

### 主要变量

- `temperature`：存储当前的温度值。
- `humidness`：存储当前的湿度值。
- `warningtep`：预警温度值，默认设置为30℃。
- `warninghum`：预警湿度值，默认设置为80%。
- `change`：用于改变预警温度或湿度的标志。
- `jump`：用于判断是否有按键按下。

### LED初始化

```c
void LED_Init(void) {
    GPIO_InitTypeDef  aaa;  // 定义一个结构体变量
    // 1、使能指定的GPIO模块时钟
    RCC_AHB1PeriphClockCmd(RCC_AHB1Periph_GPIOD, ENABLE);
    // 2、初始化引脚
    aaa.GPIO_Pin   = GPIO_Pin_5 | GPIO_Pin_8 | GPIO_Pin_12;  // 引脚号选择
    aaa.GPIO_Mode  = GPIO_Mode_OUT;  // 输出模式
    aaa.GPIO_OType = GPIO_OType_PP;  // 推挽输出
    aaa.GPIO_Speed = GPIO_High_Speed;  // 高速
    GPIO_Init(GPIOD, &aaa);  // 初始化GPIO
}
```

## 使用说明

1. **硬件连接**：按照电路图连接STM32F401、温湿度传感器、1602液晶显示屏和LED灯。
2. **软件配置**：使用Keil uVision或其他IDE打开项目，编译并下载代码到STM32F401。
3. **运行测试**：系统启动后，1602液晶屏将显示当前的温湿度数据。当温度或湿度超过预警值时，LED灯会亮起。

## 注意事项

- 请确保所有硬件连接正确，避免短路或连接错误导致设备损坏。
- 在修改预警值时，请根据实际需求进行调整，避免误报警。

## 贡献

欢迎对本项目进行改进和优化，如果您有任何建议或问题，请提交Issue或Pull Request。

## 许可证

本项目采用MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[基于STM32F401的温湿度检测显示1602加仿真](https://pan.quark.cn/s/8edd1e289ba2)