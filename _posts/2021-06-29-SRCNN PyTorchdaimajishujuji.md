---
layout: post
title: "SRCNN PyTorch代码及数据集"
date:   2023-03-12
tags: [py,--,path,SRCNN,train]
comments: true
author: admin
---
# SRCNN PyTorch代码及数据集

## 简介
本资源文件提供了基于PyTorch实现的SRCNN（Super-Resolution Convolutional Neural Network）代码，附带详细的注释和数据集。SRCNN是一种用于图像超分辨率的深度学习模型，能够将低分辨率图像转换为高分辨率图像。

## 内容概述
1. **代码结构**：
   - `prepare.py`：数据集预处理脚本，将图像数据转换为h5格式。
   - `train.py`：模型训练脚本，包含训练过程的详细注释。
   - `test.py`：模型测试脚本，用于评估模型性能。
   - `model.py`：SRCNN模型定义脚本。
   - `utils.py`：辅助函数脚本，包含数据处理和评估指标计算等功能。

2. **数据集**：
   - 提供了`img-91`作为训练集，`Set5`作为测试集。
   - 数据集已转换为h5格式，方便直接用于训练和测试。

3. **使用说明**：
   - 运行`prepare.py`进行数据集预处理。
   - 运行`train.py`开始模型训练。
   - 运行`test.py`进行模型测试和结果评估。

## 依赖环境
- Python 3.x
- PyTorch
- NumPy
- h5py
- PIL (Pillow)

## 安装与运行
1. 克隆仓库到本地：
   ```bash
   git clone https://github.com/your-repo/srcnn-pytorch.git
   cd srcnn-pytorch
   ```

2. 安装依赖：
   ```bash
   pip install -r requirements.txt
   ```

3. 运行数据预处理：
   ```bash
   python prepare.py --images-dir path/to/images --output-path path/to/output
   ```

4. 开始训练：
   ```bash
   python train.py --train-file path/to/train.h5 --eval-file path/to/eval.h5 --outputs-dir path/to/outputs
   ```

5. 进行测试：
   ```bash
   python test.py --image-file path/to/image --model-file path/to/model.pth --scale 4
   ```

## 结果展示
通过运行`test.py`，可以生成两张图片进行对比：
- (a) 原图
- (b) 双三次插值（Bicubic）
- (c) SRCNN超分辨率结果

## 贡献
欢迎提交问题和改进建议，共同完善本项目。

## 许可证
本项目遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[SRCNNPyTorch代码及数据集](https://pan.quark.cn/s/6d96b6346417)