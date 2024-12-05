---
layout: post
title: "Webrtc视频黑屏问题 Android H264 硬解码支持更多机型（CPU）- 兼容源码下载"
date:   2020-12-07
tags: [OMX,CPU,黑屏,Webrtc,视频]
comments: true
author: admin
---
# Webrtc视频黑屏问题 Android H264 硬解码支持更多机型（CPU）- 兼容源码下载

## 资源描述

本资源文件旨在解决Webrtc在Android平台上视频黑屏的问题，特别是在使用H264硬解码时，由于原生Webrtc默认仅支持高通、英特尔和三星等国际大厂的CPU，导致许多小众机型或新生CPU的设备无法正常显示视频。

### 问题现象

在使用Webrtc进行视频通话时，视频连接正常，但视频画面为黑屏，无法显示。

### 问题原因

原生Webrtc的`HardwareVideoEncoderFactory.java`和`MediaCodecVideoDecoderFactory`文件默认仅支持部分国际大厂的CPU，如高通、英特尔和三星等。许多小众机型或新生CPU的设备未被支持，导致视频黑屏问题。

### 解决方案

本资源文件提供了对`HardwareVideoEncoderFactory.java`和`MediaCodecVideoDecoderFactory`文件的修改，以兼容更多机型和CPU。具体修改点如下：

- 兼容了多种CPU的手机和电视盒子，如小米4电视、天猫魔盒、华为手机等。
- 添加了对以下CPU的支持：
  - OMX.qcom.
  - OMX.Intel.
  - OMX.Exynos.
  - OMX.Nvidia.H264.
  - OMX.ittiam.video.
  - OMX.SEC.avc.
  - OMX.IMG.MSVDX.
  - OMX.k3.video.
  - OMX.hisi.
  - OMX.TI.DUCATI1.
  - OMX.MTK.VIDEO.
  - OMX.LG.decoder.
  - OMX.rk.video_decoder.
  - OMX.amlogic.

### 使用方法

1. 下载本资源文件。
2. 将原有的`HardwareVideoEncoderFactory.java`和`MediaCodecVideoDecoderFactory`文件替换为本资源文件中的对应文件。
3. 重新编译并运行项目，检查视频黑屏问题是否已解决。

### 注意事项

- 本资源文件仅适用于Android平台。
- 请确保在替换文件前备份原有文件，以便出现问题时可以恢复。

通过使用本资源文件，您可以有效解决Webrtc在Android平台上因CPU兼容性问题导致的视频黑屏现象，提升应用的兼容性和用户体验。

## 下载链接

[Webrtc视频黑屏问题AndroidH264硬解码支持更多机型CPU-兼容源码下载](https://pan.quark.cn/s/1f1c071799d4)