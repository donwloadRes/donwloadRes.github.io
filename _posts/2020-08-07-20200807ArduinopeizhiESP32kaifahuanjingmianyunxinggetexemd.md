---
layout: post
title: "Arduino配置ESP32开发环境免运行getexe"
date:   2022-06-07
tags: [ESP32,Arduino,开发板,IDE,安装]
comments: true
author: admin
---
# Arduino配置ESP32开发环境（免运行get.exe）

## 简介

本资源文件旨在帮助用户在Arduino IDE中配置ESP32开发环境，无需运行`get.exe`文件。通过本指南，您可以轻松地将ESP32开发板与Arduino IDE集成，从而开始您的ESP32项目开发。

## 步骤

### 1. 安装Arduino IDE

首先，从Arduino官网下载并安装Arduino IDE。安装过程较为简单，按照提示完成即可。

### 2. 下载ESP32配置文件

1. 打开Arduino IDE，点击“文件” -> “首选项”。
2. 在“附加开发板管理器网址”中填入以下链接：
   ```
   https://dl.espressif.com/dl/package_esp32_index.json
   ```
3. 点击“确定”保存设置。

### 3. 安装ESP32开发板

1. 点击“工具” -> “开发板” -> “开发板管理器”。
2. 在搜索框中输入“esp32”，然后选择最新版本进行安装。
3. 安装过程可能需要一些时间，请耐心等待。

### 4. 配置ESP32开发环境

1. 下载ESP32的配置工具，并解压到Arduino的安装目录下的`hardware`文件夹中。
2. 在`hardware`文件夹中创建`espressif`文件夹，并在其中再创建`esp32`文件夹。
3. 将解压后的文件复制到`esp32`文件夹中。

### 5. 运行ESP32

1. 在Arduino IDE中选择相应的ESP32开发板。
2. 选择一个示例程序，例如点亮LED灯的示例。
3. 上传程序到ESP32开发板，观察运行结果。

## 注意事项

- 在安装ESP32开发板时，文件下载可能较慢，建议使用稳定的网络环境。
- 如果遇到安装失败的情况，可以尝试多次安装或使用其他网络环境。

通过以上步骤，您应该能够成功配置ESP32开发环境，并开始您的ESP32项目开发。祝您开发顺利！

## 下载链接

[Arduino配置ESP32开发环境免运行get.exe分享](https://pan.quark.cn/s/f0fed8029d03)