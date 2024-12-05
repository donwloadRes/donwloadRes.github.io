---
layout: post
title: "STM32F103模拟IIC控制4针096寸OLED显示屏
date   20240223
tags OLEDIIC显示STM32F103显示屏
comments true
author admin

 STM32F103模拟IIC控制4针096寸OLED显示屏

 概述

本文档提供了一套详细的教程和代码示例用于指导如何使用STM32F103系列微控制器通过模拟IIC接口来控制一款4针的096英寸OLED显示屏此显示屏因其小巧的尺寸27mm x 26mm和高分辨率128x64像素成为嵌入式项目中的优选显示部件文章基于C语言编写适合那些想要在STM32平台上集成OLED显示功能的开发者

 功能特点

 接口灵活支持包括IIC在内的四种接口方式本次教程集中于模拟IIC控制
 电源友好直接使用33V供电无需额外升压
 自发光特性OLED显示技术自带光源无需背光对比度高且节能
 简易操作通过简单的库函数调用即可实现文字数字和图形的显示
 示例丰富包含汉字显示字符串显示图片显示BMP点线图绘制等功能演示

 快速指南

 硬件准备

 STM32F103开发板
 096英寸OLED显示屏4针接口
 接线配置确保正确连接OLED的四针至STM32对应GPIO

 软件要求

 编译环境Keil uVision或STM32CubeIDE等支持ARM CortexM3的IDE
 库文件包括OLED驱动库IIC模拟函数取字模工具等

 核心步骤

1 配置IIC模拟在myiich中定义控制OLED的GPIO引脚
2 初始化OLED调用OLEDInit完成初始化过程
3 显示操作使用如OLEDShowCHineseOLEDShowString等函数显示文本或利用OLEDDrawBMP显示位图图像
4 延时与循环确保适当的延迟以观察显示效果通常通过delayms函数实现

 示例代码片段

展示如何显示一个简单的汉字

c
include oledh
include myiich"
date:   2024-02-23
tags: [OLED,IIC,显示,STM32F103,显示屏]
comments: true
author: admin
---
# STM32F103模拟IIC控制4针0.96寸OLED显示屏

## 概述

本文档提供了一套详细的教程和代码示例，用于指导如何使用STM32F103系列微控制器通过模拟IIC接口来控制一款4针的0.96英寸OLED显示屏。此显示屏因其小巧的尺寸（27mm x 26mm）和高分辨率（128x64像素）成为嵌入式项目中的优选显示部件。文章基于C语言编写，适合那些想要在STM32平台上集成OLED显示功能的开发者。

## 功能特点

- **接口灵活**：支持包括IIC在内的四种接口方式，本次教程集中于模拟IIC控制。
- **电源友好**：直接使用3.3V供电，无需额外升压。
- **自发光特性**：OLED显示技术自带光源，无需背光，对比度高且节能。
- **简易操作**：通过简单的库函数调用即可实现文字、数字和图形的显示。
- **示例丰富**：包含汉字显示、字符串显示、图片显示（BMP）、点线图绘制等功能演示。

## 快速指南

### 硬件准备

- **STM32F103开发板**
- **0.96英寸OLED显示屏**（4针接口）
- 接线配置，确保正确连接OLED的四针至STM32对应GPIO。

### 软件要求

- 编译环境：Keil uVision或STM32CubeIDE等支持ARM Cortex-M3的IDE。
- 库文件：包括OLED驱动库、IIC模拟函数、取字模工具等。

### 核心步骤

1. **配置IIC模拟**：在`myiic.h`中定义控制OLED的GPIO引脚。
2. **初始化OLED**：调用`OLED_Init()`完成初始化过程。
3. **显示操作**：使用如`OLED_ShowCHinese()`、`OLED_ShowString()`等函数显示文本，或利用`OLED_DrawBMP()`显示位图图像。
4. **延时与循环**：确保适当的延迟以观察显示效果，通常通过`delay_ms()`函数实现。

### 示例代码片段

展示如何显示一个简单的汉字：

```c
#include "oled.h"
#include "myiic.h"

int main(void) {
    delay_init();   // 初始化延时函数
    IIC_Init();     // 初始化IIC
    OLED_Init();    // OLED初始化
    OLED_Clear();   // 清屏

    OLED_ShowCHinese(8, 0, 0);  // 在指定位置显示汉字
    
    while(1) {
        // 循环显示更多内容或执行其他显示逻辑
        OLED_ShowString(0, 2, "Hello World", 16);
        delay_ms(2000);
        OLED_Clear();
    }
}
```

## 注意事项

- 在实际应用中，务必检查OLED模块的具体型号和引脚定义，以匹配正确的代码配置。
- 避免直接将OLED模块连接到5V电源，以防损坏。
- 字模提取一般通过PC工具（如PCtoLCD2002）完成，确保正确生成所需字模数据。

通过以上步骤，您就可以在STM32F103上成功运行OLED显示屏，为其嵌入式项目增添视觉交互能力。祝您的开发顺利！

## 下载链接

[STM32F103模拟IIC控制4针0.96寸OLED显示屏](https://pan.quark.cn/s/cd1c8d6cfa94)