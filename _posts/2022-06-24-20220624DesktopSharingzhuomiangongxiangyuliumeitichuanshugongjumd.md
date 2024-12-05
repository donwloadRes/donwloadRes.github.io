---
layout: post
title: "DesktopSharing 桌面共享与流媒体传输工具"
date:   2021-01-27
tags: [编码,硬件,音视频,RTSP,核显]
comments: true
author: admin
---
# DesktopSharing: 桌面共享与流媒体传输工具

## 项目简介

DesktopSharing 是一个功能强大的桌面共享工具，支持屏幕和声卡音视频数据的抓取、编码以及多种流媒体传输协议。该项目的主要功能包括：

- **屏幕采集**：使用 DXGI（适用于 Windows 8 及以上版本）和 GDI 技术进行屏幕数据抓取。
- **音频采集**：通过 WASAPI 技术采集声卡音频数据。
- **音视频编码**：支持 H.264 视频编码和 AAC 音频编码。
- **流媒体传输**：
  - **RTSP 转发**：将编码后的音视频数据进行本地 RTSP 转发。
  - **RTSP 推流**：将音视频数据推送到 RTSP 服务器。
  - **RTMP 推流**：将音视频数据推送到 RTMP 服务器。
- **硬件编码**：
  - **独显硬件编码**：支持 NVIDIA 显卡的 NVENC 硬件编码（仅适用于部分 NVIDIA 显卡）。
  - **核显硬件编码**：支持 Intel 核显的 QSV 硬件编码。
- **用户界面**：提供了一个简单的 UI 界面，方便用户操作。

## 项目进展

目前，DesktopSharing 已经完成了以下功能：

- 屏幕采集（DXGI）和 H.264 编码。
- 音频采集（WASAPI）和 AAC 编码。
- RTSP 本地转发音视频数据。
- RTSP 推流器。
- RTMP 推流器。
- 独显硬件编码（NVENC）。
- 核显硬件编码（QSV）。
- 简单的 UI 界面。

## 后续计划

未来的开发计划包括：

- 进一步优化和完善现有功能。
- 增加更多硬件编码支持。
- 提升用户界面的友好性和功能性。

## 编译环境

- 操作系统：Windows 10
- 开发工具：Visual Studio 2017
- Windows SDK 版本：10.0.17134.0

## 模块说明

- **屏幕采集**：使用 DXGI（适用于 Windows 8 及以上版本）和 GDI 技术。
- **音频采集**：使用 WASAPI 技术。
- **编码器**：
  - 独显硬件编码器：NVENC，版本 8.2
  - 核显硬件编码器：QSV

## 注意事项

- 该项目使用的模块均为开源项目，已在 Visual Studio 2017 和 Visual Studio 2019 下编译通过。
- 独显硬件编码仅支持部分 NVIDIA 显卡。
- 核显硬件编码支持 Intel 核显。

## 贡献与反馈

欢迎开发者参与项目的开发与改进，如果您有任何建议或问题，请通过 GitHub 的 Issues 功能提交反馈。

## 下载链接

[DesktopSharing桌面共享与流媒体传输工具](https://pan.quark.cn/s/3f59644db6e2)