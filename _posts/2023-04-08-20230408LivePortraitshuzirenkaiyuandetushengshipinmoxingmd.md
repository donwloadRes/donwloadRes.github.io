---
layout: post
title: "LivePortrait 数字人开源的图生视频模型"
date:   2023-04-14
tags: [LivePortrait,视频,https,bash,图生]
comments: true
author: admin
---
# LivePortrait 数字人：开源的图生视频模型

## 简介
LivePortrait 是一个开源的图生视频模型，由快手、中科大和复旦大学联合研发。通过这个模型，用户只需提供一张人脸正面图片和一段文字或音频，即可制作出专业的视频内容，如产品介绍、教学课程、趣味视频等。

## 功能特点
- **图生视频**：只需一张人脸正面图片和一段文字或音频，即可生成动态视频。
- **专业视频制作**：适用于产品介绍、教学课程、趣味视频等多种场景。
- **开源模型**：用户可以自由下载和使用，支持本地部署。

## 使用教程
### 基础环境准备
1. **克隆 GitHub 示例源代码**：
   ```bash
   git clone https://github.com/KwaiVGI/LivePortrait
   ```
2. **安装 Python 依赖包**：
   ```bash
   cd LivePortrait
   conda create -n LivePortrait python==3.9.18
   conda activate LivePortrait
   pip install -r requirements.txt
   ```
3. **下载和配置 FFmpeg 音视频工具库**：
   - 通过 FFmpeg 官网下载：https://ffmpeg.org/download.html
   - 设置 FFmpeg 目录在 PATH 环境变量中，并执行命令进行检测：
     ```bash
     ffmpeg -version
     ```

### 模型权重下载和配置
1. **HF 下载权重文件**：
   ```bash
   git lfs install
   git clone https://www.modelscope.cn/AI-ModelScope/LivePortrait.git pretrained_weights
   cd pretrained_weights
   git lfs pull
   ```
2. **百度云盘或 Google Drive 下载**：
   - 百度云盘：https://pan.baidu.com/s/1MGctWmNla_vZxDbEp2Dtzw
   - Google 云盘：https://drive.google.com/drive/folders/1UtKgzKjFAOmZkhNK-OYT0caJ_w2XAnib

### 使用 LivePortrait 生成视频
1. **终端命令行生成视频**：
   ```bash
   cd LivePortrait
   conda activate LivePortrait
   pip install tyro patch_ng
   python inference.py
   ```
2. **通过 Web 界面生成视频**：
   ```bash
   cd LivePortrait
   conda activate LivePortrait
   python app.py --flag-force-cpu
   ```

## 注意事项
- 建议使用 GPU 进行推理，以提高速度。
- 如果使用 CPU 推理，请确保内存足够（至少 22GB）。

## 参考资料
- LivePortrait 理论研究：https://arxiv.org/pdf/2407.03168
- 更多展示样例：https://liveportrait.github.io/

## 贡献与支持
欢迎开发者贡献代码和提出问题。更多信息请访问 GitHub 仓库。

---

通过以上步骤，您可以轻松地在本地部署 LivePortrait 图生视频模型，并生成您自己的专业视频内容。

## 下载链接

[LivePortrait数字人开源的图生视频模型](https://pan.quark.cn/s/f8898f366347)