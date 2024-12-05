---
layout: post
title: "最简单的基于FFmpeg的封装格式处理例子 1.1"
date:   2023-03-26
tags: [FFmpeg,封装,示例,格式,视音频]
comments: true
author: admin
---
# 最简单的基于FFmpeg的封装格式处理例子 1.1

## 简介

本仓库提供了一个基于FFmpeg的封装格式处理解决方案，包含了多个示例程序，帮助开发者理解和使用FFmpeg进行视音频的分离、复用和封装格式转换。该解决方案的1.1版本修复了之前版本中的一些问题，确保了在Release版本下的正常运行，并解决了在复用H.264裸流时声音丢失的错误。

## 主要内容

### 1. simplest ffmpeg demuxer
这是一个视音频分离器的示例程序，展示了如何使用FFmpeg将视频和音频从封装格式中分离出来。

### 2. simplest ffmpeg demuxer simple
这是视音频分离器的简化版示例程序，适合初学者快速上手，理解视音频分离的基本原理。

### 3. simplest ffmpeg muxer
这是一个视音频复用器的示例程序，展示了如何使用FFmpeg将分离后的视频和音频重新封装成新的格式。

### 4. simplest ffmpeg remuxer
这是一个封装格式转换器的示例程序，展示了如何使用FFmpeg将一种封装格式转换为另一种封装格式。

## 版本更新

### 1.1 版本更新内容
- 修复了Release版本下的运行问题。
- 修复了在复用H.264裸流时声音丢失的错误。

## 使用说明

1. 下载本仓库的资源文件。
2. 根据需要选择相应的示例程序进行编译和运行。
3. 参考示例代码，理解FFmpeg在封装格式处理中的应用。

## 注意事项

- 请确保已安装FFmpeg库，并配置好开发环境。
- 示例程序仅供参考，实际使用时请根据具体需求进行调整。

## 贡献

欢迎提交问题和建议，帮助我们改进和完善这个解决方案。

## 下载链接

[最简单的基于FFmpeg的封装格式处理例子1.1](https://pan.quark.cn/s/88e37143efca)