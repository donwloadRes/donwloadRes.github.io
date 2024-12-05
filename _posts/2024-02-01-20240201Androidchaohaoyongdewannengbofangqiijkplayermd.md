---
layout: post
title: "Android 超好用的万能播放器ijkplayer"
date:   2023-01-02
tags: [ijkplayer,Android,编解码器,格式,支持]
comments: true
author: admin
---
# Android 超好用的万能播放器——ijkplayer

## 简介

ijkplayer 是由 B 站开源的一款功能强大的视频播放器，支持 Android 和 iOS 平台。它基于 FFmpeg，并支持多种视频格式的硬解码，能够满足大多数视频播放需求。

## 功能特点

- **跨平台支持**：支持 Android 和 iOS 平台。
- **多种视频格式支持**：支持多种视频格式的硬解码，包括但不限于 MP4、AVI、MKV 等。
- **开源项目**：基于 FFmpeg 开发，代码开源，方便开发者进行二次开发和定制。
- **高性能**：采用硬解码技术，播放视频流畅，占用资源少。

## 使用方法

1. **配置编解码器格式支持**：
   - 默认配置为最少支持，如果需要更多格式支持，可以修改配置文件。
   - 可选配置：
     - `module-default.sh`：更多的编解码器/格式
     - `module-lite-hevc.sh`：较少的编解码器/格式（包括 HEVC）
     - `module-lite.sh`：较少的编解码器/格式（默认情况）

2. **编译 ijkplayer**：
   - 进入 `config` 目录，配置编解码器格式支持。
   - 进入 `android/contrib` 目录，编译 FFmpeg。
   - 编译 ijkplayer 库文件。

3. **运行示例项目**：
   - 编译并运行 `ijkplayer-example` 项目，查看播放效果。

## 注意事项

- 如果需要对更多格式进行支持，建议自行编译 ijkplayer。
- 编译过程中可能会遇到一些问题，建议参考官方文档或社区讨论。

## 贡献

欢迎开发者贡献代码，提出问题和建议。可以通过 GitHub 提交 Pull Request 或 Issue。

## 许可证

本项目遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接和本声明。

---

通过以上步骤，您可以轻松地在 Android 项目中集成 ijkplayer，实现高效的视频播放功能。希望这款万能播放器能够帮助您在开发过程中节省时间和精力。

## 下载链接

[Android超好用的万能播放器ijkplayer](https://pan.quark.cn/s/705a278b1554)