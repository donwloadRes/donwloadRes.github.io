---
layout: post
title: "使用USB转TTL下载器将固件烧写到STM32F103C8T6最小系统板中"
date:   2022-11-01
tags: [USB,TTL,STM32F103C8T6,下载,烧录]
comments: true
author: admin
---
# 使用USB转TTL下载器将固件烧写到STM32F103C8T6最小系统板中

## 简介

本资源文件详细介绍了如何使用USB转TTL下载器将固件烧写到STM32F103C8T6最小系统板中。通过本教程，您将学习到如何设置Keil5生成HEX文件、下载并安装CH340驱动、使用mcuisp或Flymcu工具进行程序烧录，以及如何正确连接USB转TTL下载器和开发板。

## 主要步骤

### 1. 设置Keil5生成HEX文件

在Keil5中，确保勾选“Create HEX File”选项，以便在编译时生成HEX文件。

### 2. 下载并安装CH340驱动

下载并安装CH340驱动程序，以确保USB转TTL下载器能够正常工作。

### 3. 下载并安装mcuisp或Flymcu

选择并下载mcuisp或Flymcu工具，用于烧录程序到STM32F103C8T6最小系统板。

### 4. 连接USB转TTL下载器和开发板

按照指定的方式连接USB转TTL下载器和STM32F103C8T6最小系统板，并设置跳线帽。

### 5. 烧录程序

使用mcuisp或Flymcu工具，选择正确的串口和HEX文件，配置其他选项并开始烧录程序。如果遇到连接问题，可以尝试按下开发板上的Reset键或重新上电。

## 注意事项

- 确保所有连接正确无误。
- 在烧录过程中，如果出现连接超时等问题，可以尝试重新连接或按下Reset键。
- 烧录完成后，恢复开发板上的跳线帽设置，并重新上电或按下Reset键，程序即可正常执行。

通过本教程，您将能够顺利地将固件烧写到STM32F103C8T6最小系统板中，并开始您的嵌入式开发工作。

## 下载链接

[使用USB转TTL下载器将固件烧写到STM32F103C8T6最小系统板中](https://pan.quark.cn/s/c0971bc844c9)