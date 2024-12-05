---
layout: post
title: "开启EPT的VT源码  支持Win10 x64"
date:   2022-10-28
tags: [源码,EPT,x64,VT,SSDT]
comments: true
author: admin
---
# 开启EPT的VT源码 - 支持Win10 x64

## 资源描述

本仓库提供了一个开启了EPT（Extended Page Table）并实现了SSDT（System Service Descriptor Table）无痕HOOK的VT（Virtualization Technology）框架源码。该源码不会触发PG（PatchGuard），并且可以在Windows 10 x64位操作系统下正常运行。

## 功能特点

- **EPT开启**：源码中已成功开启EPT，提供了更强大的内存管理功能。
- **SSDT无痕HOOK**：实现了SSDT的无痕HOOK，能够在不触发PG的情况下进行系统服务表的修改。
- **兼容性**：源码经过测试，可以在Windows 10 x64位系统下稳定运行。

## 使用说明

1. **环境准备**：确保你的开发环境支持Windows 10 x64位系统的驱动开发。
2. **源码下载**：从本仓库下载源码文件。
3. **编译与运行**：按照常规的驱动开发流程进行编译和加载，确保系统环境配置正确。
4. **测试与验证**：在Windows 10 x64位系统下进行测试，验证EPT开启和SSDT无痕HOOK的功能是否正常。

## 注意事项

- 请确保在合法和授权的环境下使用本源码，遵守相关法律法规。
- 由于涉及到系统底层操作，建议在虚拟机或测试环境中进行操作，避免对生产环境造成影响。

## 贡献与反馈

如果你在使用过程中遇到任何问题或有改进建议，欢迎提交Issue或Pull Request。我们期待与你的交流与合作。

---

希望本资源能够帮助你在VT开发中取得进展，祝你开发顺利！

## 下载链接

[开启EPT的VT源码-支持Win10x64](https://pan.quark.cn/s/f18d86a02b3c)