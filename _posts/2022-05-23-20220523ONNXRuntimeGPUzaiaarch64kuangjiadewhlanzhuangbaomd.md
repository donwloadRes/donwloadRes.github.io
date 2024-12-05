---
layout: post
title: "ONNX Runtime GPU 在 aarch64 框架的 whl 安装包"
date:   2022-08-26
tags: [aarch64,安装包,whl,ONNX,Runtime]
comments: true
author: admin
---
# ONNX Runtime GPU 在 aarch64 框架的 whl 安装包

## 简介

本仓库提供了一个适用于 aarch64 架构的 ONNX Runtime GPU 版本的 whl 安装包。ONNX Runtime 是一个开源的深度学习推断引擎，支持在不同硬件平台上运行训练好的模型并进行推断。该安装包特别针对 aarch64 架构进行了优化，适用于如 NVIDIA Jetson 系列等嵌入式设备。

## 安装包信息

- **版本**: 1.4.0 ~ 1.11.0
- **架构**: aarch64 (ARM64)
- **适用环境**: Linux + Python 3.6
- **支持**: 配合 CUDA 10.0 和 cuDNN 7.6.3 使用

## 安装方法

1. 下载 whl 安装包。
2. 使用 pip 进行安装：
   ```bash
   pip install onnxruntime_gpu-<版本号>-cp36-cp36m-linux_aarch64.whl
   ```

## 注意事项

- 该安装包适用于 aarch64 架构的设备，如 NVIDIA Jetson 系列。
- 安装前请确保已安装 CUDA 10.0 和 cuDNN 7.6.3。
- 请勿随意升级系统自带的 Python 版本。

## 其他资源

- 更多关于 ONNX Runtime 的信息，请参考官方文档。
- 如需在 NVIDIA Jetson 上安装其他开源附加包和框架，请访问 Jetson Zoo。

## 贡献

欢迎提交问题和建议，帮助改进本仓库。

## 许可证

本项目遵循 CC 4.0 BY-SA 版权协议。转载请附上原文出处链接和本声明。

## 下载链接

[ONNXRuntimeGPU在aarch64框架的whl安装包](https://pan.quark.cn/s/d737f214b02f)