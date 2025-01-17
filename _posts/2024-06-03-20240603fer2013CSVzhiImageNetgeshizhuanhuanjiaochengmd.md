---
layout: post
title: "fer2013 CSV至ImageNet格式转换教程"
date:   2022-09-18
tags: [CSV,转换,脚本,fer2013,Fer2013]
comments: true
author: admin
---
# fer2013 CSV至ImageNet格式转换教程

## 概述

本仓库提供了用于转换Fer2013人脸表情识别数据集的脚本，此脚本能够将数据集中的CSV格式数据转换为ImageNet风格的存储格式，即按类别组织图片到各自的文件夹下。Fer2013数据集包含了人脸表情的灰度图像，共计七种基本表情，分别是愤怒、厌恶、恐惧、高兴、悲伤、惊讶和中性。

## 文件结构

- `csv2img.py`: 核心转换脚本，负责读取CSV数据，并生成图片文件。
- `fer2013.csv`: 原始Fer2013数据集的CSV文件（需自行下载或已存在于仓库中）。
- `Fer2013Image`: 转换后的图片存储目录，会根据表情类别创建子文件夹存放相应图片。

## 快速指南

### 步骤1：准备环境

确保您的Python环境中已安装以下库：
- NumPy
- OpenCV
- Pandas
- Tqdm（进度条显示）

### 步骤2：运行脚本

1. **下载数据**: 首先，您需要从资源链接或原始来源下载`fer2013.csv`文件。
2. **修改配置**: 确认脚本中的`csv_path`变量指向您的`fer2013.csv`文件路径，`out_dir_path`设置为您希望创建图片目录的路径。
3. **执行转换**: 在命令行界面，运行脚本`python csv2img.py`。

### 步骤3：检查结果

转换完成后，会在指定的`out_dir_path`目录下发现一系列以数字命名的子文件夹（对应不同的表情类别），每个子文件夹内是相应的表情图片。

## 注意事项

- 本脚本假设CSV文件的结构保持不变，如有自定义或更新的CSV结构，请相应调整脚本中的数据处理逻辑。
- 在大量数据转换时，请确保有足够的磁盘空间。
- 转换过程中可能需要一些时间，特别是对于较大的数据集，请耐心等待进度条完成。

通过本仓库提供的脚本，您可以便捷地将Fer2013数据集转换为更加易于深度学习框架使用的目录结构，加速表情识别项目的开发进程。

## 下载链接

[fer2013CSV至ImageNet格式转换教程](https://pan.quark.cn/s/3b510b1f9f0f)