---
layout: post
title: "RK3399固件烧录指导"
date:   2023-12-02
tags: [固件,烧录,RK3399,开发板,烧写]
comments: true
author: admin
---
# RK3399固件烧录指导

本仓库提供了一个名为“rk3399固件烧录指导.docx”的资源文件，该文件详细介绍了如何对RK3399开发板进行固件烧录的步骤和注意事项。

## 资源文件描述

该资源文件包含了以下内容：

1. **未烧录过固件的情况**：
   - 上电后，开发板将自动进入MASKROM模式（适用于研1板初始状态）。

2. **已烧录过固件的情况**：
   - 按住recover按键并上电或复位，系统将进入LOADER固件烧写模式。在此模式下，可以烧写包括loader在内的所有固件。
   - 或者通过串口运行命令 `reboot boot loader`，或者使用adb命令 `adb reboot bootloader`，也可以进入LOADER固件烧写模式。

3. **烧录工具的使用**：
   - 运行AndroidTool后，您将看到相应的界面，根据界面提示进行固件烧录操作。

## 注意事项

- 在进行固件烧录前，请确保您已备份重要数据，以防数据丢失。
- 请严格按照文档中的步骤操作，避免因操作不当导致设备损坏。

希望这份指导文档能帮助您顺利完成RK3399开发板的固件烧录工作。

## 下载链接

[RK3399固件烧录指导分享](https://pan.quark.cn/s/75158970f2bd)