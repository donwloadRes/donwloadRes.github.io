---
layout: post
title: "最简单的基于FFMPEG+SDL的视频播放器-最终版"
date:   2024-05-15
tags: [编译,SDL,FFmpeg,gcc,解码]
comments: true
author: admin
---
# 最简单的基于FFMPEG+SDL的视频播放器-最终版

本项目提供了一个最简单的基于FFmpeg和SDL的视频播放器实现，支持多种视频格式的解码和显示，包括HEVC、H.264、MPEG2等。通过学习本例子，您可以了解FFmpeg的基本解码流程，并掌握如何使用SDL进行视频显示。

## 项目描述

本程序实现了视频文件的解码和显示功能，是最简单的FFmpeg视频解码方面的教程。项目包含两个工程：

1. **simplest_ffmpeg_player**：标准版，适合FFmpeg学习的初学者。
2. **simplest_ffmpeg_player_su**：SU（SDL Update）版，加入了简单的SDL事件处理，适合进一步学习SDL的使用。

该程序的最终版不仅支持VC2010编译，还支持以下几种编译方式：

- cl.exe命令行编译
- mingw编译
- gcc编译
- gcc(MacOS)编译

此外，还修复了个别操作系统（例如Ubuntu）中绿屏的问题。

## 使用说明

1. **标准版（simplest_ffmpeg_player）**：
   - 适合FFmpeg初学者，展示了基本的视频解码和显示流程。

2. **SU版（simplest_ffmpeg_player_su）**：
   - 在标准版的基础上加入了SDL事件处理，适合进一步学习SDL的使用。

## 编译方式

本项目支持多种编译方式，您可以根据自己的开发环境选择合适的编译方式：

- **VC2010**：使用Visual Studio 2010进行编译。
- **cl.exe命令行编译**：适用于Windows平台，使用Microsoft的cl.exe编译器。
- **mingw编译**：适用于Windows平台，使用MinGW编译器。
- **gcc编译**：适用于Linux平台，使用gcc编译器。
- **gcc(MacOS)编译**：适用于MacOS平台，使用gcc编译器。

## 注意事项

- 在某些操作系统（如Ubuntu）中可能会出现绿屏问题，本项目已修复该问题。
- 请确保您的开发环境中已正确安装FFmpeg和SDL库。

## 贡献

欢迎大家提交问题和改进建议，共同完善本项目。

## 许可证

本项目采用开源许可证，具体许可证信息请参阅LICENSE文件。

---

希望通过本项目，您能够快速入门FFmpeg和SDL的使用，并掌握视频解码和显示的基本流程。

## 下载链接

[最简单的基于FFMPEGSDL的视频播放器-最终版](https://pan.quark.cn/s/4f605a7db02f)