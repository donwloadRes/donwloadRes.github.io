---
layout: post
title: "SVD生成视频可本地部署ComfyUI使用指南二使用Stable Video Diffusion生成视频"
date:   2021-09-27
tags: [SVD,视频,生成,ComfyUI,显存]
comments: true
author: admin
---
# 【SVD生成视频+可本地部署】ComfyUI使用指南（二）——使用Stable Video Diffusion生成视频

本资源文件提供了使用ComfyUI和Stable Video Diffusion（SVD）生成视频的详细指南。SVD是由Stability AI开源的稳定视频扩散模型，能够将静止图像转换为动态视频。

## 内容概述

1. **SVD简介**
   - SVD是什么？
   - SVD能做什么？
   - SVD的缺点（不能干的事情）

2. **在ComfyUI中使用SVD**
   - 环境要求（约15G显存）
   - 使用Stable-XL生成图片再生成视频（Text2Img2Video）
   - 第一次初始化+运行示例
   - 第二次生成图片+视频

3. **方法**
   - SVD的训练过程
   - 使用Nvidia提出的Align your Latents基本结构

## 使用说明

1. **环境准备**
   - 确保显存至少为15G。
   - 下载并安装ComfyUI。

2. **模型下载**
   - 从官方地址下载SVD模型。

3. **运行示例**
   - 按照指南进行第一次初始化和运行示例。
   - 第二次生成图片和视频，注意时间和显存的使用。

4. **注意事项**
   - 生成的视频长度较短（<=4秒）。
   - 模型可能生成没有运动的视频或非常慢的相机平移。
   - 不能直接使用文本控制模型，需串联其他模型。

## 贡献与反馈

欢迎对本指南提出改进建议或贡献代码。请通过GitHub的Issues或Pull Requests进行反馈。

## 版权声明

本资源文件遵循CC 4.0 BY-SA版权协议，转载请附上原文出处声明。

## 下载链接

[SVD生成视频可本地部署ComfyUI使用指南二使用StableVideoDiffusion生成视频](https://pan.quark.cn/s/fd87e555da14)