---
layout: post
title: "从零开始利用YOLOv5训练自己的数据集
date   20220505
tags YOLOv5训练文件yaml
comments true
author admin

 从零开始利用YOLOv5训练自己的数据集

本资源文件提供了从零开始利用YOLOv5训练自己的数据集的详细教程包含coco128数据集和YOLOv5权重文件的国内下载链接更新于2020年7月28日

 内容概述

1 准备工作
    下载YOLOv5项目
    下载官方例子的数据集
    安装项目需求

2 训练自定义数据
    创建Dataset的yaml文件
    创建标签
    组织目录
    选择模型
    训练模型

3 可视化
    查看训练图像标签和增强效果
    查看每代的预测结果
    查看训练的损失和性能指标

4 补充
    解决常见问题
    更新YOLOv5文件

 使用步骤

 1 准备工作

首先克隆YOLOv5项目并下载官方例子的数据集

bash
git clone httpsgithubcomultralyticsyolov5
python3 c from yolov5utilsgoogleutils import gdrivedownload gdrivedownload1noKgR81BJtqk75b00eAjdv03qVCQn2f coco128zip"
date:   2022-05-05
tags: [YOLOv5,训练,--,文件,yaml]
comments: true
author: admin
---
# 从零开始：利用YOLOv5训练自己的数据集

本资源文件提供了从零开始利用YOLOv5训练自己的数据集的详细教程，包含coco128数据集和YOLOv5权重文件的国内下载链接。更新于2020年7月28日。

## 内容概述

1. **准备工作**
   - 下载YOLOv5项目
   - 下载官方例子的数据集
   - 安装项目需求

2. **训练自定义数据**
   - 创建Dataset的yaml文件
   - 创建标签
   - 组织目录
   - 选择模型
   - 训练模型

3. **可视化**
   - 查看训练图像、标签和增强效果
   - 查看每代的预测结果
   - 查看训练的损失和性能指标

4. **补充**
   - 解决常见问题
   - 更新YOLOv5文件

## 使用步骤

### 1. 准备工作

首先，克隆YOLOv5项目并下载官方例子的数据集：

```bash
git clone https://github.com/ultralytics/yolov5
python3 -c "from yolov5.utils.google_utils import gdrive_download; gdrive_download('1n_oKgR81BJtqk75b00eAjdv03qVCQn2f', 'coco128.zip')"
cd yolov5
pip install -U -r requirements.txt
```

### 2. 训练自定义数据

#### 2.1 创建Dataset的yaml文件

根据官方的coco128.yaml文件，修改训练图像目录的路径、验证图像路径、类数和类列表名称。

#### 2.2 创建标签

使用Labelbox和CVAT工具进行图像标记，将标签导出为darknet格式，每张图像一个txt文件。

#### 2.3 组织目录

将数据集放在YOLOv5项目旁边，包含images和labels两个文件夹。

#### 2.4 选择模型

从models文件夹中选择模型，如yolov5s.yaml，更新其中参数以适应自定义数据集。

#### 2.5 训练

使用以下命令开始训练：

```bash
python train.py --img 640 --batch 16 --epochs 5 --data /data/coco128.yaml --cfg /models/yolov5s.yaml --weights ''
```

### 3. 可视化

训练过程中，可以通过查看train*.jpg图像来查看训练图像、标签和增强效果。每代训练完成后，可以通过test_batch0_gt.jpg查看标签，通过test_batch0_pred.jpg查看预测结果。训练的损失和性能指标保存在tensorboard和results.txt日志文件中。

### 4. 补充

解决常见问题，如权重文件过期、CUDA out of memory等。定期更新YOLOv5文件以获取最新功能和修复。

## 注意事项

- 确保显卡性能足够，否则适当调整batch-size和img-size。
- 定期更新YOLOv5文件以获取最新功能和修复。

通过本教程，您可以从零开始，利用YOLOv5训练自己的数据集，实现目标检测任务。

## 下载链接

[从零开始利用YOLOv5训练自己的数据集](https://pan.quark.cn/s/8d7b88d6f0c9)