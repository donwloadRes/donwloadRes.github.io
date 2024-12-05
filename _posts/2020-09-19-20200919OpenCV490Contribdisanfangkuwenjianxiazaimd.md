---
layout: post
title: "OpenCV 490  Contrib 第三方库文件下载"
date:   2023-10-30
tags: [4.9,OpenCV,文件,opencv,ffmpeg]
comments: true
author: admin
---
# OpenCV 4.9.0 + Contrib 第三方库文件下载

## 资源描述

本仓库提供了一个资源文件的下载，主要用于解决在 Windows 10 环境下编译安装 OpenCV 4.9.0 + Contrib 时遇到的第三方库文件下载失败及 `setlocal` 错误的问题。资源文件包括以下内容：

### 1. opencv4.9.0_3rd.zip

该文件包含了 OpenCV 4.9.0 所需的第三方库文件，解压后应放置在 `opencv-4.9.0/build/3rdparty/ffmpeg/` 目录下。具体内容包括：

- `ffmpeg_version.cmake`
- `opencv_videoio_ffmpeg.dll`
- `opencv_videoio_ffmpeg_64.dll`
- `ippicv/` 目录

### 2. downloads.zip

该文件包含了 OpenCV 4.9.0 编译过程中所需的额外下载文件，解压后应放置在 `opencv-4.9.0/build/downloads` 目录下。具体内容包括：

- `wechat_qrcode/` 目录
  - `detect.caffemodel`
  - `detect.prototxt`
  - `sr.caffemodel`
  - `sr.prototxt`
- `xfeatures2d/` 目录
  - `boostdesc_bgm.i`
  - `boostdesc`
  - `binboost_064.i`
  - `vgg_generated_48.i`

## 使用方法

1. 下载本仓库提供的 `opencv4.9.0_3rd.zip` 和 `downloads.zip` 文件。
2. 解压 `opencv4.9.0_3rd.zip` 文件到 `opencv-4.9.0/build/3rdparty/ffmpeg/` 目录。
3. 解压 `downloads.zip` 文件到 `opencv-4.9.0/build/downloads` 目录。
4. 按照 OpenCV 官方文档继续进行编译安装。

## 注意事项

- 请确保解压路径正确，否则可能会导致编译失败。
- 如果在编译过程中仍然遇到问题，请参考 OpenCV 官方文档或社区支持。

希望本资源能够帮助你顺利完成 OpenCV 4.9.0 + Contrib 的编译安装！

## 下载链接

[OpenCV4.9.0Contrib第三方库文件下载](https://pan.quark.cn/s/99bdcb93fc2f)