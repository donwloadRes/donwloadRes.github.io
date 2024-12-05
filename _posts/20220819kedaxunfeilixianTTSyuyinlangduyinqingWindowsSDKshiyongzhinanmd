---
layout: post
title: "科大讯飞离线TTS语音朗读引擎 Windows SDK 使用指南"
date:   2023-07-01
tags: [科大,SDK,离线,AppID,DLL]
comments: true
author: admin
---
# 科大讯飞离线TTS语音朗读引擎 Windows SDK 使用指南

## 简介
本仓库提供了一个基于科大讯飞离线TTS语音朗读引擎的Windows SDK资源文件，该资源文件包含了C代码封装成DLL，并通过C#在Unity中调用的示例。该示例主要用于将文字合成为.wav音频文件。

## 资源文件说明
- **tts_offline_sample.c**: 封装DLL的源文件，用于将科大讯飞的离线TTS引擎封装成DLL供C#调用。
- **ToSpeech.cs**: Unity调用脚本，用于在Unity项目中调用封装好的DLL，实现文字到语音的转换。

## 使用步骤
1. **获取科大讯飞SDK**: 由于科大讯飞的离线SDK与AppID是捆绑的，因此需要在科大讯飞开发平台生成自己的应用和AppID，并下载Windows离线语音合成SDK。
2. **运行Demo**: 下载并运行科大讯飞提供的Demo，确保能够运行Demo中的samples内的测试文件。
3. **替换代码**: 使用本仓库中的`tts_offline_sample.c`代码替换Demo中的`tts_offline_sample.c`文件。
4. **配置AppID**: 确保在代码中正确配置了AppID，以保证SDK的正常运行。
5. **Unity调用**: 在Unity项目中使用`ToSpeech.cs`脚本调用封装好的DLL，实现文字到语音的转换。

## 注意事项
- 请确保在科大讯飞开发平台生成的AppID与代码中的AppID一致，否则可能导致SDK无法正常工作。
- 该Demo仅实现了将文字合成为.wav文件的功能，如需进一步扩展，请根据实际需求进行修改。

## 贡献
欢迎大家提交Issue和Pull Request，共同完善本仓库的内容。

## 许可证
本仓库的代码遵循MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[科大讯飞离线TTS语音朗读引擎WindowsSDK使用指南](https://pan.quark.cn/s/3c926a83d24d)