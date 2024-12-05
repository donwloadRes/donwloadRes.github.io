---
layout: post
title: "SquareLine Studio 创建页面仅显示桌面选项的解决方案"
date:   2024-10-10
tags: [SquareLine,Studio,选项,页面,VPN]
comments: true
author: admin
---
# SquareLine Studio 创建页面仅显示桌面选项的解决方案

## 简介

SquareLine Studio 是一款针对 LVGL（Light and Versatile Graphics Library）的强大图形化设计平台，能够大大缩减 UI 设计的时间。然而，许多用户在安装 SquareLine Studio 后，发现创建页面中只有桌面（desktop）选项，这对于使用 Arduino、ESP32 或 MicroPython 开发的用户来说是不够的。本文将介绍如何解决这个问题。

## 问题描述

在安装 SquareLine Studio 后，用户打开软件时发现创建页面中只有桌面选项，无法选择其他开发板或平台。

## 解决方法

### 方法一：网络连接问题

1. **问题原因**：第一次打开软件时，由于网络连接问题，软件未能连接到 GitHub，导致组件选项缺失。
2. **解决步骤**：
   - 开启 VPN 后，重新打开 SquareLine Studio。
   - 组件选项将会恢复正常显示。

### 方法二：离线解决方案

1. **问题原因**：没有 VPN 的用户无法通过网络连接解决问题。
2. **解决步骤**：
   - 下载 Arduino.zip 文件并解压。
   - 将解压后的文件放置在 `C:\Users\username\Documents\SquareLine\boards` 路径下。
   - 重新打开 SquareLine Studio，组件选项将会恢复正常显示。

## 注意事项

- 确保网络连接正常，或者使用 VPN 解决网络问题。
- 对于没有 VPN 的用户，可以使用离线解决方案，手动添加组件文件。

## 结语

通过以上方法，您可以解决 SquareLine Studio 创建页面中只有桌面选项的问题，从而顺利进行 UI 设计。希望本文对您有所帮助！

## 下载链接

[SquareLineStudio创建页面仅显示桌面选项的解决方案](https://pan.quark.cn/s/75e549768d8c)