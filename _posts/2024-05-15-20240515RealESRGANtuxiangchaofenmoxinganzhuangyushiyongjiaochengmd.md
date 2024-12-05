---
layout: post
title: "RealESRGAN图像超分模型安装与使用教程"
date:   2021-06-15
tags: [--,Real,ESRGAN,bash,超分]
comments: true
author: admin
---
# Real-ESRGAN图像超分模型安装与使用教程

## 简介
Real-ESRGAN是一个基于深度学习的图像超分辨率重建模型，能够显著提高图像的分辨率和清晰度。本教程详细介绍了Real-ESRGAN的安装和使用方法，适用于Python开发者和对图像处理感兴趣的用户。

## 安装步骤

### 1. 环境准备
- Python >= 3.7 (推荐使用Anaconda或Miniconda)
- PyTorch >= 1.7

### 2. 项目安装
1. 克隆项目仓库：
   ```bash
   git clone https://github.com/xinntao/Real-ESRGAN.git
   cd Real-ESRGAN
   ```

2. 安装依赖库：
   ```bash
   pip install basicsr
   pip install facexlib
   pip install gfpgan
   pip install -r requirements.txt
   python setup.py develop
   ```

### 3. 模型下载
下载预训练模型并将其放置在项目文件夹的`weights`目录中。

## 使用方法

### 1. 图片超分
运行以下命令进行图片超分：
```bash
python inference_realesrgan.py -i inputs -o results
```

### 2. 视频超分
运行以下命令进行视频超分：
```bash
python inference_realesrgan_video.py -i inputs -o results
```

## 参数说明
- `-i` 或 `--input`：输入图像或文件夹路径。
- `-o` 或 `--output`：输出文件夹路径。
- `-n` 或 `--model_name`：指定使用的模型名称。
- `-s` 或 `--outscale`：指定最终的放大倍数。
- `-t` 或 `--tile`：指定瓦片大小，0表示无瓦片。
- `--face_enhance`：使用GFPGAN增强人脸。

## 示例
假设你有一个名为`input.jpg`的图片，想要将其分辨率提高4倍，可以使用以下命令：
```bash
python inference_realesrgan.py -i input.jpg -o output -s 4
```

## 注意事项
- 如果遇到CUDA内存不足的问题，可以尝试减小`--tile`的值。
- 使用`--face_enhance`参数可以增强人脸细节，但会增加计算时间。

## 参考
本教程基于Real-ESRGAN项目，更多详细信息请参考项目官方文档。

## 下载链接

[Real-ESRGAN图像超分模型安装与使用教程](https://pan.quark.cn/s/2f192092fc06)