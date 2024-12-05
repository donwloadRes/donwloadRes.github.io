---
layout: post
title: "ChatGLM3 多轮对话训练数据"
date:   2020-09-13
tags: [json,训练,train,test,data]
comments: true
author: admin
---
# ChatGLM3 多轮对话训练数据

## 资源描述

本仓库提供了一个用于训练 ChatGLM3 模型的多轮对话数据集。该数据集包含了原始数据、数据处理代码以及训练所需的 `train.json`、`dev.json` 和 `test.json` 文件。

## 数据结构

- **原始数据**: 包含多轮对话的原始文本数据。
- **处理代码**: 用于处理原始数据并生成训练数据的代码。
- **train.json**: 训练数据文件，存放于 `finetune_demo/data/JDMulConversations/train.json`。
- **dev.json**: 验证数据文件，用于模型训练过程中的验证。
- **test.json**: 测试数据文件，用于模型训练后的测试。

## 使用说明

### 数据存放位置

训练数据文件 `train.json` 存放在 `finetune_demo/data/JDMulConversations/train.json` 路径下。

### 修改 Lora 配置

在使用该数据集进行训练前，需要修改 Lora 配置文件，具体配置如下：

```yaml
data_config:
  train_file: train.json
  val_file: dev.json
  test_file: test.json
  num_proc: 16
```

### 训练命令

使用以下命令进行模型训练：

```bash
CUDA_VISIBLE_DEVICES=1 python finetune_hf.py data/JDMulConversations/ /root/autodl-tmp/model/chatglm3-6b configs/lora.yaml
```

## 注意事项

- 确保数据路径正确，避免训练过程中出现路径错误。
- 根据实际需求调整 `num_proc` 参数，以优化数据处理速度。
- 训练过程中请确保 CUDA 设备可用，并根据实际情况调整 `CUDA_VISIBLE_DEVICES` 参数。

## 贡献

欢迎提交 Issue 或 Pull Request 来改进本数据集和相关代码。

## 下载链接

[ChatGLM3多轮对话训练数据](https://pan.quark.cn/s/70a2cd367ff1)