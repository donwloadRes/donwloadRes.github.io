---
layout: post
title: "基于STM32单片机的MLX90614无接触式红外测温仪额温枪"
date:   2022-05-22
tags: [STM32,单片机,模块,温度,测温]
comments: true
author: admin
---
# 基于STM32单片机的MLX90614无接触式红外测温仪额温枪

## 项目简介

本项目基于STM32单片机，采用MLX90614模块进行无接触式红外测温，结合OLED显示屏显示测温数据，并通过蓝牙HC-05模块将温度数据上传至手机APP。项目还包括按键设置温度上限值功能，当温度异常时，蜂鸣器会进行报警。本资源文件提供了完整的源程序、原理图和元件清单，适合用于制作真实的额温枪无接触式测温装置。

## 功能特点

1. **主控芯片**：采用STM32单片机作为主控芯片。
2. **测温模块**：使用MLX90614模块进行无接触式红外测温。
3. **显示功能**：采用OLED显示屏显示测温数据。
4. **数据传输**：通过蓝牙HC-05模块将温度数据上传至手机APP。
5. **温度设置**：可以通过按键设置温度上限值。
6. **报警功能**：当温度异常时，蜂鸣器进行报警。

## 文件内容

- **源程序**：包含完整的STM32单片机源代码，代码中有详细的中文注释，方便新手理解和学习。
- **原理图**：提供了详细的电路原理图，方便硬件设计和调试。
- **元件清单**：列出了项目所需的所有元器件清单，方便采购和制作。

## 使用说明

1. **硬件连接**：根据原理图连接各个元器件。
2. **程序烧录**：将源程序烧录到STM32单片机中。
3. **功能测试**：通过按键设置温度上限值，观察OLED显示屏上的温度数据，并通过蓝牙模块查看手机APP上的数据。
4. **报警测试**：当温度超过设定值时，蜂鸣器应发出报警声。

## 注意事项

- 请确保所有元器件连接正确，避免短路或连接错误。
- 在烧录程序前，请确认STM32单片机的型号与程序兼容。
- 使用蓝牙模块时，请确保手机APP与模块配对成功。

## 贡献与反馈

如果您在使用过程中遇到任何问题或有改进建议，欢迎提交Issue或Pull Request。我们非常欢迎您的贡献和反馈！

## 许可证

本项目遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[基于STM32单片机的MLX90614无接触式红外测温仪额温枪](https://pan.quark.cn/s/ef3e268df39c)