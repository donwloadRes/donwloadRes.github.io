---
layout: post
title: "使用HuggingfacePEFT和LoRA训练大型语言模型LLM的demo代码"
date:   2024-06-19
tags: [LoRA,模型,脚本,训练,LLM]
comments: true
author: admin
---
# 使用Huggingface、PEFT和LoRA训练大型语言模型（LLM）的demo代码

## 简介

本仓库提供了一个关于使用Huggingface、PEFT（Parameter-Efficient Fine-Tuning）和LoRA（Low-Rank Adaptation）训练大型语言模型（LLM）的demo代码。该资源文件包含几个关键脚本和设置，帮助用户在不同的平台上进行模型训练。

## 资源文件内容

### 1. `setup_lambdalabs.py` 脚本

该脚本用于设置大部分所需的配置，特别适用于使用lambdalabs平台的用户。在使用该脚本之前，你需要创建一个名为`.env`的文件，并在其中包含以下三个条目：

- `LL_SECRET`：lambdalabs的密钥。
- `ssh_key_filename`：私有RSA密钥的路径。
- `training_data_url`：训练数据的URL。

### 2. `train_text.py` 脚本

这是一个用于训练LoRA模型的脚本。你可以通过查看该脚本的头部来调整一些关键设置，包括：

- `model_name`：模型名称。
- `load_in_8bit`：是否以8位加载模型。
- `lora_file_path`：LoRA文件路径。
- `text_filename`：文本文件名。
- `output_dir`：输出目录。
- `cutoff_len`：截断长度。
- `overlap_len`：重叠长度。
- `newline_favor_len`：新行偏好长度。

### 重要提示

当前存在一个保存LoRA模型的问题，用户需要注意这一点。

## 使用方法

1. 克隆本仓库到本地。
2. 根据你的平台和需求，配置相应的环境变量和脚本参数。
3. 运行`setup_lambdalabs.py`脚本进行配置。
4. 运行`train_text.py`脚本进行LoRA模型的训练。

## 注意事项

- 请确保在运行脚本之前，所有必要的依赖项已安装。
- 对于保存LoRA模型的问题，请密切关注并及时更新代码。

## 贡献

欢迎对本仓库进行贡献，包括但不限于代码优化、问题修复和文档改进。请提交PR或提出Issue。

## 许可证

本项目采用MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[使用HuggingfacePEFT和LoRA训练大型语言模型LLM的demo代码](https://pan.quark.cn/s/7be80b75ab63)