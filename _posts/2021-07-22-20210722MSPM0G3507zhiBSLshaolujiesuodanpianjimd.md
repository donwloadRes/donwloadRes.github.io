---
layout: post
title: "MSPM0G3507之BSL烧录解锁单片机"
date:   2021-07-25
tags: [烧录,单片机,BSL,解锁,MSPM0G3507]
comments: true
author: admin
---
# MSPM0G3507之BSL烧录（解锁单片机）

本资源文件提供了关于如何使用BSL（Bootloader Service Layer）烧录工具解锁MSPM0G3507单片机的详细指南。该指南适用于在多次正常烧录后遇到烧录错误的情况，通过BSL烧录可以解锁单片机，使其恢复正常烧录功能。

## 内容概述

1. **前言**
   - 介绍在多次正常烧录后遇到烧录错误的情况，建议使用BSL烧录进行解锁。
   - 说明该方法仅针对单片机解锁，不涉及程序烧录。

2. **相关配置**
   - 主控芯片：MSPM0G3507SPTR（48角）
   - 开发环境：Keil 版本5.33
   - 所需硬件：USB转TTL模块（部分板子自带CH340，连接USB即可）
   - 驱动安装：CH340驱动（已安装Keil的用户通常已具备）

3. **接线步骤**
   - 将板子上的PA18引脚与3V3进行连接（注意不要接错到5V）。
   - 使用USB转TTL模块与MSPM0G3507进行连接，注意3V3的供电方式。

4. **软件配置**
   - 使用BSL烧录工具进行配置，确保软件路径正确。

5. **下载步骤**
   - 确保PA18接3V3后连接电脑。
   - 板子上电后，在10秒内按下复位按键并松开。
   - 点击“Download”控件进行下载，显示“Download finished”即成功。

6. **总结**
   - 通过BSL烧录解锁后，单片机可以再次使用DAP-Link进行烧录。
   - 建议检查代码是否存在问题，确保每次烧录都能正常进行。

## 注意事项

- 确保接线正确，避免因接线错误导致烧录失败。
- 在操作过程中，严格按照步骤进行，避免因操作不当导致单片机损坏。
- 如果代码存在问题，建议找到一份可以正常烧录和运行的代码进行参考。

通过本指南，您可以有效地解决MSPM0G3507单片机在多次烧录后遇到的锁定问题，恢复其正常烧录功能。

## 下载链接

[MSPM0G3507之BSL烧录解锁单片机](https://pan.quark.cn/s/a62d7fe2458e)