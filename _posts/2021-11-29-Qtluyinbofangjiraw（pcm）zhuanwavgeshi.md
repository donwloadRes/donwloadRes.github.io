---
layout: post
title: "Qt录音播放及raw（pcm）转wav格式"
date:   2021-11-06
tags: [wav,播放,raw,录音,Qt]
comments: true
author: admin
---
# Qt录音播放及raw（pcm）转wav格式

## 资源描述

本资源提供了一个完整的Qt程序，实现了录音机的功能。通过QAudioInput生成的raw文件无法直接用播放器播放，因此本程序还包含了将生成的.raw文件转换为wav格式的音频文件的功能。转换后的wav文件既可以通过QAudioOutput播放，也可以使用其他播放器进行播放。

## 功能特点

1. **录音功能**：使用QAudioInput实现录音，并将录音数据保存为raw格式文件。
2. **格式转换**：将生成的raw文件转换为wav格式，方便播放和使用。
3. **播放功能**：支持使用QAudioOutput播放转换后的wav文件。

## 使用说明

1. **录音**：启动程序后，点击录音按钮开始录音，录音数据将保存为raw格式文件。
2. **转换**：录音结束后，程序会自动将raw文件转换为wav格式。
3. **播放**：转换完成后，可以选择使用QAudioOutput播放wav文件，或使用其他播放器播放。

## 注意事项

- 本程序依赖于Qt库，请确保已安装Qt开发环境。
- 转换后的wav文件可以直接在大多数播放器中播放。

## 适用场景

- 需要使用Qt实现录音功能的开发者。
- 需要将raw格式音频文件转换为wav格式的开发者。
- 需要使用QAudioOutput播放音频文件的开发者。

通过本资源，您可以快速实现一个简单的录音机功能，并掌握raw文件与wav文件之间的转换方法。

## 下载链接

[Qt录音播放及rawpcm转wav格式](https://pan.quark.cn/s/c98950df9fee)