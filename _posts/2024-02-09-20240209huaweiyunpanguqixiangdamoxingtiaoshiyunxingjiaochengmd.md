---
layout: post
title: "华为云盘古气象大模型调试运行教程"
date:   2023-03-16
tags: [模型,教程,py,下载,运行]
comments: true
author: admin
---
# 华为云盘古气象大模型调试运行教程

本仓库提供了一个详细的教程，帮助初学者了解和运行华为云盘古气象（Pangu-Weather）大模型。教程内容涵盖了模型的基本介绍、运行环境准备、模型文件下载、调试运行步骤以及结果验证等。

## 内容概述

1. **模型概述**
   - 介绍盘古气象大模型的背景和应用领域。
   - 详细说明模型的架构和功能。

2. **运行环境准备**
   - 推荐使用Anaconda管理Python环境。
   - 注册并使用Climate Data Store (CDS) API。

3. **模型文件下载**
   - 提供模型文件的下载链接和存储方式。

4. **调试运行步骤**
   - 详细说明如何克隆项目代码、创建虚拟环境、安装依赖包。
   - 指导如何下载初始场数据、进行模型预测和结果可视化。

5. **结果验证**
   - 介绍如何对盘古气象模型以及ECMWF、GFS的预报效果进行检验对比。
   - 提供数据来源和验证方法。

## 使用说明

1. **克隆仓库**
   ```bash
   git clone https://github.com/HaxyMoly/Pangu-Weather-ReadyToGo.git
   cd Pangu-Weather-ReadyToGo
   ```

2. **创建虚拟环境**
   ```bash
   conda create -n pgwdome -y python=3.10
   conda activate pgwdome
   ```

3. **安装依赖包**
   - CPU环境：
     ```bash
     pip install -r requirements_cpu.txt
     ```
   - GPU环境：
     ```bash
     pip install -r requirements_gpu.txt
     ```

4. **下载模型文件**
   - 创建一个名为`models`的文件夹，并将下载的模型文件放入其中。

5. **运行模型**
   - 修改`data_prepare.py`中的初始场时间。
   - 执行`data_prepare.py`下载初始场数据并转换为npy格式。
   - 根据需要修改`inference.py`中的变量。
   - 执行`inference.py`进行预测。
   - 执行`forecast_decode.py`将npy转换回NetCDF格式。

6. **结果可视化**
   - 进入预测文件路径，使用`ncvue`工具可视化预测结果。

## 注意事项

- 确保Python环境配置正确。
- 下载模型文件时注意存储路径。
- 运行过程中如遇到问题，请参考教程中的常见问题解答部分。

## 贡献

欢迎提交问题和改进建议，帮助我们完善本教程。

## 许可证

本教程遵循CC 4.0 BY-SA版权协议。

## 下载链接

[华为云盘古气象大模型调试运行教程](https://pan.quark.cn/s/e40b31be86ad)