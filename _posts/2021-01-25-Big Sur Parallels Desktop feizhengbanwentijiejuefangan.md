---
layout: post
title: "Big Sur Parallels Desktop 非正版问题解决方案"
date:   2021-09-28
tags: [Parallels,Desktop,解决方案,虚拟机,文件]
comments: true
author: admin
---
# Big Sur Parallels Desktop 非正版问题解决方案

本资源文件提供了一个解决方案，用于解决在 macOS Big Sur 系统中使用 Parallels Desktop 时遇到的“This copy of Parallels Desktop may not be genuine”错误提示。该解决方案详细描述了如何通过替换特定文件来解决此问题，确保您的 Parallels Desktop 虚拟机能够正常运行。

## 解决方案概述

1. **错误信息**：在使用 Parallels Desktop 时，可能会弹出“This copy of Parallels Desktop may not be genuine”的错误提示。

2. **解决方案步骤**：
   - 打开 Parallels Desktop 虚拟机中的 Windows 系统。
   - 找到需要修改的文件：`C:\Program Files (x86)\Parallels\Parallels Tools\Plugins\DesktopUtilities.dll`。
   - 将新文件拖动到该文件夹下完成替换。
   - 如果遇到文件被占用的情况，可以通过资源监视器来杀掉相关进程。

3. **文件替换完成**：替换完成后，重启 Parallels Desktop 虚拟机，错误提示将不再出现。

## 注意事项

- 建议在替换文件前，自行保留原文件以备不时之需。
- 该解决方案适用于特定版本的 Parallels Desktop，请确保您的版本与此解决方案兼容。

通过以上步骤，您可以有效解决 Big Sur 系统中 Parallels Desktop 的非正版问题，确保虚拟机的正常运行。

## 下载链接

[BigSurParallelsDesktop非正版问题解决方案](https://pan.quark.cn/s/cbed243e9a28)