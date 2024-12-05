---
layout: post
title: "Qt  FFmpeg RTSP视频流解码延迟02s以内"
date:   2020-02-04
tags: [FFmpeg,解码,Qt,视频流,延迟]
comments: true
author: admin
---
# Qt + FFmpeg RTSP视频流解码：延迟0.2s以内！

## 项目简介

本项目实现了一路基于Qt和FFmpeg的RTSP视频流解码方案。通过调用FFmpeg API（版本为FFmpeg 4.1.2），我们成功地将视频流的延迟控制在200ms以内，达到了商业使用标准。

## 功能特点

- **低延迟解码**：通过优化FFmpeg的解码流程，实现了低于200ms的视频延迟，适用于对实时性要求较高的应用场景。
- **跨平台支持**：基于Qt框架开发，支持Windows、Linux和macOS等多平台运行。
- **易于集成**：项目代码结构清晰，易于理解和集成到其他项目中。

## 使用说明

1. **环境配置**：
   - 确保系统中已安装Qt开发环境。
   - 下载并配置FFmpeg 4.1.2库，确保编译通过。

2. **编译与运行**：
   - 克隆本仓库到本地。
   - 使用Qt Creator打开项目文件，进行编译。
   - 运行生成的可执行文件，输入RTSP视频流地址，即可开始解码。

3. **参数调整**：
   - 可根据实际需求调整FFmpeg的解码参数，以进一步优化性能。

## 依赖库

- Qt 5.x
- FFmpeg 4.1.2

## 贡献

欢迎大家提出问题和建议，或者提交Pull Request，共同完善本项目。

## 许可证

本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 下载链接

[QtFFmpegRTSP视频流解码延迟0.2s以内](https://pan.quark.cn/s/84144c26b7cf)