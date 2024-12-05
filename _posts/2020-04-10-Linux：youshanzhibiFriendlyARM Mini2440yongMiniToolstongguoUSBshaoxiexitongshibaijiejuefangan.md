---
layout: post
title: "Linux：友善之臂FriendlyARM Mini2440用MiniTools通过USB烧写系统失败解决方案"
date:   2022-05-15
tags: [USB,烧写,MiniTools,之臂,开发板]
comments: true
author: admin
---
# Linux：友善之臂FriendlyARM Mini2440用MiniTools通过USB烧写系统失败解决方案

## 简介
本资源文件旨在为使用友善之臂FriendlyARM Mini2440开发板的用户提供一个解决方案，帮助解决在使用MiniTools通过USB烧写系统时遇到的失败问题。通过本资源，用户可以找到详细的步骤和工具，确保系统能够成功烧写到开发板上。

## 内容概述
1. **问题背景**：
   - 用户在使用MiniTools通过USB烧写系统时遇到连接失败的问题。
   - 经过多次尝试和搜索，问题仍未解决。

2. **解决方案**：
   - 发现开发板的BootLoader输出信息中缺少“SD card … Found Hello USB Loop”等字样。
   - 确认开发板使用的是supervivi而不是superboot，因此不支持MiniTools和SD卡烧写。
   - 推荐使用dnw工具替代友善之臂官方提供的USB下载工具。

3. **工具和步骤**：
   - 下载并安装SuperVivi-Transfer-Tool-Complete工具。
   - 手动安装驱动程序（注意：在某些Windows系统上可能会导致蓝屏问题）。
   - 使用SuperVivi-USB-Transfer-Tool程序进行USB上传。
   - 通过XShell进行串口监听，确保信息清晰明了。

4. **烧写步骤**：
   - 接线：确保串口和USB线连接稳定，并提供稳定的电源。
   - 进入BootLoader：通过开关和复位键进入选择菜单。
   - 擦除Nand Flash并分区。
   - 下载Supervivi / Superboot。
   - 烧写内核和文件系统。

## 注意事项
- 在烧写过程中，确保所有连接稳定，避免因松动导致的失败。
- 使用XShell进行串口监听时，不要同时使用SuperVivi-USB-Transfer-Tool的串口功能，以免卡死。

## 结论
通过本资源文件提供的解决方案和步骤，用户可以成功解决使用MiniTools通过USB烧写系统失败的问题，确保Linux系统能够顺利烧写到友善之臂FriendlyARM Mini2440开发板上。

## 下载链接

[Linux友善之臂FriendlyARMMini2440用MiniTools通过USB烧写系统失败解决方案分享](https://pan.quark.cn/s/bc60490f837d)