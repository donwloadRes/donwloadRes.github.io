---
layout: post
title: "MMAction2 SlowFast 训练配置与日志分析"
date:   2020-02-13
tags: [训练,py,配置文件,my,slowfast]
comments: true
author: admin
---
# MMAction2 SlowFast 训练配置与日志分析

本仓库提供了一个关于MMAction2框架下SlowFast模型的训练配置文件和训练日志分析资源。具体内容包括：

- **训练日志文件**: `20220805_165139.log.json`
- **训练配置文件**: `my_slowfast_kinetics_pretrained_r50_4x16x1_20e_ava_rgb.py`
- **测试训练集效果的配置文件**: `my_slowfast_kinetics_pretrained_r50_4x16x1_20e_ava_rgb2.py`

## 文件说明

### 训练日志文件
- **文件名**: `20220805_165139.log.json`
- **描述**: 该文件记录了2022年8月5日16时51分39秒开始的训练过程中的详细日志信息，包括训练损失、验证指标等。

### 训练配置文件
- **文件名**: `my_slowfast_kinetics_pretrained_r50_4x16x1_20e_ava_rgb.py`
- **描述**: 该配置文件定义了使用预训练的SlowFast模型在Kinetics数据集上进行训练的参数设置，包括网络结构、优化器、学习率调度等。

### 测试训练集效果的配置文件
- **文件名**: `my_slowfast_kinetics_pretrained_r50_4x16x1_20e_ava_rgb2.py`
- **描述**: 该配置文件是为了测试训练集效果而特别调整的，与主配置文件相比，可能包含了一些针对训练集的优化设置。

## 使用方法

1. **克隆仓库**:
   ```bash
   git clone https://github.com/your-repo-link.git
   ```

2. **查看训练日志**:
   ```bash
   cat 20220805_165139.log.json
   ```

3. **运行训练**:
   ```bash
   python train.py --config my_slowfast_kinetics_pretrained_r50_4x16x1_20e_ava_rgb.py
   ```

4. **测试训练集效果**:
   ```bash
   python train.py --config my_slowfast_kinetics_pretrained_r50_4x16x1_20e_ava_rgb2.py
   ```

## 贡献

欢迎任何形式的贡献，包括但不限于：
- 提交问题
- 提出改进建议
- 提交代码合并请求

## 许可证

本项目采用[MIT许可证](LICENSE)。

---

如有任何问题或建议，请通过[issues](https://github.com/your-repo-link/issues)页面联系我们。

## 下载链接

[MMAction2SlowFast训练配置与日志分析](https://pan.quark.cn/s/caa9b2a06a08)