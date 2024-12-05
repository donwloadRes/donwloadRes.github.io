---
layout: post
title: "C语言归一化混音示例"
date:   2024-02-18
tags: [混音,归一化,源码,ALSA,示例]
comments: true
author: admin
---
# C语言归一化混音示例

## 简介

本仓库提供了一个C语言归一化混音的示例，包含源码和音频文件。为了方便测试，还附带了Linux下使用ALSA播放PCM的源码。

## 内容

- **归一化混音源码**: 提供了C语言实现的归一化混音算法，可以直接用于音频处理。
- **音频文件**: 包含用于测试的音频文件，可以直接用于混音测试。
- **ALSA播放PCM源码**: 提供了在Linux系统下使用ALSA库播放PCM音频的示例代码，方便用户测试混音效果。

## 使用方法

1. **编译归一化混音源码**:
   ```bash
   gcc -o normalize_mixer normalize_mixer.c
   ```

2. **编译ALSA播放PCM源码**:
   ```bash
   gcc -o alsa_play alsa_play.c -lasound
   ```

3. **运行归一化混音程序**:
   ```bash
   ./normalize_mixer input1.wav input2.wav output.wav
   ```

4. **使用ALSA播放混音后的音频**:
   ```bash
   ./alsa_play output.wav
   ```

## 注意事项

- 确保在Linux系统下使用，并已安装ALSA库。
- 音频文件格式为WAV，确保输入文件格式正确。

## 贡献

欢迎提交问题和改进建议，帮助完善本示例。

## 许可证

本项目采用MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[C语言归一化混音示例](https://pan.quark.cn/s/d554e5f0c5ee)