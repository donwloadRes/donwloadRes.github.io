---
layout: post
title: "Qt GDAL C++ 遥感图像显示与处理"
date:   2023-03-15
tags: [图像,鼠标,遥感,缩放,bash]
comments: true
author: admin
---
# Qt GDAL C++ 遥感图像显示与处理

## 简介

本项目提供了一个基于Qt和GDAL库的C++应用程序，用于显示和处理遥感图像。该软件不仅支持遥感图像的显示，还提供了鼠标拖动、随鼠标位置缩放等交互功能。此外，还包含了部分栅格图像处理功能，如图像锐化、平滑等，并支持显示矢量图像。

## 功能特性

- **遥感图像显示**：支持多种遥感图像格式的显示，如GeoTIFF、JPEG2000等。
- **交互功能**：
  - 鼠标拖动：用户可以通过鼠标拖动图像，实现图像的平移。
  - 随鼠标位置缩放：用户可以通过鼠标滚轮或特定按键实现图像的缩放，缩放中心为鼠标当前位置。
- **栅格图像处理**：
  - 图像锐化：增强图像的边缘细节。
  - 图像平滑：减少图像噪声，使图像更加平滑。
- **矢量图像显示**：支持显示矢量图像，如Shapefile等。

## 依赖库

- **Qt**：用于构建用户界面和处理用户交互。
- **GDAL**：用于处理遥感图像数据，支持多种栅格和矢量数据格式。

## 安装与使用

1. **克隆仓库**：
   ```bash
   git clone https://github.com/your-repo-url.git
   ```

2. **安装依赖**：
   ```bash
   sudo apt-get install qt5-default libgdal-dev
   ```

3. **编译项目**：
   ```bash
   cd your-repo-directory
   qmake
   make
   ```

4. **运行程序**：
   ```bash
   ./your-executable
   ```

## 贡献

欢迎任何形式的贡献，包括但不限于代码改进、功能扩展、文档完善等。请提交Pull Request或Issue来参与项目。

## 许可证

本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 联系

如有任何问题或建议，请通过[邮箱地址]或[GitHub Issue]联系我们。

## 下载链接

[QtGDALC遥感图像显示与处理](https://pan.quark.cn/s/d0b139df1a81)