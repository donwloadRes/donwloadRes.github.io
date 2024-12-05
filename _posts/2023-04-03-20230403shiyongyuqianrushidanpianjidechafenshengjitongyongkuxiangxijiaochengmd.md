---
layout: post
title: "适用于嵌入式单片机的差分升级通用库+详细教程"
date:   2021-03-09
tags: [差分,升级,算法,版本,嵌入式]
comments: true
author: admin
---
# 适用于嵌入式单片机的差分升级通用库+详细教程

## 简介
本资源文件提供了一个适用于嵌入式单片机的差分升级通用库，并附带详细的教程。差分升级（又称为增量升级）是一种通过差分算法将源版本与目标版本之间的差异部分提取出来，制作成差分包，然后在设备上通过还原算法将差异部分在源版本上进行还原，从而升级成目标版本的过程。

## 特点
- **节省资源空间**：差分升级方案可以节省MCU内部的资源空间。
- **降低功耗**：在下载和升级过程中，差分升级可以显著降低功耗。
- **减少下载量**：差分升级可以极大减少下载量，特别是对于嵌入式STM32等单片机来说，可以减少维护成本。

## 实现原理
差分升级过程包括以下几个步骤：
1. 使用旧版本bin文件和新版本bin文件制作差分包。
2. 将差分包下载到设备内。
3. 设备使用差分算法还原出新版本bin。
4. 设备将新版本bin进行CRC验证后刷到代码执行区。
5. 设备重启并以新版本运行。

## 关键点
1. **差分包制作过程**：使用稳定的开源差分算法bsdiff+lzma生成差分包。
2. **嵌入式设备中差分算法库的移植**：使用开源差分算法bsdiff+lzma来还原新版本文件，代码全开源，并已抽象出极简的接口，移植简单。

## 使用方法
1. **差分包制作**：使用上位机软件制作差分包，上位机软件已开源，可自行修改。
2. **差分算法库的移植**：将差分算法库移植到嵌入式设备中，提供详细的移植教程和代码示例。

## 适用范围
本库适用于市场上所有的单片机，如STM32、瑞萨、华大、复旦微等，但要求RAM至少要10k以上，库本身的消耗大概是5k的ROM。

## 贡献
欢迎开发者贡献代码和提出改进建议，共同完善本差分升级通用库。

## 许可证
本项目遵循CC 4.0 BY-SA版权协议，转载请附上原文出处声明。

## 下载链接

[适用于嵌入式单片机的差分升级通用库详细教程](https://pan.quark.cn/s/07f3819ba17d)