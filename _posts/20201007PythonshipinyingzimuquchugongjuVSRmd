---
layout: post
title: "Python视频硬字幕去除工具VSR"
date:   2022-08-12
tags: [字幕,去除,视频,VSR,conda]
comments: true
author: admin
---
# Python视频硬字幕去除工具VSR

## 项目简介

VSR（Video-subtitle-remover）是一款基于AI技术的视频硬字幕去除工具。它能够无损分辨率地将视频中的硬字幕去除，并生成去除字幕后的文件。通过超强AI算法模型，VSR可以对去除字幕文本的区域进行填充（非相邻像素填充与马赛克去除），确保去除字幕后的视频质量不受影响。

## 主要功能

1. **无损分辨率去除字幕**：VSR能够在不降低视频分辨率的情况下，精确去除视频中的硬字幕。
2. **AI算法填充**：使用先进的AI算法，对去除字幕的区域进行智能填充，避免出现马赛克或像素化现象。
3. **自定义字幕位置**：支持用户自定义字幕位置，仅去除指定位置中的字幕。
4. **全视频自动去除**：支持全视频自动去除所有文本，无需手动指定字幕位置。
5. **批量处理**：支持多选图片批量去除水印文本，提高处理效率。

## 使用说明

### 直接下载运行

1. 下载压缩包并解压。
2. 运行程序，如果不能运行，请按照以下教程尝试源码安装conda环境运行。

### 源码安装运行

1. **下载安装Miniconda**
   - Windows: 下载并安装 `Miniconda3-py38_4.11.0-Windows-x86_64.exe`
   - Linux: 下载并安装 `Miniconda3-py38_4.11.0-Linux-x86_64.sh`

2. **创建并激活虚拟环境**
   - 切换到源码所在目录：`cd <源码所在目录>`
   - 创建激活conda环境：
     ```bash
     conda create -n videoEnv python=3.8
     conda activate videoEnv
     ```

3. **安装依赖文件**
   - 确保已安装Python 3.8+，使用conda创建项目虚拟环境并激活环境。
   - 安装CUDA和cuDNN（Linux用户）：
     ```bash
     wget https://developer.download.nvidia.com/compute/cuda/11.7.0/local_installers/cuda_11.7.0_515.43.04_linux.run
     sudo sh cuda_11.7.0_515.43.04_linux.run
     ```
   - 添加环境变量并安装cuDNN。

4. **运行程序**
   - 运行图形化界面：`python gui.py`
   - 运行命令行版本（CLI）：`python ./backend/main.py`

## 常见问题

1. **CondaHTTPError**：将项目中的`.condarc`文件放在用户目录下（如 `C:/Users/<你的用户名>`），如果用户目录已经存在该文件则覆盖。
2. **7z文件解压错误**：升级7-zip解压程序到最新版本。

## 系统要求

- **GPU**：GTX 1060或以上显卡（仅限Nvidia显卡，AMD显卡不支持）
- **CPU**：支持AVX指令集

## 项目开源地址

[GitHub项目地址](https://github.com/YaoFANGUK/video-subtitle-remover)

## 联系我们

如有任何问题或建议，欢迎通过GitHub Issues或邮件联系我们。

## 下载链接

[Python视频硬字幕去除工具VSR分享](https://pan.quark.cn/s/9a73f15c2bdf)