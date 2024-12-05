---
layout: post
title: "Arduino ESP32开发环境搭建入门教程"
date:   2020-01-05
tags: [ESP32,Arduino,文件夹,esp32,开发板]
comments: true
author: admin
---
# Arduino ESP32开发环境搭建入门教程

本文详细介绍了如何在本地和在线两种方式下搭建Arduino ESP32的开发环境。无论你是初学者还是有经验的开发者，通过本文的指导，你都能顺利完成ESP32开发环境的搭建。

## 方法一：本地安装

### 1. 安装 Arduino IDE
从官网下载 Arduino IDE 软件并安装。

### 2. 下载 arduino-esp32 库
从网盘获取并安装 arduino-esp32 库。

### 3. 安装arduino-esp32 库
1. 找到Arduino IDE安装目录，打开hardware文件夹。
2. 在hardware文件夹中创建一个espressif文件夹。
3. 将解压出的文件夹移动到espressif文件夹中，并重命名为esp32。
4. 打开esp32文件夹，打开tool文件夹，找到get.exe并双击运行，等待其运行结束。
5. 运行Arduino IDE，即可在工具>开发板>ESP32 Arduino选项栏中看到ESP32-S3板型。

### 4. 验证环境搭建
1. 串口按照自己实际的串口选择，其余可以按照图示参考。
2. 选择获取ID的示例程序。
3. 编译后打开串口监视器，能答应设备ID则说明环境搭建成功。

## 方法二：在线安装

### 1. 添加开发板管理地址
在Arduino IDE中，选择文件>首选项，在附加开发板管理器网址中添加以下网址：
https://github.com/espressif/arduino-esp32/releases/download/1.0.4/package_esp32_index.json

### 2. 添加开发板
在工具>开发板>开发板管理器中搜索ESP32，点击安装。

### 3. 等待安装完成
安装完成后，选择ESP32开发板，即可开始使用。

通过以上两种方法，你可以轻松搭建Arduino ESP32的开发环境，开始你的ESP32开发之旅。

## 下载链接

[ArduinoESP32开发环境搭建入门教程](https://pan.quark.cn/s/4c2d1120becd)