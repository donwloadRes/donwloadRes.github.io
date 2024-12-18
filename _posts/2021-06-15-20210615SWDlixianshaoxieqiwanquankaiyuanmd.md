---
layout: post
title: "SWD离线烧写器完全开源"
date:   2022-08-08
tags: [离线,烧写,DAP,串口,写器]
comments: true
author: admin
---
# SWD离线烧写器（完全开源）

## 项目介绍

本项目使用STM32F103RET6作为主控，基于ST官方CMSIS-DAP项目进行修改，实现STM32F103系列可脱机、可去读保护烧写。因项目暂时只有103系列脱机烧写需求，所以暂时只添加了103的烧写算法。

## 项目功能

1. 使用8M FLASH，可使用虚拟U盘向FLASH放置HEX文件或BIN文件进行烧写（BIN较快）。
2. 可去除目标板的读保护，直接烧写（烧写后可能需要手动重启）。
3. 支持手动切换模式，使离线烧写器支持DAP仿真。
4. 安装驱动后可支持虚拟USB转TTL。
5. 可离线使用串口调试功能（仅支持英文及常用数字符号）。

## 使用教程

1. 长按SELECT键开机可进入DAP仿真模式，屏幕上显示DAP-CONNECT。
2. 直接插入电脑USB端口可向离线烧写器放入相关烧写文件，并可使用虚拟串口功能。
3. 连接目标板开机，选择文件后选择FLASH后即可进行烧写。
4. 选择“>>”，进入DEBUG MODE后选择ENTER即可进行离线串口调试。

## 项目框架及实现

项目框架主要为4个部分：CMSIS-DAP模块、虚拟U盘、串口模块、离线调试模块和离线烧写器部分。当初始化识别到选择按钮按下时进行CMSIS-DAP模块的初始化，并进行CMSIS-DAP进程。

## 后续项目优化

项目目前主要有两个比较大的不足需要优化：
1. HEX文件转换的时间较长，大约在5-10秒左右，可能造成用户体验不佳，后续考虑想办法在读取的同时进行转换并进行烧写，并每次烧录定长数据段，以达到快速烧写的方法。
2. 离线烧写只添加了F103系列的烧写算法，因为手头上开发板没有那么多，无法测试其他MCU是否能够成功，如果有需要的话会添加其他如F407系列MCU的离线烧写算法，并添加切换功能。

## 相关演示

- DAP仿真功能
- 虚拟串口及U盘模拟
- 离线文件烧写
- 离线串口调试功能

## 项目意见

如果项目有问题或者有新功能需求，欢迎向作者提交意见。

## 下载链接

[SWD离线烧写器完全开源](https://pan.quark.cn/s/e7b0deecc9c7)