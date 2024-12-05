---
layout: post
title: "Ffmpeg+Qt 简单播放器"
date:   2023-08-12
tags: [Qt,Ffmpeg,Creator,播放器,项目]
comments: true
author: admin
---
# Ffmpeg+Qt 简单播放器

## 项目描述

本项目是一个基于Windows环境，使用Ffmpeg和Qt Creator开发的简单播放器。该播放器具备以下功能：

1. **声音输出**：使用PortAudio库进行声音输出。
2. **视频显示**：使用SDL2库进行视频显示。
3. **音视频同步**：实现了音视频的同步播放。
4. **开发环境**：使用Qt Creator进行开发，便于Debug运行，可以方便地查看Ffmpeg各个结构体的变量变化。

## 项目特点

- **跨平台**：虽然本项目主要在Windows环境下开发，但Ffmpeg和Qt Creator都是跨平台的工具，因此可以轻松移植到其他操作系统。
- **易于调试**：使用Qt Creator进行开发，提供了强大的调试功能，方便开发者查看和分析Ffmpeg的内部状态。
- **模块化设计**：项目结构清晰，各个模块（如声音输出、视频显示、音视频同步）独立开发，便于维护和扩展。

## 使用说明

1. **环境配置**：确保你的开发环境已经安装了Qt Creator、Ffmpeg、PortAudio和SDL2库。
2. **编译运行**：使用Qt Creator打开项目文件，配置好相关库路径后，即可编译并运行项目。
3. **调试**：在Qt Creator中设置断点，逐步调试代码，查看Ffmpeg各个结构体的变量变化。

## 注意事项

- 本项目是一个简单的播放器示例，适合学习和研究Ffmpeg和Qt的使用。
- 由于使用了PortAudio和SDL2库，确保这些库已经正确安装并配置好。

## 贡献

欢迎对本项目进行改进和扩展，如果你有任何建议或发现了bug，请提交issue或pull request。

## 许可证

本项目采用MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[FfmpegQt简单播放器](https://pan.quark.cn/s/3997fa2b91ad)