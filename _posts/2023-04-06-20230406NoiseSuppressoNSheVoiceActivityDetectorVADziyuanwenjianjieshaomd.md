---
layout: post
title: "Noise SuppressoNS 和 Voice Activity DetectorVAD 资源文件介绍"
date:   2024-09-20
tags: [语音,文件,NS,VAD,编译]
comments: true
author: admin
---
# Noise Suppresso(NS) 和 Voice Activity Detector(VAD) 资源文件介绍

## 简介
本资源文件包含了基于webrtc 2022/12/10更新版本的Noise Suppressor(NS噪音抑制)和Voice Activity Detector(VAD语音检测)。最新版的VAD采用了RNNiose神经网络分频判断技术，实测基本可以做到语音自动分段。NS噪音抑制的性能也相当出色，默认等级能将背景底噪削弱大半。这些功能可广泛应用于语音直播、优化增强语音效果等应用场景。

## 特点
- **最新技术**：基于webrtc 2022/12/10的更新版本。
- **高性能VAD**：使用RNNiose神经网络分频判断，实现语音自动分段。
- **强大的NS**：噪音抑制效果显著，能大幅削弱背景底噪。
- **平台支持**：目前仅支持Win32平台，基于vc2019编译器修改。
- **独立性**：不依赖任何第三方库，将所有代码文件添加到工程即可编译使用。

## 使用说明
1. **添加代码**：将所有代码文件添加到你的项目工程中。
2. **编译**：使用vc2019编译器进行编译。
3. **调用**：参考压缩包内的`AudioProcessing_example.cpp`文件，了解调用流程。

## 其他平台支持
如果你需要其他系统平台的编译支持，或者希望移植webrtc中Audio Process内的其他过滤处理功能，可以通过邮件或站内消息联系本人。有时间的话，我会酌情考虑帮忙移植。

## 注意事项
- 本资源文件仅支持Win32平台。
- 压缩包内附有从测试工程中剥离的调用演示代码，仅作为调用流程参考。

希望本资源文件能帮助你在语音处理项目中取得更好的效果！

## 下载链接

[NoiseSuppressoNS和VoiceActivityDetectorVAD资源文件介绍](https://pan.quark.cn/s/f38682a11636)