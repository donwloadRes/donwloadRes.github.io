---
layout: post
title: "Draco 编解码器可执行文件"
date:   2020-03-24
tags: [Draco,draco,exe,decoder,encoder]
comments: true
author: admin
---
# Draco 编解码器可执行文件

## 简介

本仓库提供了一个已编译的 Draco 编解码器可执行文件，包括 `draco_decoder.exe` 和 `draco_encoder.exe`。这些程序可以直接运行，无需额外配置，完全免费使用。

## 文件说明

- **draco_decoder.exe**: Draco 解码器，用于将 Draco 压缩的 3D 模型解码为原始格式。
- **draco_encoder.exe**: Draco 编码器，用于将 3D 模型压缩为 Draco 格式。

## 使用方法

1. **解码器使用**:
   - 将 `draco_decoder.exe` 放置在你希望解码的 Draco 文件所在的目录中。
   - 打开命令行工具，导航到该目录。
   - 运行以下命令进行解码：
     ```
     draco_decoder.exe -i input.drc -o output.obj
     ```
   - 其中 `input.drc` 是输入的 Draco 文件，`output.obj` 是输出的解码文件。

2. **编码器使用**:
   - 将 `draco_encoder.exe` 放置在你希望编码的 3D 模型文件所在的目录中。
   - 打开命令行工具，导航到该目录。
   - 运行以下命令进行编码：
     ```
     draco_encoder.exe -i input.obj -o output.drc
     ```
   - 其中 `input.obj` 是输入的 3D 模型文件，`output.drc` 是输出的 Draco 压缩文件。

## 注意事项

- 请确保输入文件格式与命令中的格式一致。
- 本程序为免费使用，无需任何授权。

## 贡献

如果你有任何改进建议或发现了问题，欢迎提交 Issue 或 Pull Request。

## 许可证

本项目遵循 MIT 许可证。详情请参阅 [LICENSE](LICENSE) 文件。

## 下载链接

[Draco编解码器可执行文件](https://pan.quark.cn/s/5d56ea5761b9)