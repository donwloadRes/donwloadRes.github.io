---
layout: post
title: "STM32F103R6按键中断点亮LED仿真实例"
date:   2021-04-16
tags: [STM32F103R6,LED,Proteus,Keil5,仿真]
comments: true
author: admin
---
# STM32F103R6按键中断点亮LED仿真实例

## 项目简介

本项目基于STM32F103R6芯片，通过Proteus仿真和Keil5开发环境，实现了一个简单的按键中断控制LED灯的点亮与熄灭。该项目参考了《STM32嵌入式微控制器快速上手》（第二版）第六章中的实例6.5.1，并提供了详细的连线图和代码实现。

## 功能描述

- **硬件平台**：STM32F103R6芯片
- **开发环境**：Keil5
- **仿真工具**：Proteus
- **功能实现**：通过按键触发中断，控制LED灯的点亮与熄灭

## 项目结构

```
STM32F103R6_LED_Interrupt/
├── Keil5_Project/
│   ├── main.c
│   ├── stm32f10x_it.c
│   ├── stm32f10x_it.h
│   └── ...
├── Proteus_Simulation/
│   ├── STM32F103R6_LED_Interrupt.pdsprj
│   └── STM32F103R6_LED_Interrupt.pdsprj.bak
└── README.md
```

## 使用说明

1. **Keil5项目**：
   - 打开`Keil5_Project`文件夹中的Keil5工程文件。
   - 编译并生成HEX文件。

2. **Proteus仿真**：
   - 打开`Proteus_Simulation`文件夹中的Proteus工程文件。
   - 将生成的HEX文件加载到STM32F103R6芯片中。
   - 运行仿真，观察按键中断对LED灯的控制效果。

## 参考资料

- **书籍**：《STM32嵌入式微控制器快速上手》（第二版）第六章，实例6.5.1

## 贡献

欢迎对本项目进行改进和扩展，如果您有任何建议或发现了问题，请提交Issue或Pull Request。

## 许可证

本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 下载链接

[STM32F103R6按键中断点亮LED仿真实例](https://pan.quark.cn/s/b9da3053f5d7)