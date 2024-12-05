---
layout: post
title: "FasterRCNNpytorch在VGGResNet和FPN基础中实现"
date:   2020-07-10
tags: [FasterRCNN,sh,sm,FPN,make]
comments: true
author: admin
---
# FasterRCNN-pytorch：在VGG、ResNet和FPN基础中实现

## 项目描述

本仓库提供了一个基于PyTorch实现的FasterRCNN模型，支持在VGG、ResNet和FPN（Feature Pyramid Network）三种不同的骨干网络中进行实现。该实现参考了rbg的FasterRCNN代码，并在VOC2017数据集上进行了训练和测试。

## 模型表现

在VOC2017数据集上，模型的表现如下：

- **VGG16**：0.7061
- **ResNet101**：0.754

## 使用说明

### 1. 环境准备

在运行模型之前，您需要进行以下准备工作：

1. 进入`lib`目录：
   ```bash
   cd ./lib
   ```

2. 修改`make.sh`和`setup.py`中的`gpu_id`设置。具体来说，您需要在`make.sh`的第5、12和19行以及`setup.py`的第143行中修改参数设置，其中包含关键字“-arch=”。您需要根据您的GPU型号选择适当的体系结构，参考下表：

   | GPU型号               | 架构    |
   |-----------------------|---------|
   | TitanX（麦克斯韦/帕斯卡） | sm_52   |
   | GTX 960M              | sm_50   |
   | GTX 1080（钛）        | sm_61   |
   | 网格K520（AWS g2.2xlarge） | sm_30   |

### 2. 编译与运行

完成上述设置后，您可以运行以下命令进行编译和运行：

```bash
sh make.sh
```

## 注意事项

- 请确保您的GPU型号与所选的架构匹配，否则可能会导致运行失败。
- 本项目依赖于PyTorch和相关CUDA库，请确保您的环境已正确配置。

## 贡献

欢迎大家提出问题和改进建议，如果您有任何疑问或建议，请在GitHub上提交Issue或Pull Request。

## 许可证

本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 下载链接

[FasterRCNN-pytorch在VGGResNet和FPN基础中实现](https://pan.quark.cn/s/83b314ec4f0e)