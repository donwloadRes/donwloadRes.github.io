---
layout: post
title: "IMX6ULL学习笔记（11）——获取和编译官方SDK"
date:   2022-11-20
tags: [SDK,包含,Linux,官方,IMX6ULL]
comments: true
author: admin
---
# IMX6ULL学习笔记（11）——获取和编译官方SDK

本资源文件提供了关于IMX6ULL开发板的官方SDK（Software Development Kit）的获取和编译方法。SDK是NXP针对其官方评估板的软件开发包，包含了固件库和各种程序范例，适用于Windows和Linux两种主机系统。

## 内容概述

### 1. 简介
SDK（Software Development Kit）是NXP针对其官方评估板的软件开发包，可以在NXP的官网下载得到。SDK中包含了固件库和各种程序范例，这个SDK包提供了Windows和Linux两种版本，分别针对主机系统是Windows和Linux。

### 2. 获取SDK
- **官网下载**：i.MX 6ULL单核处理器，配备Arm® Cortex®-A7内核。
- **百度网盘**：提供百度网盘下载链接，提取码为51ub。

### 3. SDK工程结构
安装完成后的SDK包含以下主要目录和文件：
- **boards**：包含NXP官方评估版MCIMX6ULL-EVK的各种示例程序。
- **CMSIS**：包含CMSIS标准相关的文件。
- **CORTEXA**：包含Cortex-A核适配IAR、GCC的头文件。
- **devices**：包含i.MX固件库。
- **docs**：包含部分说明文档，如《Getting Started with MCUXpresso SDK for i.MX 6ULL Derivatives》。
- **middleware**：包含一些中间层软件，如fatfs、lwip、sdmmc、usb等。
- **rtos**：包含FreeRTOS实时操作系统的源代码。
- **tools**：包含开发工具，如cmake_toolchain_files、imgutil、mfgtools等。

### 4. 搭建Linux开发环境
- **安装CMake工具**：执行`sudo apt-get install cmake`。
- **安装交叉编译工具**：执行`sudo apt-get install gcc-arm-none-eabi`。
- **安装Linux版本SDK**：将SDK文件拷贝到Linux下，运行`.run`文件生成SDK。

### 5. 编译SDK
- **打开SDK源码目录**：选择ARM GCC版本工程，运行`build_ddr_release.sh`脚本生成`.bin`文件。
- **常见错误**：确保添加`ARMGCC_DIR`环境变量，执行`export ARMGCC_DIR=/usr`。

通过本资源文件，您可以顺利获取并编译IMX6ULL开发板的官方SDK，为后续的开发工作打下坚实的基础。

## 下载链接

[IMX6ULL学习笔记11获取和编译官方SDK](https://pan.quark.cn/s/7661d87f7ea5)