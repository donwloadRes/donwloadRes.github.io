---
layout: post
title: "STM32F103RCT6 定时器简单用法教程"
date:   2020-06-15
tags: [定时器,TIM,TIM2,NVIC,STM32F103RCT6]
comments: true
author: admin
---
# STM32F103RCT6 定时器简单用法教程

欢迎来到STM32F103RCT6定时器基础教程。本文档旨在为你详细介绍如何在STM32F103RCT6微控制器上配置和使用定时器，特别是针对新手开发者。STM32F103RCT6是一款基于ARM Cortex-M3核心的高效能微控制器，配备了多种定时器类型，包括高级控制定时器、通用定时器和基本定时器，分别满足不同的应用场景。

## 定时器概述

STM32F103RCT6提供了丰富多样的定时器选项，分为三类：
- **高级控制定时器**: TIM1和TIM8，具备16位向上/下计数能力，支持多种工作模式，如PWM、输入捕获和输出比较。
- **通用定时器**: 包括TIM2至TIM5，同样为16位，适用于更广泛的计时和控制任务。
- **基本定时器**: TIM6和TIM7，适合简单的定时任务，如延时和周期性中断。

## 初始化步骤

### 示例代码概览

以下是配置TIM2进行简单定时的代码段，展示如何设置计数器、预分频器和中断：

```c
#include "stm32f10x.h"

void TIM2_Configuration(void) {
    TIM_TimeBaseInitTypeDef TIM_TimeBaseStructure;
    NVIC_InitTypeDef NVIC_InitStructure;

    RCC_APB1PeriphClockCmd(RCC_APB1Periph_TIM2, ENABLE); // 使能TIM2时钟

    TIM_TimeBaseStructure.TIM_Period = 9999; // 设置自动重载值，这里假设我们想让定时器每隔一段时间中断
    TIM_TimeBaseStructure.TIM_Prescaler = 7199; // 预分频设置，假设系统时钟为72MHz，则此值让定时器约1ms中断一次
    TIM_TimeBaseStructure.TIM_CounterMode = TIM_CounterMode_Up; // 上升沿计数模式
    TIM_TimeBaseStructure.TIM_ClockDivision = 0;
    TIM_TimeBaseInit(TIM2, &TIM_TimeBaseStructure);

    TIM_ITConfig(TIM2, TIM_IT_Update, ENABLE); // 启用定时器更新中断

    NVIC_InitStructure.NVIC_IRQChannel = TIM2_IRQn;
    NVIC_InitStructure.NVIC_IRQChannelPreemptionPriority = 0; // 抢占优先级
    NVIC_InitStructure.NVIC_IRQChannelSubPriority = 1;   // 子优先级
    NVIC_InitStructure.NVIC_IRQChannelCmd = ENABLE;
    NVIC_Init(&NVIC_InitStructure);

    TIM_Cmd(TIM2, ENABLE); // 启动TIM2
}

void TIM2_IRQHandler(void) {
    if(TIM_GetITStatus(TIM2, TIM_IT_Update) != RESET) { // 检测定时器更新中断
        // 在此处添加中断处理逻辑
        TIM_ClearITPendingBit(TIM2, TIM_IT_Update); // 清除中断标志位
    }
}
```

## 使用注意事项

- 在配置定时器之前，务必确保相应的GPIO口已被正确配置，尤其是当定时器连接到输出引脚时。
- 调整预分频器和自动重装载值来获得所需的定时周期。
- 不同的应用场景可能需要调整中断优先级，确保系统的响应符合预期。
- 记得在主函数中启动定时器，并在合适的位置注册中断处理函数。

这份简明教程为你入门STM32F103RCT6的定时器使用打下了坚实的基础。深入实践，结合官方参考手册和更多实例，你将能够灵活运用这些强大的定时器功能来提升你的项目性能。

## 下载链接

[STM32F103RCT6定时器简单用法教程](https://pan.quark.cn/s/ed645dc2e71d)