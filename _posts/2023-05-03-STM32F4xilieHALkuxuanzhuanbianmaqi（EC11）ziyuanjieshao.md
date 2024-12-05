---
layout: post
title: "STM32F4系列HAL库旋转编码器（EC11）资源介绍"
date:   2023-07-17
tags: [GPIO,EC11,旋转,HAL,编码器]
comments: true
author: admin
---
# STM32F4系列HAL库旋转编码器（EC11）资源介绍

本资源文件详细介绍了如何使用STM32F4系列的HAL库处理EC11旋转编码器的电气连接、波形分析，并提供了HAL初始化代码及实战GitHub链接。通过外部中断捕获AB相的旋转信息，实现顺/逆时针旋转的计数和回调处理。

## 概述

EC11是一种增量型AB相旋转编码器，常用于各种需要大量数据范围的情况，如收音机选台、音量选择等。增量型编码器输出的信号与当前位置无关，仅与旋转的方向和角度有关。AB相输出模式通过两个线输出根据相位判断方向，根据高低电平数量判断走过度数。

## 电气连接

EC11常见额定电压为5V，实测3.3V也可以驱动，但不建议使用3.3V（会出现杂波）。阻容用于进行上拉输出和硬件滤波。A、B为旋转信息的输出（两相），C为接地，SW为内部的开关，可以当作轻触按键使用（注意加软件滤波）。

## 波形分析

每转动一格，AB相会出现一个持续10-150ms的低电平，默认为高电平状态。顺时针转动时A相的低电平会比B相提前，逆时针转动时A相的低电平会比B相延后。

## 思路

通过在A（或B）相的一个边沿（上升下降均可）检测另一相的电平高低，即可判断旋转方向。因此需要的外设有：外部中断一个输入状态的GPIO。注意：因为要直接接入5V的电压，因此需要GPIO耐压为5V（即为数据手册表FT的管脚）。未避免干扰，输入状态和外部中断的GPIO设置为上拉模式。

## HAL初始化

外部中断和NVIC GPIO初始化代码如下：

```c
// 外部中断
#define EC11_A_GPIO_Group GPIOA
#define EC11_A_GPIO_PIN GPIO_PIN_0
// GPIO输入
#define EC11_B_GPIO_Group GPIOA
#define EC11_B_GPIO_PIN GPIO_PIN_1

void EC11_Decode(void (*Clockwise)(void), void (*Anticlockwise)(void)) {
    // Delay_ms(1);
    if (HAL_GPIO_ReadPin(EC11_B_GPIO_Group, EC11_B_GPIO_PIN) == GPIO_PIN_SET) {
        Anticlockwise();
    } else {
        Clockwise();
    }
}
```

## 成品

GitHub链接提供了完整的实战代码，可供参考和使用。

## 总结

本资源文件通过详细的步骤和代码示例，帮助用户快速掌握如何使用STM32F4的HAL库处理EC11旋转编码器，实现旋转方向的判断和计数功能。

## 下载链接

[STM32F4系列HAL库旋转编码器EC11资源介绍](https://pan.quark.cn/s/725375e37bf8)