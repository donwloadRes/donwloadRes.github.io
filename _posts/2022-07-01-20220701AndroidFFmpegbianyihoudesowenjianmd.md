---
layout: post
title: "Android FFmpeg 编译后的so文件"
date:   2023-06-05
tags: [so,FFmpeg,文件,编译,Android]
comments: true
author: admin
---
# Android FFmpeg 编译后的so文件

本仓库提供了一个资源文件的下载，包含基于 FFmpeg 5.0.1 和 FFmpeg 4.3.2 编译后的 so 文件，适用于 Android 平台的快速接入。资源文件中包含了 arm64-v8a 和 armeabi-v7a 架构的 so 文件，以及相应的 include 文件。

## 资源文件内容

- **FFmpeg 5.0.1 编译后的 so 文件**
  - 架构：arm64-v8a, armeabi-v7a
  - 包含的 so 文件：
    - libavcodec.so
    - libavfilter.so
    - libavformat.so
    - libavutil.so
    - libswresample.so
    - libswscale.so
  - 包含的 include 文件

- **FFmpeg 4.3.2 编译后的 so 文件**
  - 架构：arm64-v8a, armeabi-v7a
  - 包含的 so 文件：
    - libavcodec.so
    - libavfilter.so
    - libavformat.so
    - libavutil.so
    - libswresample.so
    - libswscale.so
  - 包含的 include 文件

## 使用说明

1. **下载资源文件**：
   你可以直接下载本仓库中的资源文件，解压后即可使用。

2. **集成到 Android 项目**：
   将解压后的 so 文件和 include 文件分别放置到你的 Android 项目的 `jniLibs` 目录和 `src/main/cpp` 目录中。

3. **配置 CMakeLists.txt**：
   在你的 `CMakeLists.txt` 文件中添加相应的配置，以确保能够正确链接这些 so 文件。

4. **开始使用 FFmpeg**：
   配置完成后，你就可以在你的 Android 项目中使用 FFmpeg 提供的功能了。

## 注意事项

- 本资源文件仅包含编译后的 so 文件和 include 文件，不包含源代码。
- 请根据你的项目需求选择合适的 FFmpeg 版本（5.0.1 或 4.3.2）。
- 如果你需要自定义编译 FFmpeg，请参考 FFmpeg 官方文档进行编译。

## 贡献

如果你有任何问题或建议，欢迎提交 Issue 或 Pull Request。

## 许可证

本资源文件遵循 FFmpeg 的许可证，具体请参考 FFmpeg 官方文档。

## 下载链接

[AndroidFFmpeg编译后的so文件](https://pan.quark.cn/s/308b0121eb46)