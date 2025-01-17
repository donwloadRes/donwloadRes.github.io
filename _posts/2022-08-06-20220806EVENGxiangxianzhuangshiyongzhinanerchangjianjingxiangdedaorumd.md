---
layout: post
title: "EVENG详细安装使用指南二 常见镜像的导入"
date:   2021-12-22
tags: [镜像,EVE,NG,导入,opt]
comments: true
author: admin
---
# EVE-NG详细安装使用指南（二）—— 常见镜像的导入

欢迎来到EVE-NG详细安装使用系列教程的第二部分。本指南专注于帮助您掌握在EVE-NG平台中导入各种镜像文件的技巧，特别强调QEMU镜像的处理方法。无论是希望扩展您的网络模拟环境，还是想深入了解如何使用华为、思科等厂商设备的镜像，这篇文档都将为您提供清晰的步骤和注意事项。

## 支持的镜像类型

EVE-NG平台广泛支持三种主要类型的镜像：

1. **Dynamips**：主要用于模拟Cisco IOS设备。
2. **IOL/IOU**：适用于更高级的Cisco设备镜像。
3. **QEMU镜像**：最为通用，支持众多厂商设备，包括华为、H3C、Cisco等。

## 华为镜像导入教程

### 1. 准备阶段

- **下载镜像**: 从可靠的源，如EVE-NG中文网或百度网盘获取镜像文件。
- **了解存放路径**: 明确各类镜像的默认存储位置，比如QEMU镜像位于`/opt/unetlab/addons/qemu`。

### 2. 导入步骤

- **创建目录与命名**: 按照规范，在`/opt/unetlab/addons/qemu/`下创建文件夹，结构如`设备名称-版本号`。
- **上传镜像**: 使用FTP工具（如WinSCP）导入下载的`.qcow2`或`.img`格式镜像至对应目录。
- **图标与模板**: 将设备图标置于`/opt/unetlab/html/images/icons`，模板文件放入正确CPU架构的`/opt/unetlab/html/templates`目录。

### 3. 设置权限

- **修正权限**: 导入后，通过命令行执行`/opt/unetlab/wrappers/unl_wrapper -a fixpermissions`以修正文件权限。

### 4. 测试与使用

- 在EVE-NG平台中新建实验，检验导入的镜像是否可用。启动设备，使用默认用户名和密码登录验证。

## 注意事项

- **启动问题**: 若遇到设备无法正常启动，尝试调整CPU核心数和内存配置。
- **文档完整性**: 上述步骤基于概述，完整细节请参照原始文章。

通过以上步骤，您应该能顺利地在EVE-NG环境中导入并使用华为及其他厂商的设备镜像，进一步提升您的网络实验和学习体验。记得每一步操作都要细心，并确认环境的兼容性，祝您模拟实验之旅顺畅！

---

本指南旨在辅助用户高效、准确地完成镜像导入流程，实践前建议详细阅读原始文章以获取最新的指导信息。

## 下载链接

[EVE-NG详细安装使用指南二常见镜像的导入](https://pan.quark.cn/s/d9d3a3ed286d)