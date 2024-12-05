---
layout: post
title: "Matlab语音信号分离代码 - VMSep-2010：歌声与伴奏的分离"
date:   2024-11-01
tags: [代码,Matlab,文件,分离,伴奏]
comments: true
author: admin
---
# Matlab语音信号分离代码 - VMSep-2010：歌声与伴奏的分离

## 简介

本仓库提供了一个Matlab代码，用于将单声道录音中的演唱声音和伴奏分离。该代码是我清华大学学士学位论文的研究成果。通过本代码，您可以将混合的语音信号分离为独立的歌声和伴奏部分。

## 代码功能

该代码提供了两种运行方式：

1. **直接在Matlab工作区中运行**：
   - 如果您的Matlab工作区中已经存在混合信号，可以使用以下命令调用代码：
     ```matlab
     [voice, accom] = main(mix);
     ```
   - 其中，`mix`是输入的混合信号（必须为单声道，并以16kHz采样）。输出参数`voice`和`accom`将分别是分离出的演唱声音和伴奏。

2. **通过文件输入输出**：
   - 如果混合信号存储在文件中（也必须是以16kHz采样的单声道wav文件），可以使用以下命令调用代码：
     ```matlab
     vmsep(fileMix, fileVoice, fileAccom);
     ```
   - 其中，`fileMix`是输入的混合信号文件名，`fileVoice`和`fileAccom`分别是输出演唱声音文件和输出伴奏文件的名称。您可以省略`.wav`扩展名。如果省略`fileVoice`和`fileAccom`，输出文件的主要名称将是输入文件的主要名称加上`_voice`和`_accom`。

## 代码原理

有关代码的工作原理，请查看`ref`文件夹中的相关文件。这些文件详细解释了代码的实现细节和算法原理。

## 注意事项

- 该代码是我很久以前完成的工作，因此将不再进行更新（抱歉，T_T）。
- 您可以根据自己的需求对代码进行调整和优化。

## 使用说明

1. 下载本仓库中的代码文件。
2. 根据您的需求选择合适的运行方式。
3. 运行代码并查看分离结果。

## 贡献

如果您对代码有任何改进或建议，欢迎提交Pull Request或Issue。

## 许可证

本代码遵循MIT许可证，您可以自由使用、修改和分发。

---

希望本代码对您的研究或项目有所帮助！

## 下载链接

[Matlab语音信号分离代码-VMSep-2010歌声与伴奏的分离](https://pan.quark.cn/s/2ff4183dde1b)