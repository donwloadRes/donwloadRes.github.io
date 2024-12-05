---
layout: post
title: "使用Stable Diffusion插件StableSR将图片高清放大"
date:   2024-05-05
tags: [StableSR,https,插件,com,模型]
comments: true
author: admin
---
# 使用Stable Diffusion插件StableSR将图片高清放大

本文介绍了如何使用Stable Diffusion插件StableSR将图片高清放大。StableSR是一个强大的工具，能够利用预训练的文本到图像扩散模型中的先验知识，实现盲超分辨率（SR）。通过使用时间感知编码器，StableSR可以在不改变预训练合成模型的情况下，实现令人满意的恢复结果，从而保留生成先验并最小化训练成本。

## 主要内容

### 1. 安装StableSR插件
- 项目地址：https://github.com/pkuliyi2015/sd-webui-stablesr
- 国内镜像：https://gitee.com/han51535/sd-webui-stablesr

### 2. 安装Multidiffusion插件
- 项目地址：https://github.com/pkuliyi2015/multidiffusion-upscaler-for-automatic1111
- 国内镜像：https://gitee.com/stable_diffusion/multidiffusion-upscaler-for-automatic1111

### 3. 下载所需模型
- StabilityAI官方大模型（5.21GB）
- VAE模型（745MB）
- StableSR脚本模型（400MB）

### 4. 开始工作
- 打开SD WEBUI，转到图生图，打开测试的图片。
- 设置Tiled Diffusion，启动VAE切片。
- 脚本设置，选择StableSR脚本模型，设置缩放比。

### 5. 问题解答
- 生成过程中内存溢出的解决方法。

## 总结
StableSR插件提供了一种高效的方法，能够将普通图片放大并提升其清晰度。通过本文的介绍，您可以轻松掌握StableSR的安装和使用方法，实现图片的高清放大。

## 下载链接

[使用StableDiffusion插件StableSR将图片高清放大](https://pan.quark.cn/s/2c333777e9ae)