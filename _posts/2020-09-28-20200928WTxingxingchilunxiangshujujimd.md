---
layout: post
title: "WT行星齿轮箱数据集"
date:   2021-12-16
tags: [齿轮箱,数据,齿轮,行星,WT]
comments: true
author: admin
---
# WT-行星齿轮箱数据集

## 简介

WT-行星齿轮箱数据集是由北京工业大学刘东东、崔玲丽和北京交通大学程卫东在综述文献[1]中公开的数据集。该数据集考虑了齿轮箱的安装和拆卸因素，包含了不同转速下的齿轮健康、齿轮损坏、齿面磨损、齿根断裂和缺齿五种运行状态。这些数据可用于旋转机械的传统故障诊断、智能诊断和迁移学习研究。

## 数据集内容

1. **试验台组成**：
   - 电机
   - 行星齿轮箱
   - 固定轴齿轮箱
   - 加载装置

2. **行星齿轮箱结构**：
   - 四个行星齿轮绕一个太阳齿轮旋转
   - 模拟了太阳齿轮的五种工作状态：齿轮健康、齿轮损坏、齿面磨损、齿根断裂和缺齿

3. **数据集详细信息**：
   - 包含转速为20Hz、25Hz、30Hz、35Hz、40Hz、45Hz、50Hz、55Hz的太阳齿轮的五种工作状态数据
   - 数据包括X、Y轴的振动数据和转速数据
   - 采样频率为48KHz，每种转速下太阳轮每种工作状态的数据采集了5分钟
   - 振动数据采用Sinocera CA-YD-1181加速度计采集，编码器捕获速度脉冲

## 使用说明

1. **数据格式**：
   - 所有数据均为mat格式

2. **引用要求**：
   - 使用该数据集时，请引用参考文献[1]，以促进知识传播

## 参考文献

[1] Dongdong Liu, Lingli Cui, and Weidong Cheng. A review on deep learning in planetary gearbox health state recognition: Methods, applications, and dataset publication. Measurement Science and Technology, DOI 10.1088/1361-6501/acf390.

## 数据集下载

请访问相关链接下载数据集。

---

**注意**：本README.md文件为示例文件，实际使用时请根据具体情况进行调整。

## 下载链接

[WT-行星齿轮箱数据集分享](https://pan.quark.cn/s/122fdc114d96)