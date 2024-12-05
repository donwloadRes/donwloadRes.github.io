---
layout: post
title: "新手如何在Arduino上安装ESP32和ESP8266开发板及库文件"
date:   2020-12-15
tags: [开发板,Arduino,文件,IDE,文件夹]
comments: true
author: admin
---
# 新手如何在Arduino上安装ESP32和ESP8266开发板及库文件

本文将详细介绍如何在Arduino IDE中安装ESP32和ESP8266开发板，并配置相应的库文件。无论你是初学者还是有一定经验的开发者，本文都将为你提供清晰的步骤和指导。

## 安装ESP32和ESP8266开发板

### 方法一：通过开发板管理器安装

1. **打开Arduino IDE**：双击打开Arduino IDE。
2. **进入首选项**：点击左上角的“文件” -> “首选项”。
3. **添加开发板管理器网址**：在“附加开发板管理器网址”一栏右边点击白蓝色图标，添加以下两个网址（注意分行）：
   ```
   http://arduino.esp8266.com/stable/package_esp8266com_index.json
   http://arduino.esp32.com/stable/package_esp32com_index.json
   ```
4. **安装开发板**：点击工具栏的“开发板” -> “开发板管理器”，搜索到`esp32`和`esp8266`，分别点击安装。

### 方法二：手动安装

1. **下载资源文件**：下载提供的资源文件包。
2. **解压文件**：将下载的文件解压到Arduino IDE的安装目录下的`arduino15`文件夹中。
3. **确认文件结构**：确保解压后的文件夹中包含“硬件”和“工具”两个子文件夹。
4. **验证安装**：打开Arduino IDE，在“开发板”中应该能看到ESP32和ESP8266的选项，表示安装成功。

## 安装库文件

1. **定位库文件夹**：右击Arduino软件，点开文件所在位置，找到`libraries`文件夹。
2. **替换或插入库文件**：将你拥有的库文件替换或插入到此文件夹中。

## 总结

通过以上步骤，你可以在Arduino IDE中成功安装ESP32和ESP8266开发板，并配置相应的库文件。希望这些步骤能帮助你顺利开始使用这些开发板进行项目开发。

## 下载链接

[新手如何在Arduino上安装ESP32和ESP8266开发板及库文件](https://pan.quark.cn/s/97d7e89bed19)