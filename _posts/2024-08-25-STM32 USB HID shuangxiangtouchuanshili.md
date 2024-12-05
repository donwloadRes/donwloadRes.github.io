---
layout: post
title: "STM32 USB HID 双向透传示例"
date:   2021-03-04
tags: [HID,USB,描述符,透传,双向]
comments: true
author: admin
---
# STM32 USB HID 双向透传示例

## 简介

本资源文件是《STM32 USB使用记录：HID类设备（后篇）》的示例代码和相关文档。该文章详细介绍了如何在STM32微控制器上实现USB HID（Human Interface Device）双向透传功能。通过自定义HID设备的报告描述符，实现了USB HID的双向数据传输，适用于免驱设备的应用场景。

## 功能特点

- **双向透传**：实现了USB HID设备的双向数据传输，支持主机与设备之间的数据交互。
- **免驱使用**：大部分情况下，HID设备接入主机后无需安装驱动程序即可使用。
- **自定义报告描述符**：通过调整配置描述符、端口和报告描述符，创建了一个自定义的HID设备。

## 使用说明

1. **项目构建**：
   - 使用STM32Cube工具生成基础项目，选择Custom Human Interface Device Class (HID)。
   - 根据文章中的指导，调整配置描述符、端口和报告描述符。

2. **代码调整**：
   - 修改`usbd_custom_hid_if.c`文件中的报告描述符，实现双向透传功能。
   - 调整`usbd_conf.h`和`usbd_customhid.h`中的定义值，以适应全速USB设备的需求。

3. **接收与发送代码**：
   - 在`usbd_custom_hid_if.c`文件中修改接收事件（OutEvent）部分的代码，实现数据接收和发送。

4. **测试**：
   - 使用提供的测试工具进行设备测试，确保双向透传功能正常工作。

## 示例代码

本资源文件包含了完整的示例代码，可以直接导入到STM32开发环境中进行编译和测试。代码结构清晰，注释详细，方便开发者理解和修改。

## 参考文档

- [STM32 USB使用记录：HID类设备（后篇）](https://blog.csdn.net/naisu_kun/article/details/131880999)

## 贡献

欢迎开发者提交问题和改进建议，共同完善本示例代码。

## 许可证

本资源文件遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[STM32USBHID双向透传示例分享](https://pan.quark.cn/s/ce0e1017eee3)