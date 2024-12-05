---
layout: post
title: "lang-segment-anything本地部署"
date:   2020-09-27
tags: [segment,anything,lang,下载,groundingdino]
comments: true
author: admin
---
# lang-segment-anything本地部署

## 简介

`lang-segment-anything` 是一个基于语言文本提示对图像中的物体进行分割的算法。它结合了 `GroundingDINO` 和 `segment-anything` 两大算法，在半自动标注上有很好的应用场景。该算法可以对没有训练的物体进行分割，也就是可以完成文本到图像物体的匹配。

## 本地部署

### 1. 代码及相关文件下载

除了要下载 `lang-segment-anything` 的代码外，还需要下载 `GroundingDINO` 和 `segment-anything` 的一些配置文件和权重。

- 首先进入 GitHub 官网下载 `lang-segment-anything` 的所有文件，可以 `git clone` 或者下载 zip 压缩包。
- 然后下载 `segment-anything` 需要的权重文件，有三种选择：`l`、`b`、`h`，这里只下载了效果最好的 `h`。
- 除此以外还要下载 `GroundingDINO` 的权重文件和对应的配置文件：有 `swinb` 和 `swint` 两种选择。
- `GroundingDINO` 用到了 `bert` 模型，因为在线下载模型很容易连接失败，所以最好也下载到本地，下载以下 5 个文件即可。

### 2. 环境配置

基本上按照 GitHub 上的操作即可，使用 `conda` 从 `yml` 文件创建虚拟环境：

```bash
conda env create -f environment.yml
```

主要是安装 `torch`、`segment-anything` 和 `groundingdino`。注意需要将 `environment.yml` 文件中 `groundingdino` 要修改为 `groundingdino-py`。还有 `lang-sam` 包找不到，可以不安装。`torch` 的安装可以按照以下代码执行：

```bash
pip install torch torchvision torchmetrics --index-url https://download.pytorch.org/whl/cu118
```

### 3. 代码修改

首先修改 `lang-sam` 下面的 `lang-sam.py` 文件，主要是添加了 `bulid_groundingdino_local` 和 `load_model_loacl` 方法用来加载本地 `groundingdino` 模型。注意权重文件和配置文件要对应。

### 4. demo 演示

运行下列代码，首先会提示是否更新 `lightning`，要选择否，更新的版本不行：

```bash
lightning run app app.py
```

运行代码之后，会在网页弹出以下窗口，上传图片之后，就能对图片进行文本提示的分割了。

## 注意事项

- 经试验，`lang-segment-anything` 在 `ubuntu18.04` 系统上成功部署，在 `windows` 系统上失败，建议在 `ubuntu` 系统上部署。

## 下载链接

[lang-segment-anything本地部署](https://pan.quark.cn/s/6b5555ac8827)