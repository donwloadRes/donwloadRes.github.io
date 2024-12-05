---
layout: post
title: "adb_root: Magisk模块，实现ADB Root功能"
date:   2022-09-13
tags: [adb,root,模块,Android,Magisk]
comments: true
author: admin
---
# adb_root: Magisk模块，实现ADB Root功能

## 模块简介

adb_root是一款专为Magisk设计的模块，旨在为Android设备上的ADB（Android Debug Bridge）用户提供特殊权限。通过这个模块，您能够在设备上以root权限运行adb守护进程（adbd）。不同于传统的root访问（通过superuser，即su），adb_root使开发者或高级用户能直接通过adb命令临时获取系统的深层访问能力，例如推送或拉取系统目录下的文件、重新挂载系统分区等。请注意，这一功能携带较高的安全风险，适用于有经验的用户进行特定调试任务，并建议在完成操作后立即禁用。

## 功能特性

- **ADB Root权限**: 允许adb命令以root权限执行。
- **自定义adbd二进制**: 使用了特别打补丁的adbd，该补丁去除了属性检查和USB认证，确保在某些厂商特定配置下仍能启用adb root。
- **安全性警告**: 高度强调该模块的安全风险，不适合日常使用，且仅应在必要时刻启用。
- **适用平台**: 本模块限制在Aarch64架构的设备上使用，适合多数现代Android设备。

## 补丁详情

该模块基于AOSP（Android Open Source Project）源代码中的adb daemon组件进行修改，具体补丁涉及对`adb/daemon/main.cpp`文件的调整，旨在绕过原本的安全限制，实现adb root的功能性突破。

### 注意事项

- **慎用**: 不熟悉adb或不具备相应技术背景的用户应避免使用，以免引起系统不稳定或其他潜在问题。
- **安全性考量**: 经常使用adb root会增加安全漏洞的风险，使用完毕务必禁用该模块。
- **兼容性**: 确认您的设备为Aarch64架构以保证模块正常工作。

安装此Magisk模块前，请确保您已了解其用途及可能带来的风险，合理利用以提升开发或调试效率，同时保障设备的安全。

## 下载链接

[adb_rootMagisk模块实现ADBRoot功能](https://pan.quark.cn/s/3cc2187cf773)