---
layout: post
title: "QT HIDAPI USB 示例项目"
date:   2024-09-02
tags: [文件,DLL,示例,项目,QT]
comments: true
author: admin
---
# QT HIDAPI USB 示例项目

## 项目描述

本仓库提供了一个使用QT编写的HIDAPI示例项目，名为“qt-win-usb-hidapi的demo”。该项目包含了在Windows平台上使用HIDAPI进行USB设备通信的示例代码。资源文件中包含了适用于32位和64位Windows系统的DLL和LIB文件，方便用户在不同架构的系统上进行开发和测试。

## 使用说明

1. **环境准备**：
   - 确保你已经安装了QT开发环境。
   - 本项目适用于Windows操作系统，支持32位和64位系统。

2. **构建项目**：
   - 下载本仓库的资源文件。
   - 打开QT Creator，导入项目文件。
   - 在构建项目时，请确保将相应的DLL文件拷贝到编译生成的EXE文件所在的目录中。

3. **调试注意事项**：
   - 在调试过程中，可能需要根据实际连接的USB设备的VID（Vendor ID）和PID（Product ID）进行修改。请确保在代码中正确配置这些参数。

## 文件结构

- `src/`：包含示例项目的源代码。
- `lib/`：包含32位和64位系统所需的LIB文件。
- `dll/`：包含32位和64位系统所需的DLL文件。

## 常见问题

- **DLL文件缺失**：如果在运行时提示缺少DLL文件，请确保在编译后将相应的DLL文件拷贝到EXE文件所在的目录。
- **VID和PID不匹配**：如果设备无法识别，请检查代码中的VID和PID是否与实际设备的值一致。

## 贡献

欢迎提交问题和改进建议。如果你有更好的实现方式或发现了bug，请提交Issue或Pull Request。

## 许可证

本项目采用MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[QTHIDAPIUSB示例项目](https://pan.quark.cn/s/271b0ebfb176)