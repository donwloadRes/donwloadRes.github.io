---
layout: post
title: "OpenCV 420 编译所需资源文件下载仓库"
date:   2024-01-23
tags: [编译,OpenCV,opencv,videoio,ffmpeg]
comments: true
author: admin
---
# OpenCV 4.2.0 编译所需资源文件下载仓库

本仓库提供了编译 OpenCV 4.2.0 所需的资源文件，特别是 `opencv_videoio_ffmpeg.dll` 和 `opencv_videoio_ffmpeg_64.dll`。由于网络原因，这些文件可能无法直接从官方源下载，因此我将所有相关文件放到了 `.cache` 文件夹中，方便大家使用。

## 资源文件说明

- **opencv_videoio_ffmpeg.dll**: 适用于32位系统的FFmpeg视频IO库。
- **opencv_videoio_ffmpeg_64.dll**: 适用于64位系统的FFmpeg视频IO库。

## 使用方法

1. **下载仓库**: 首先，将本仓库下载到本地。
2. **配置CMake**: 使用CMake配置OpenCV 4.2.0的编译路径，确保选择正确的编译选项。
3. **编译**: 使用Qt的`mingw32-make`进行编译。

## 注意事项

- 确保在CMake配置时，选择正确的编译路径，以便找到`.cache`文件夹中的资源文件。
- 如果你在编译过程中遇到任何问题，请检查是否正确配置了CMake和编译环境。

## 贡献

如果你有任何改进建议或发现了问题，欢迎提交Issue或Pull Request。

## 许可证

本仓库中的资源文件遵循OpenCV的许可证。请在使用前仔细阅读相关许可证条款。

## 下载链接

[OpenCV4.2.0编译所需资源文件下载仓库](https://pan.quark.cn/s/8f3d3ac435b5)