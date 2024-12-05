---
layout: post
title: "ESP32HUB75MatrixPanelI2SDMA 库介绍"
date:   2023-06-19
tags: [矩阵,DMA,I2S,ESP32,LED]
comments: true
author: admin
---
# ESP32-HUB75-MatrixPanel-I2S-DMA 库介绍

## 概述

ESP32-HUB75-MatrixPanel-I2S-DMA 是一个适用于 ESP32 的 Adafruit GFX 兼容库，专门用于驱动 64x32px 或 64x64px 的 HUB75 LED 矩阵模块。该库利用 ESP32 的 DMA 引擎，通过 I2S 接口实现高效的 LED 矩阵驱动，显著提高了刷新率。此外，该库还支持多个面板的链接，使得扩展 LED 矩阵变得更加容易。

## 主要特点

- **低CPU开销**：初始化的像素数据通过 DMA 引擎直接从内存中传输到矩阵输入，减少了 CPU 的负担。
- **快速刷新**：更新像素数据仅需在 DMA 缓冲区上进行按位逻辑操作，无需进行管脚操作或阻塞 IO。
- **全屏 BCM**：库利用二进制代码调制（BCM）在整个矩阵上渲染像素，支持亮度可变的色彩深度。
- **TrueColor 24 位输出**：根据矩阵大小和刷新率，最多可以输出 TrueColor 24 位色彩。
- **CIE 1931 亮度校正**：支持 CIE 1931 亮度校正，实现更自然的 LED 调光效果。
- **Adafruit GFX API 兼容**：可以使用 Adafruit GFX API 进行图形绘制和操作。

## 适用场景

该库适用于需要高刷新率和低 CPU 开销的 LED 矩阵应用场景，例如：

- 动态广告牌
- 信息显示器
- 艺术装置
- 游戏显示器

## 使用方法

1. **安装库**：将该库添加到您的 ESP32 Arduino 或 IDF 项目中。
2. **初始化矩阵**：根据您的硬件配置初始化 HUB75 LED 矩阵。
3. **绘制图形**：使用 Adafruit GFX API 在矩阵上绘制图形或文本。
4. **更新显示**：调用库提供的更新函数，将图形数据传输到 LED 矩阵。

## 示例代码

以下是一个简单的示例代码，展示如何初始化和更新 LED 矩阵：

```cpp
#include <ESP32-HUB75-MatrixPanel-I2S-DMA.h>

MatrixPanel_I2S_DMA *dma_display = nullptr;

void setup() {
  HUB75_I2S_CFG mxconfig;
  mxconfig.mx_width = 64;
  mxconfig.mx_height = 32;

  dma_display = new MatrixPanel_I2S_DMA(mxconfig);
  dma_display->begin();
  dma_display->clearScreen();
}

void loop() {
  dma_display->fillRect(0, 0, 64, 32, dma_display->color565(255, 0, 0));
  delay(1000);
  dma_display->clearScreen();
  delay(1000);
}
```

## 注意事项

- 确保您的 ESP32 硬件支持 I2S DMA 功能。
- 根据实际需求调整矩阵的宽度和高度。
- 在使用多个面板链接时，确保面板之间的连接正确。

## 贡献

欢迎对该库进行改进和优化，如果您有任何建议或问题，请提交到 GitHub 仓库的 Issues 页面。

## 许可证

该库采用开源许可证，具体信息请参阅 LICENSE 文件。

## 下载链接

[ESP32-HUB75-MatrixPanel-I2S-DMA库介绍](https://pan.quark.cn/s/e74d3ed62757)