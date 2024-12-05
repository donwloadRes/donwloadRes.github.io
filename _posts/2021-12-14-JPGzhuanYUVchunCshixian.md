---
layout: post
title: "JPG转YUV纯C实现"
date:   2024-02-03
tags: [JPG,YUV,文件,444,解码]
comments: true
author: admin
---
# JPG转YUV纯C实现

本仓库提供了一个纯C语言实现的JPG转YUV工具，无需任何第三方库。该工具能够将JPG格式的图像文件转换为YUV420或YUV444格式的文件。代码实现包括JPG头解析、Huffman解码、IDCT等关键步骤，适用于Windows、Linux和ARM平台。

## 功能描述

- **JPG转YUV420/YUV444**：支持将JPG图像转换为YUV420或YUV444格式。
- **纯C语言实现**：代码完全使用C语言编写，无任何第三方库依赖。
- **跨平台支持**：已在Windows、Linux和ARM平台上验证通过。

## 使用方法

1. **编译代码**：将代码编译为可执行文件。
2. **运行程序**：使用以下命令运行程序：
   ```
   ./main ./3.jpg ./4.yuv 444
   ```
   其中：
   - `./3.jpg` 是输入的JPG文件路径。
   - `./4.yuv` 是输出的YUV文件路径。
   - `444` 是输出的YUV格式（可选值：`420` 或 `444`）。

## 已知问题

- **Photoshop生成的JPG文件解码失败**：通过Photoshop转换出来的JPG文件在解码时可能会失败，原因是头部信息解析异常。建议使用Windows自带的画图工具另存为JPG文件后再进行解码。

## 注意事项

- 请确保输入的JPG文件路径和输出的YUV文件路径正确。
- 输出的YUV格式参数必须是`420`或`444`，否则程序将无法正确运行。

## 贡献

欢迎提交问题和改进建议，帮助我们完善这个工具。

## 下载链接

[JPG转YUV纯C实现](https://pan.quark.cn/s/c07b4218ccf8)