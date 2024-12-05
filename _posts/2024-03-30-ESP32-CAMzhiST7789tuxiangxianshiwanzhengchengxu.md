---
layout: post
title: "ESP32-CAM之ST7789图像显示完整程序"
date:   2024-04-24
tags: [ESP32,CAM,ST7789,图像,GPIO]
comments: true
author: admin
---
# ESP32-CAM之ST7789图像显示完整程序

本仓库提供了一个完整的ESP32-CAM与ST7789显示屏的图像显示程序，以及相关的驱动库。通过本程序，您可以轻松地将ESP32-CAM捕捉到的图像显示在ST7789显示屏上。

## 内容概述

- **ESP32-CAM之ST7789图像显示程序**：这是一个完整的示例程序，展示了如何使用ESP32-CAM捕捉图像，并通过ST7789显示屏进行显示。
- **ST7789驱动库**：提供了ST7789显示屏的驱动库，方便您在ESP32平台上进行图像显示。
- **esp32-camera库**：ESP32-CAM的摄像头驱动库，用于捕捉图像。

## 使用方法

1. **克隆仓库**：
   ```bash
   git clone https://github.com/your-repo-url.git
   ```

2. **安装依赖库**：
   确保您的开发环境中已经安装了ESP-IDF或Arduino IDE，并且已经包含了`esp32-camera`库。

3. **编译与烧录**：
   使用ESP-IDF或Arduino IDE打开项目，编译并烧录到ESP32-CAM开发板上。

4. **连接硬件**：
   将ST7789显示屏正确连接到ESP32-CAM开发板上，确保引脚连接正确。

5. **运行程序**：
   程序运行后，ESP32-CAM将捕捉图像并显示在ST7789显示屏上。

## 硬件连接

| ESP32-CAM引脚 | ST7789引脚 |
|---------------|------------|
| GPIO 18       | SCK        |
| GPIO 19       | SDA        |
| GPIO 23       | RES        |
| GPIO 22       | DC         |
| GPIO 5        | CS         |
| GND           | GND        |
| 3.3V          | VCC        |

## 注意事项

- 确保ESP32-CAM和ST7789的电源电压一致，通常为3.3V。
- 在连接硬件时，请注意引脚的正确对应关系，避免短路或连接错误。

## 贡献

欢迎大家提交问题和改进建议。如果您有更好的实现方法或优化建议，欢迎提交Pull Request。

## 许可证

本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 下载链接

[ESP32-CAM之ST7789图像显示完整程序](https://pan.quark.cn/s/fd94d05694be)