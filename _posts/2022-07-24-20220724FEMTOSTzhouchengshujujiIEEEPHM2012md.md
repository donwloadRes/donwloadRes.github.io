---
layout: post
title: "FEMTO-ST轴承数据集（IEEE PHM 2012）"
date:   2024-02-24
tags: [数据,轴承,FEMTO,ST,IEEE]
comments: true
author: admin
---
# FEMTO-ST轴承数据集（IEEE PHM 2012）

## 简介
FEMTO-ST轴承数据集是由IEEE可靠性协会和FEMTO-ST研究所联合组织的IEEE PHM 2012数据挑战赛中提供的数据集。该数据集主要用于轴承的剩余寿命预测，包含了多种工况下的振动和温度数据。

## 数据集内容
数据集包含以下主要内容：
1. **振动数据**：由两个相互定位为90°的微型加速度计采集，分别放置在垂直轴和水平轴上，采样频率为25.6kHz。
2. **温度数据**：由电阻温度探测器采集，放置在靠近外轴承环的孔内，采样频率为0.1Hz。

## 实验平台
实验平台（PRONOSTIA）由以下部分组成：
- **旋转部分**：电机功率250W，最高转速2830rpm，保证第二根转轴转速为2000rpm。
- **负载部分**：使用气动千斤顶为轴承提供4000N的动载荷。

## 数据集结构
数据集分为三个文件夹：
1. **训练数据（Learning_set）**：用于模型训练的数据。
2. **测试数据（Test_set）**：比赛时采用的截断数据。
3. **全寿命数据（Full_Test_set）**：测试数据的完整版。

## 数据格式
数据文件为CSV格式，可以使用Excel软件打开查看。

## 使用说明
1. **解压数据**：下载数据后，首先解压文件。
2. **读取数据**：使用提供的读取文件代码（text_2.m）进行数据读取。注意修改代码中的文件路径。

## 参考资料
在使用该数据集时，请引用作者文章（文末）。

## 数据和代码获取
数据和代码可以通过IEEE PHM 2012数据挑战赛的官方渠道获取。

---

通过该数据集，研究人员可以进行轴承剩余寿命预测的相关研究，提升故障预测与健康管理（PHM）技术水平。

## 下载链接

[FEMTO-ST轴承数据集IEEEPHM2012](https://pan.quark.cn/s/71e2b8246897)