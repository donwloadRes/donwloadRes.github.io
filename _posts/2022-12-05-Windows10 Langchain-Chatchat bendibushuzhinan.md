---
layout: post
title: "Windows10 Langchain-Chatchat 本地部署指南"
date:   2021-05-25
tags: [Chatchat,Langchain,conda,解决,虚拟环境]
comments: true
author: admin
---
# Windows10 Langchain-Chatchat 本地部署指南

本资源文件提供了在Windows 10系统上本地部署Langchain-Chatchat的详细步骤，包括常见问题解决和避坑指南。无论你是从零开始部署，还是遇到问题需要解决，本指南都能为你提供帮助。此外，本资源还附带了全部模型安装包，方便用户快速完成部署。

## 内容概述

1. **环境要求**
   - 安装 Anaconda
   - 安装 CUDA
   - Python 3.8 - 3.11

2. **安装流程**
   - 更新 Conda
   - 创建虚拟环境
   - 下载 Langchain-Chatchat 代码
   - 下载 LLM 模型和 Embedding 模型
   - 初始化数据库
   - 运行 Web 页面

3. **常见问题汇总**
   - 常见错误及解决方法

## 使用说明

1. **更新 Conda**
   - 打开 Anaconda Powershell Prompt
   - 执行 `conda update conda`
   - 测试是否安装成功：`conda list`

2. **创建虚拟环境**
   - 创建虚拟环境：`conda create -n Chatchat python==3.10`
   - 激活虚拟环境：`conda activate Chatchat`

3. **下载 Langchain-Chatchat**
   - 创建目录：`md C:\Chatchat`
   - 进入目录：`cd C:\Chatchat`
   - 下载代码：`git clone https://github.com/chatchat-space/Langchain-Chatchat`

4. **下载模型**
   - 下载 ChatGLM2-6B 和 m3e-base 模型
   - 修改配置文件
   - 下载依赖：`pip install -r requirements.txt`

5. **初始化数据库**
   - 执行 `python init_database.py --recreate-vs`

6. **运行 Web 页面**
   - 执行 `python init_database.py -a`

## 常见问题

- **ModuleNotFoundError: No module named 'pwd'**
  - 解决方法：参考文章中的解决方法

- **OSError: Unable to load vocabulary from file**
  - 解决方法：参考文章中的解决方法

- **AttributeError: 'ChatGLMTokenizer' object has no attribute 'tokenizer'**
  - 解决方法：参考文章中的解决方法

- **AssertionError: Torch not compiled with CUDA enabled**
  - 解决方法：确保 CUDA 和 PyTorch 版本对应

## 注意事项

- 确保 CUDA 和 PyTorch 版本对应，否则可能会报错。
- 在修改配置文件时，路径不要包含中文，否则可能会导致运行报错。

通过本指南，你可以顺利完成 Langchain-Chatchat 的本地部署，并解决可能遇到的各种问题。祝你部署顺利！

## 下载链接

[Windows10Langchain-Chatchat本地部署指南](https://pan.quark.cn/s/957a2fc74264)