---
layout: post
title: "数字人解决方案——ER-NeRF实时对话数字人模型推理部署带UI交互界面"
date:   2024-02-03
tags: [ER,NeRF,UI,对话,bash]
comments: true
author: admin
---
# 数字人解决方案——ER-NeRF实时对话数字人模型推理部署带UI交互界面

## 简介

本仓库提供了一个基于ER-NeRF的实时对话数字人解决方案，包括模型推理部署和UI交互界面。该解决方案集成了大语言模型、语音合成、视频生成和背景替换等功能，旨在实现高效的数字人实时对话体验。

## 主要功能

1. **大语言模型**：使用ChatGLM3-6B模型进行对话生成，支持中英双语，具备强大的语义理解和生成能力。
2. **语音合成**：通过Edge-TTS实现文本到语音的转换，支持多种语言和声音选择。
3. **视频生成**：利用ER-NeRF技术生成数字人的视频流，支持实时对话和口播功能。
4. **背景替换**：提供背景替换功能，用户可以根据需要更换数字人对话的背景。

## 环境要求

- 建议显存：24G以上
- Python版本：3.10或更高

## 安装步骤

1. **下载源码**：
   ```bash
   git clone https://github.com/Fictionarry/ER-NeRF.git
   cd ER-NeRF
   ```

2. **创建虚拟环境**：
   ```bash
   conda create --name vrh python=3.10
   conda activate vrh
   ```

3. **安装依赖**：
   ```bash
   conda install pytorch==2.0.0 torchvision==0.15.0 torchaudio==2.0.0 pytorch-cuda=11.7 -c pytorch -c nvidia
   conda install -c fvcore -c iopath -c conda-forge fvcore iopath
   pip install -r requirements.txt
   pip install tensorflow
   ```

4. **下载pytorch3d**：
   ```bash
   git clone https://github.com/facebookresearch/pytorch3d.git
   cd pytorch3d
   python setup.py install
   ```

## 使用说明

1. **启动UI交互界面**：
   运行以下命令启动UI界面：
   ```bash
   python webui.py
   ```

2. **进行实时对话**：
   在UI界面中输入对话内容，系统将自动生成数字人的视频回复。

## 讨论群

如有任何问题或建议，欢迎加入讨论群：
- 企鹅群号：787501969

## 版权声明

本项目遵循CC 4.0 BY-SA版权协议，转载请附上原文出处声明。

## 下载链接

[数字人解决方案ER-NeRF实时对话数字人模型推理部署带UI交互界面](https://pan.quark.cn/s/52ac07c6eacc)