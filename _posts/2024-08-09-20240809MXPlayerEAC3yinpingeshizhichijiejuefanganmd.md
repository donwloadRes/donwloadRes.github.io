---
layout: post
title: "MX Player EAC3音频格式支持解决方案"
date:   2024-01-24
tags: [MX,Player,解码器,EAC3,版本]
comments: true
author: admin
---
# MX Player EAC3音频格式支持解决方案

## 简介

本仓库提供了一个解决方案，用于解决MX Player不支持EAC3音频格式的问题。MX Player是一款广受欢迎的Android视频播放器，但由于授权问题，从1.69版本开始移除了对AC3/DTS格式的支持，导致无法播放包含EAC3音频的视频文件。

## 解决方案

### 1. 下载MX_FFmpeg解码器

为了支持EAC3格式的音频播放，您需要下载并安装MX_FFmpeg解码器。该解码器可以增强MX Player的音频解码能力，使其能够播放EAC3格式的音频文件。

### 2. 安装步骤

1. **查看MX Player版本**：在MX Player中，进入“选项” → “帮助” → “关于”，查看当前的MX Player版本。
2. **下载对应版本的MX_FFmpeg**：根据您的MX Player版本和处理器架构，下载相应的MX_FFmpeg解码器。例如，如果您的MX Player版本为1.25.0，且处理器为ARMv8 NEON架构，则下载对应的解码器包。
3. **安装解码器**：
   - 在手机存储中任意新建一个文件夹，例如`MxPlayerPro`。
   - 将下载的MX_FFmpeg解码器压缩包放入该文件夹中。
   - 在MX Player中，进入“选项” → “本地播放器设置” → “解码器” → “自定义编解码器”，选择刚刚放入的解码器压缩包。

### 3. 常用配置

- **长按加速**：在播放视频时，长按屏幕可以加速播放。
- **双击播放/暂停**：在“本地播放器设置” → “播放器” → “控制”中，勾选“双击 (播放/暂停)”选项。

## 注意事项

- **解码器版本匹配**：确保下载的MX_FFmpeg解码器版本与您的MX Player版本匹配，否则可能会出现无法识别解码器的情况。
- **字幕加载问题**：如果遇到MKV视频文件中的SRT字幕无法加载的问题，建议直接下载最新版本的MX Player，并按照上述步骤安装解码器。

## 参考资料

本解决方案参考了CSDN博客文章《MX Player不支持此音频格式（EAC3）》，详细内容请参阅原文。

---

通过以上步骤，您应该能够成功解决MX Player不支持EAC3音频格式的问题，享受更丰富的视频播放体验。

## 下载链接

[MXPlayerEAC3音频格式支持解决方案](https://pan.quark.cn/s/47218556267b)