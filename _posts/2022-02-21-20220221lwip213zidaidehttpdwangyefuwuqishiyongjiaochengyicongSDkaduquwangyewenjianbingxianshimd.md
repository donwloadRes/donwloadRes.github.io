---
layout: post
title: "lwip213自带的httpd网页服务器使用教程一从SD卡读取网页文件并显示"
date:   2020-10-03
tags: [网页文件,教程,SD,lwip,自带]
comments: true
author: admin
---
# lwip-2.1.3自带的httpd网页服务器使用教程（一）从SD卡读取网页文件并显示

## 概述
本教程详细介绍了如何在STM32F103ZE单片机上使用lwip-2.1.3自带的httpd网页服务器，并通过SD卡读取网页文件并显示。教程内容包括从SD卡动态加载网页文件的实现方法，以及如何使用makefsdata工具将网页文件打包成C语言数组。

## 主要内容

### 1. 开发环境
- **单片机**: STM32F103ZE
- **有线网口芯片**: ENC28J60
- **网页设计软件**: Adobe Dreamweaver CS3

### 2. 网页文件存储
由于STM32单片机的Flash容量有限，本教程介绍了如何通过外接SD卡来存储网页文件。SD卡可以使用FAT、FAT32或exFAT文件系统，以文件的形式存储网页文件，并通过FatFS读取存储器中的文件。

### 3. 动态加载网页文件
本教程详细讲解了如何在lwipopts.h中配置相关宏，并实现两个关键接口函数`fs_open_custom`和`fs_close_custom`，以便从SD卡动态加载网页文件并显示。

### 4. makefsdata工具的使用
lwip自带的makefsdata工具可以将网页文件打包成C语言数组，本教程提供了在Windows系统上编译makefsdata工具的方法，并介绍了如何使用该工具生成fsdata.c文件。

### 5. 示例程序
教程提供了完整的示例程序和PCB文件的下载地址，用户可以根据教程内容自行打印PCB板并焊好器件，然后直接运行示例程序。

## 总结
通过本教程，用户可以掌握在STM32单片机上使用lwip-2.1.3自带的httpd网页服务器，并通过SD卡动态加载网页文件的方法。教程内容详细，适合有一定嵌入式开发基础的用户学习。

## 下载链接

[lwip-2.1.3自带的httpd网页服务器使用教程一从SD卡读取网页文件并显示](https://pan.quark.cn/s/a8bcd4582c92)