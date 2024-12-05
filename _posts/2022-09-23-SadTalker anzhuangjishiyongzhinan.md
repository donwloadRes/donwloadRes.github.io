---
layout: post
title: "SadTalker 安装及使用指南"
date:   2021-01-16
tags: [SadTalker,--,生成,安装,使用指南]
comments: true
author: admin
---
# SadTalker 安装及使用指南

## 简介
SadTalker 是一个由西安交通大学开源的人工智能模型，能够通过从音频中学习生成3D运动系数，并使用全新的3D面部渲染器来生成头部运动，从而实现图片+音频生成高质量视频的功能。本资源文件提供了SadTalker的安装及使用指南，帮助用户避免常见的安装和使用问题。

## 功能特点
- **高质量视频生成**：通过图片和音频生成高质量的说话视频。
- **3D面部渲染**：使用先进的3D面部渲染技术，生成逼真的头部运动。
- **支持多种输入**：支持真人图片和接近真人的图片作为输入。
- **集成Stable Diffusion**：支持与Stable Diffusion WebUI集成，方便用户生成和处理图片。

## 安装步骤
1. **环境准备**：
   - 安装Anaconda，用于管理Python环境和包。
   - 配置镜像源，以加快包的下载速度。

2. **创建虚拟环境**：
   - 使用conda创建一个新的虚拟环境，并激活该环境。
   ```bash
   conda create -n sadtalker python=3.8
   conda activate sadtalker
   ```

3. **安装依赖包**：
   - 安装PyTorch和其他必要的依赖包。
   ```bash
   pip install torch==1.12.1+cu113 torchvision==0.13.1+cu113 torchaudio==0.12.1 --extra-index-url https://download.pytorch.org/whl/cu113
   conda install ffmpeg
   pip install -r requirements.txt
   ```

4. **下载模型文件**：
   - 在SadTalker项目根目录下新建`checkpoints`和`gfpgan`目录，并将下载的模型文件放入相应目录中。

## 使用方法
1. **启动UI**：
   - 执行`webui.bat`脚本启动SadTalker的Web UI。
   ```bash
   .\webui.bat
   ```

2. **命令行生成视频**：
   - 通过图片和音频生成视频。
   ```bash
   python inference.py --driven_audio data/sample.wav --source_image data/sample.png
   ```

3. **参数控制**：
   - 使用参数控制生成的视频效果。
   ```bash
   python inference.py --driven_audio data/sample.wav --source_image data/sample.png --preprocess full --still --enhancer gfpgan
   ```

## 常见问题
- **安装失败**：确保使用conda安装包，并指定Python版本为3.8。
- **模型下载慢**：推荐使用镜像站点下载模型文件。
- **CUDA问题**：检查显卡驱动、CUDA和PyTorch版本是否匹配。

## 参考资料
- 详细安装及使用指南请参考：[SadTalker 安装及使用（避坑指南）](https://blog.csdn.net/qq8864/article/details/133632123)

## 贡献
欢迎提交问题和改进建议，帮助我们完善SadTalker的使用指南。

## 许可证
本项目遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[SadTalker安装及使用指南](https://pan.quark.cn/s/af333bc3ec85)