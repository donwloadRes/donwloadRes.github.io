---
layout: post
title: "Android反Frida注入检测Demo"
date:   2021-11-09
tags: [Frida,Demo,检测,Android,注入]
comments: true
author: admin
---
# Android反Frida注入检测Demo

本仓库提供了一个Android反Frida注入检测的Demo资源文件。该Demo主要用于检测Frida注入，并包含了端口检测和libc检测的功能。

## 资源文件描述

- **Android反Frida注入检测的demo**：该Demo旨在帮助开发者检测Android设备上是否存在Frida注入。通过端口检测和libc检测，可以有效识别并防止Frida工具的注入。

## 功能介绍

1. **端口检测**：检测设备上是否存在Frida服务器的监听端口，从而判断是否存在Frida注入。
2. **libc检测**：通过检测libc库中的特定函数，判断是否存在Frida注入。

## 使用说明

1. 下载本仓库中的资源文件。
2. 将Demo集成到您的Android项目中。
3. 运行Demo，进行Frida注入检测。

## 注意事项

- 本Demo仅供学习和研究使用，请勿用于非法用途。
- 由于Frida工具的不断更新，本Demo可能需要定期更新以适应新的Frida版本。

## 贡献

欢迎开发者提交Pull Request，共同完善本Demo的功能和检测方法。

## 许可证

本项目采用MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[Android反Frida注入检测Demo](https://pan.quark.cn/s/7b422abe0879)