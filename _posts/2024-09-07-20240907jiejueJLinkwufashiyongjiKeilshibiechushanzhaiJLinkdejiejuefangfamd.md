---
layout: post
title: "解决JLink无法使用及Keil识别出山寨JLink的解决方法"
date:   2022-10-22
tags: [Link,Keil,固件,刷写,解决]
comments: true
author: admin
---
# 解决J-Link无法使用及Keil识别出山寨J-Link的解决方法

## 简介
本资源文件旨在帮助用户解决在使用J-Link调试器时遇到的问题，特别是当J-Link无法正常工作或被Keil识别为山寨版时。通过本资源文件，用户可以学习如何重新刷写J-Link固件，以及如何绕过Keil对山寨J-Link的检测。

## 适用场景
- J-Link指示灯停止闪烁，无法正常工作。
- Keil提示J-Link固件需要更新，更新后识别出J-Link为山寨版。
- J-Link固件损坏，需要重新刷写。

## 解决方法
### 1. 重新刷写J-Link固件
- **问题描述**：J-Link指示灯停止闪烁，可能是固件损坏。
- **解决步骤**：
  1. 使用SAM-BA工具重新刷写J-Link固件。
  2. 确保使用Windows XP或Windows 7 32位操作系统，因为这些系统有对应的上位机串口驱动程序。

### 2. 绕过Keil对山寨J-Link的检测
- **问题描述**：Keil提示J-Link固件需要更新，更新后识别出J-Link为山寨版。
- **解决步骤**：
  1. 下载并安装老版本的J-Link驱动程序（如v4.40版本）。
  2. 使用J-Link ARM程序输入`exec invalidatefw`命令，将固件版本还原到以前的版本。
  3. 替换Keil安装目录下ARM/Segger文件夹中的相关文件。

### 3. 解决Keil中Flash Download窗口缺少芯片类型的问题
- **问题描述**：在Keil的Flash Download窗口中没有所需芯片的Flash类型。
- **解决步骤**：
  1. 找到比所需芯片晚出现但低于4.6版本的J-Link驱动。
  2. 重复上述步骤，重新刷写J-Link固件。

## 注意事项
- 在刷写固件过程中，请确保操作正确，避免进一步损坏J-Link。
- 使用老版本驱动时，请注意兼容性问题。

## 结语
通过本资源文件提供的解决方法，用户可以有效解决J-Link无法使用及Keil识别出山寨J-Link的问题。希望这些方法能帮助您顺利进行开发和调试工作。

## 下载链接

[解决J-Link无法使用及Keil识别出山寨J-Link的解决方法分享](https://pan.quark.cn/s/4d3984b5420b)