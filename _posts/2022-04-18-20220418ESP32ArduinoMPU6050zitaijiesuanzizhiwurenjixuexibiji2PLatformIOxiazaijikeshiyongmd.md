---
layout: post
title: "【ESP32Arduino+MPU6050姿态解算】自制无人机学习笔记2 PLatformIO 下载即可使用"
date:   2023-04-12
tags: [ESP32,无人机,MPU6050,解算,姿态]
comments: true
author: admin
---
# 【ESP32Arduino+MPU6050姿态解算】自制无人机学习笔记2 PLatformIO 下载即可使用

## 简介

本资源文件提供了一个基于ESP32和MPU6050的姿态解算项目，适用于自制无人机的开发。该项目使用PlatformIO进行开发，下载后即可使用。通过本项目，您可以学习如何使用ESP32和MPU6050实现无人机的姿态解算，并进行稳定性控制。

## 项目特点

- **ESP32**：国产之光，双核算力强大，自带互联网模块，适合作为无人机的开发平台。
- **MPU6050**：价格低廉，体积小，功能强大，可靠性高，可与ESP32通讯辅助无人机调整姿态。
- **姿态解算**：通过ESP32和MPU6050的结合，实现无人机的自稳定功能。
- **PlatformIO**：使用PlatformIO进行开发，方便快捷，适合初学者和进阶开发者。

## 使用方法

1. **下载资源文件**：下载后用VScode打开文件夹，能看到src里面有这几个文件。
2. **主程序**：其中`start.cpp`是主程序，点击上传到ESP32。
3. **硬件连接**：按照以下引脚接法连接ESP32与MPU6050：
   - 3.3v -> VCC
   - GND -> GND
   - GPIO22 -> SCL
   - GPIO21 -> SDA
4. **串口监视器**：将ESP32连接电脑，打开串口监视器即可看到ESP32正在输出陀螺仪的姿态数据。注意波特率是115200。

## 详细介绍

代码源自Arduino IDE中的MPU6050实例，经过整理并调整为适用于ESP32的模式供大家使用。输出的数据包括Pitch（俯仰角）、Roll（横滚角）、Yaw（偏航角）。如果想在串口监视器中看到其它数据，可在可视化部分中找到要显示的数据的相关函数进行调用。

## 注意事项

- 本项目已经过无人机稳定性控制的测试，可控制四轴无人机进行稳定性控制，故可保证其可靠性。
- 在使用过程中，请确保硬件连接正确，避免因连接错误导致的设备损坏。

## 致谢

感谢colour64提供的原始文章和代码，本项目在此基础上进行了整理和优化，方便大家学习和使用。

## 联系我们

如有任何问题或建议，欢迎通过CSDN博客或GitHub联系我们。

---

希望本项目能帮助到您，祝您在无人机开发的道路上取得成功！

## 下载链接

[ESP32ArduinoMPU6050姿态解算自制无人机学习笔记2PLatformIO下载即可使用](https://pan.quark.cn/s/f08352c5be2e)