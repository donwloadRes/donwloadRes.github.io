---
layout: post
title: "东南大学齿轮箱数据集"
date:   2024-11-02
tags: [数据,故障,fault,齿轮箱,文件]
comments: true
author: admin
---
# 东南大学齿轮箱数据集

## 简介

本资源文件提供了东南大学齿轮箱数据集，该数据集主要用于机器学习和故障诊断研究。数据集包含了多种齿轮箱的振动信号数据，涵盖了不同类型的故障和正常运行状态。

## 数据集组成

该数据集主要分为轴承数据集和齿轮箱数据集，每个故障类型均对应两种工况（转速20Hz（1200rpm）-负载0V(0Nm) 和转速30Hz(1800rpm)-负载2V(7.32Nm)），分别对应着gearset和bearingset文件夹。

### 轴承数据集（5种类型）
- 滚子故障（Ball fault）
- 内圈故障（Inner ring fault）
- 外圈故障（Outer ring fault）
- 复合故障（Combination fault on both inner ring and outer ring）
- 正常运行（Health working state）

### 齿轮数据集（5种类型）
- 缺损（Chipped tooth，齿轮上有裂纹）
- 断齿（Missing tooth）
- 在齿轮根部的裂纹（Root fault）
- 齿面磨损（Surface fault）
- 正常运行（Health working state）

## 数据说明

- 每个故障类型的一种工况单独存储在一个CSV文件中，文件名字清楚的标识了类型和工况。
- 每个CSV文件均有一些配置信息，这些配置信息作者没有进行详细描述，欢迎指导的朋友进行评论探讨。
- 一共有8个通道信号，对应着数据的8列，具体如下：
  - 第1列：电机振动信号
  - 第2、3、4列：分别对应行星齿轮x、y和z三个方向的振动信号
  - 第5列：对应着电机扭矩
  - 第6、7、8列：分别对应着减速器x、y和z三个方向的振动信号
- 采样频率是5120Hz。
- 该数据集仅可以用来做智能诊断和迁移学习的相关内容，并未提供相关轴承型号、故障齿轮安装位置等。

## 数据读取

为了方便大家操作，本人编写了相关matlab代码，可实现所有数据的自动读取，具体文件见附件。同时，提供了最终提取数据的结果（附件的data.mat文件），data.mat中存放着所有类型的数据，每个数据均有8列，对应着东南大学提供的excel。

## 附件

- 所有原始数据集（gearset文件夹和bearingset文件夹）
- 自动读取CSV文件的matlab代码文件（main.m可执行脚本，sort_nat.m函数）
- 已保存数据文件(data.mat)
- 相关参考资料，包括与这个数据集相关的SCI论文和学位论文，供大家参考

## 使用说明

该数据集适用于机器学习和故障诊断研究，特别是针对齿轮箱和轴承的故障检测与诊断。用户可以通过提供的matlab代码自动读取和处理数据，进行进一步的分析和模型训练。

## 参考资料

- 相关SCI论文和学位论文，供大家参考

## 注意事项

- 数据集仅供学术研究使用，不得用于商业用途。
- 数据集的配置信息未详细描述，使用时需自行探索和验证。

---

希望本数据集能为您的研究提供帮助！

## 下载链接

[东南大学齿轮箱数据集分享](https://pan.quark.cn/s/0f6e6250b451)