---
layout: post
title: "Mac OS 安装 Stable Diffusion 详细教程及模型包"
date:   2021-03-13
tags: [Stable,Diffusion,安装,教程,模型]
comments: true
author: admin
---
# Mac OS 安装 Stable Diffusion 详细教程及模型包

本资源文件提供了在 Mac OS 上安装 Stable Diffusion 的详细教程，并附带了所需的模型包。Stable Diffusion 是一款强大的 AI 绘画工具，本文将指导您完成从安装 Home Brew、依赖包、拉取 Web UI 存储库、下载模型、启动项目、测试、安装汉化包及配置语言等全过程。

## 内容概述

1. **安装 Home Brew**
   - 在终端中执行以下命令安装 Home Brew：
     ```bash
     /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
     ```

2. **安装所需依赖**
   - 使用 Home Brew 安装以下依赖包：
     ```bash
     brew install cmake protobuf rust python@3.10 git wget
     ```

3. **拉取 Stable Diffusion Web UI 存储库**
   - 执行以下命令拉取 Stable Diffusion 的 Web UI 仓库代码：
     ```bash
     git clone https://github.com/AUTOMATIC1111/stable-diffusion-webui
     ```

4. **下载模型**
   - 下载模型文件并将其放置在 `stable-diffusion-webui/models/Stable-diffusion` 目录下。

5. **启动项目**
   - 进入项目目录并执行启动命令。

6. **测试与配置**
   - 完成安装后进行测试，并根据需要安装汉化包及配置语言。

## 模型包说明

本资源文件中包含了一个基本的 Stable Diffusion 模型，您可以根据需要下载并使用。模型文件应放置在指定的目录中，以确保项目正常运行。

## 注意事项

- 确保您的 Mac 设备满足运行 Stable Diffusion 的硬件要求。
- 在安装过程中，请按照教程步骤逐一执行，避免跳过关键步骤。
- 如果在安装过程中遇到问题，请参考教程中的常见问题解答部分，或查阅相关文档。

通过本教程，您将能够在 Mac OS 上成功安装并运行 Stable Diffusion，享受 AI 绘画的乐趣。

## 下载链接

[MacOS安装StableDiffusion详细教程及模型包](https://pan.quark.cn/s/50531f8d7cda)