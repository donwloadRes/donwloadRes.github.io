---
layout: post
title: "ESP826601实战一带OLED显示屏电子时钟"
date:   2024-01-15
tags: [OLED,ESP8266,01,显示屏,模块]
comments: true
author: admin
---
# ESP8266-01实战一——带OLED显示屏电子时钟

## 项目简介
本项目基于ESP8266-01模块，结合OLED显示屏，实现了一个简单的电子时钟功能。通过Arduino IDE进行编程，ESP8266模块能够连接到WiFi网络，并从网络获取当前时间，显示在OLED屏幕上。

## 硬件准备
- ESP8266模块 (esp8266-01)
- 微型锂电池 (3.7V)
- OLED显示屏 (四线IIC)
- 电木板
- 杜邦线若干
- 自锁开关

## 接线说明
ESP8266模块与OLED显示屏的接线如下：
- ESP8266模块 (esp8266-01)
  - VCC -> OLED 3V3
  - GND -> OLED GND
  - IO0 -> OLED SCL
  - IO2 -> OLED SDA

## 软件准备
本项目使用Arduino IDE进行开发。需要安装以下库文件：
- ESP8266WiFi
- U8g2lib

## 项目总结
通过本项目，您可以学习到如何使用ESP8266模块连接WiFi网络，并通过HTTP请求获取网络时间，最终在OLED显示屏上显示。项目代码完全开源，适合初学者学习和实践。

## 下载链接

[ESP8266-01实战一带OLED显示屏电子时钟](https://pan.quark.cn/s/e46722fa48f4)