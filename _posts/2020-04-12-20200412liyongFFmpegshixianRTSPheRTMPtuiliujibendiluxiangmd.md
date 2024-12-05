---
layout: post
title: "利用FFmpeg实现RTSP和RTMP推流及本地录像"
date:   2020-12-21
tags: [编译,推流,FFmpeg,RTSP,RTMP]
comments: true
author: admin
---
# 利用FFmpeg实现RTSP和RTMP推流及本地录像

本项目是从 `xdisp_virt` 项目中剥离出来的，主要功能是实现实时的 H264 + AAC 编码音频和视频的 RTSP 和 RTMP 协议推流，以及保存到本地的 MP4 和 MKV 录像文件。

## 项目描述

本项目提供了一个核心的推流和本地录像功能，并附带一个简单的调用示例。为了成功编译本项目，需要下载和编译 FFmpeg 库、libfdk-aac 库以及 x264 库。这些库的编译过程可能会非常耗时。如果你不想自己编译这些库，可以直接使用已经编译好的 `stream_push.dll` 动态库。

- **stream_push 目录**：包含实现核心推流和保存本地录像的工程。
- **demo 目录**：包含一个简单的调用示例，演示了如何抓取屏幕并推流到 RTSP/RTMP 服务器，以及保存到本地。
- **bin 目录**：包含已经编译好的二进制文件。

## 编译依赖

为了成功编译本项目，你需要下载和编译以下库：

- FFmpeg 库
- libfdk-aac 库
- x264 库

这些库的编译过程可能会非常耗时，如果你不想自己编译，可以直接使用已经编译好的 `stream_push.dll` 动态库。

## 使用方法

1. **编译依赖库**：
   - 下载并编译 FFmpeg 库、libfdk-aac 库和 x264 库。
   - 将编译好的库文件添加到项目中。

2. **编译项目**：
   - 进入 `stream_push` 目录，编译核心推流和本地录像工程。
   - 进入 `demo` 目录，编译调用示例。

3. **运行示例**：
   - 运行 `demo` 目录中的示例程序，抓取屏幕并推流到 RTSP/RTMP 服务器，以及保存到本地。

## 参考资料

更多详细信息和编译步骤可以参考我的博客文章：[利用FFmpeg实现RTSP和RTMP推流及本地录像](https://blog.csdn.net/fanxiushu/article/details/80996391)

## 许可证

本项目遵循相应的开源许可证，请参考具体文件中的许可证声明。

## 联系方式

如有任何问题或建议，请通过以下方式联系我：

- 邮箱：[your-email@example.com]
- 博客：[https://blog.csdn.net/fanxiushu](https://blog.csdn.net/fanxiushu)

感谢你的关注和支持！

## 下载链接

[利用FFmpeg实现RTSP和RTMP推流及本地录像](https://pan.quark.cn/s/2fcf87ec8247)