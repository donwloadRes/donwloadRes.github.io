---
layout: post
title: "STM32实现PWM输出频率1kHz占空比50的方波和呼吸灯"
date:   2024-06-01
tags: [TIM,GPIO,TIM3,PWM,TimeBaseStructure]
comments: true
author: admin
---
# STM32实现PWM输出频率1kHz占空比50%的方波和呼吸灯

本资源文件详细介绍了如何使用STM32微控制器实现PWM输出，具体包括输出频率为1kHz、占空比为50%的方波以及实现呼吸灯效果。通过本教程，您将学习到如何配置STM32的定时器和GPIO，以及如何编写代码来生成所需的PWM信号。

## 内容概述

1. **PWM输出1kHz方波的实现**
   - 选择合适的GPIO引脚
   - 初始化GPIO
   - 配置定时器模式
   - 下载程序并观察现象

2. **呼吸灯的实现**
   - 计算PWM数据表
   - 初始化GPIO
   - 配置NVIC
   - 配置TIM3模式

## 使用说明

1. **硬件准备**
   - 野火指南者开发板
   - STM32f103VET6芯片
   - 连接LED灯

2. **软件准备**
   - STM32CubeMX
   - Keil uVision

3. **步骤**
   - 使用STM32CubeMX生成初始化代码
   - 在Keil uVision中编写和调试代码
   - 下载程序到开发板并观察输出效果

## 代码示例

以下是部分代码示例，展示了如何配置定时器和GPIO以实现PWM输出：

```c
static void TIM3_GPIO_Config(void) {
    GPIO_InitTypeDef GPIO_InitStructure;
    RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOA | RCC_APB2Periph_AFIO, ENABLE);
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_AF_PP;
    GPIO_InitStructure.GPIO_Pin = GPIO_Pin_6;
    GPIO_InitStructure.GPIO_Speed = GPIO_Speed_50MHz;
    GPIO_Init(GPIOA, &GPIO_InitStructure);
}

static void TIM3_Mode_Config(void) {
    TIM_TimeBaseInitTypeDef TIM_TimeBaseStructure;
    TIM_OCInitTypeDef TIM_OCInitStructure;
    RCC_APB1PeriphClockCmd(RCC_APB1Periph_TIM3, ENABLE);
    TIM_TimeBaseStructure.TIM_Period = (1000 - 1);
    TIM_TimeBaseStructure.TIM_Prescaler = (72 - 1);
    TIM_TimeBaseStructure.TIM_ClockDivision = TIM_CKD_DIV1;
    TIM_TimeBaseStructure.TIM_CounterMode = TIM_CounterMode_Up;
    TIM_TimeBaseInit(TIM3, &TIM_TimeBaseStructure);
    TIM_OCInitStructure.TIM_OCMode = TIM_OCMode_PWM1;
    TIM_OCInitStructure.TIM_OutputState = TIM_OutputState_Enable;
    TIM_OCInitStructure.TIM_Pulse = 500;
    TIM_OCInitStructure.TIM_OCPolarity = TIM_OCPolarity_Low;
    TIM_OC1Init(TIM3, &TIM_OCInitStructure);
    TIM_OC1PreloadConfig(TIM3, TIM_OCPreload_Enable);
    TIM_ARRPreloadConfig(TIM3, ENABLE);
    TIM_Cmd(TIM3, ENABLE);
}
```

## 总结

通过本教程，您将掌握如何在STM32上实现PWM输出，并能够应用到实际项目中。希望本资源对您的学习和开发有所帮助。

## 下载链接

[STM32实现PWM输出频率1kHz占空比50的方波和呼吸灯](https://pan.quark.cn/s/20d0cb4a3cf2)