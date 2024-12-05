---
layout: post
title: "基于傅里叶变换的数字盲水印工具"
date:   2022-10-21
tags: [--,水印,python,png,图像]
comments: true
author: admin
---
# 基于傅里叶变换的数字盲水印工具

## 简介

本仓库提供了一个基于傅里叶变换的数字盲水印加解密工具。盲水印技术是一种将水印信息嵌入到图像中而不影响图像视觉质量的技术，常用于版权保护、数据认证等领域。本工具通过Python和OpenCV实现，支持在图像中嵌入和提取水印。

## 资源文件

- **blindwatermark-master.rar**: 包含盲水印加解密的Python脚本及相关资源文件。

## 文件说明

- **encode-python.py**: 用于将水印嵌入到源图像中的加密脚本。
- **decode-python.py**: 用于从嵌入水印的图像中提取水印的解密脚本。

## 依赖环境

- Python
- OpenCV

## 使用方法

### 加密（嵌入水印）

```bash
python encode-python.py --image [源文件] --watermark [水印文件] --result [生成目标文件地址] [--alpha 混杂强度]
```

- `--image`: 源图像文件路径。
- `--watermark`: 水印图像文件路径。
- `--result`: 生成目标文件路径。
- `--alpha`: 混杂强度（可选参数）。

### 解密（提取水印）

```bash
python decode-python.py --original [源文件] --image [待解密文件] --result [水印生成文件地址]
```

- `--original`: 原始图像文件路径。
- `--image`: 待解密的图像文件路径。
- `--result`: 提取的水印生成文件路径。

## 示例

假设你有一张名为`source.png`的图像和一个名为`watermark.png`的水印图像，你可以使用以下命令将水印嵌入到源图像中：

```bash
python encode-python.py --image source.png --watermark watermark.png --result output.png --alpha 0.5
```

然后，你可以使用以下命令从嵌入水印的图像中提取水印：

```bash
python decode-python.py --original source.png --image output.png --result extracted_watermark.png
```

## 注意事项

- 确保源图像和水印图像的尺寸匹配。
- 调整`--alpha`参数可以控制水印的可见性和嵌入强度。

## 适用场景

本工具适用于CTF（Capture The Flag）比赛中的Misc（杂项）题目，以及其他需要进行数字水印嵌入和提取的场景。

## 贡献

欢迎提交问题和改进建议，帮助我们完善这个工具。

## 下载链接

[基于傅里叶变换的数字盲水印工具](https://pan.quark.cn/s/65437d846972)