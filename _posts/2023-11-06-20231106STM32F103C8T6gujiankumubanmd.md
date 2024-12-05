---
layout: post
title: "STM32F103C8T6 固件库模板"
date:   2020-05-03
tags: [文件,工程,固件,MDK5,模板]
comments: true
author: admin
---
# STM32F103C8T6 固件库模板

## 简介

本资源提供了一个基于STM32F103C8T6微控制器的固件库模板，适用于使用ST公司提供的标准外设库进行开发。该模板包含了必要的文件和目录结构，方便开发者快速搭建工程环境，减少重复性工作。

## 内容

- **CORE**: 存放核心文件和启动文件。
- **OBJ**: 用于存放编译过程文件以及生成的hex文件。
- **STM32F10x_FWLib**: 存放ST官方提供的库函数源码文件。
- **USER**: 存放工程文件、主函数文件以及其他必要的配置文件。

## 使用步骤

1. **准备资料**:
   - 下载并解压V3.5版本的固件库包。
   - 安装MDK5开发环境。

2. **新建工程**:
   - 在电脑的某个目录下新建一个文件夹，用于存放工程文件。
   - 使用MDK5新建工程，并选择STM32F103C8T6芯片型号。

3. **添加文件**:
   - 将固件库包中的相关文件复制到工程目录下的相应文件夹中。
   - 在MDK5中添加这些文件到工程中。

4. **配置工程**:
   - 设置编译中间文件的存放路径。
   - 配置头文件路径，确保编译器能够找到所有必要的头文件。

5. **编译工程**:
   - 编译工程，生成hex文件。
   - 使用ST-Link等工具将hex文件下载到MCU中。

## 注意事项

- 确保安装了对应芯片型号的器件pack，否则MDK5可能无法正确识别芯片型号。
- 在配置全局宏定义时，根据芯片容量选择合适的宏定义。
- 如果只使用部分外设，可以只添加对应外设的库文件，以减少工程大小和编译时间。

## 参考资料

- [STM32F10x_StdPeriph_Lib_V3.5.0](https://www.st.com/content/st_com/en/products/embedded-software/mcu-mpu-embedded-software/stm32-embedded-software/stm32-standard-peripheral-libraries/stsw-stm32054.html)
- [MDK5开发环境](https://www.keil.com/download/product/)

## 贡献

欢迎提交问题和改进建议，帮助完善本模板。

## 许可证

本资源遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[STM32F103C8T6固件库模板分享](https://pan.quark.cn/s/2b3dd86e700c)