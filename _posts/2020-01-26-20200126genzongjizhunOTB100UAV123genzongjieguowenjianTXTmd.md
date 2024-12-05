---
layout: post
title: "跟踪基准OTB100、UAV123跟踪结果文件TXT"
date:   2024-02-21
tags: [文件,结果,跟踪,SiamRPN,UAV123]
comments: true
author: admin
---
# 跟踪基准OTB100、UAV123跟踪结果文件TXT

## 简介

本仓库提供了一系列目标跟踪算法的跟踪结果文件，这些结果文件是在OTB100和UAV123基准测试数据集上进行测试后生成的。所有结果文件均为TXT格式，方便用户直接下载和使用。

## 文件来源

所有跟踪结果文件均使用pysot-toolkit进行测试，并在硬件配置为Tesla P100 GPU的环境下完成。代码、模型和超参数均使用原作者已公布的源码，未作改动。

## 包含的跟踪器

以下是本仓库中包含的跟踪器及其来源：

### OTB100跟踪结果
- CFNet
- CGACD
- DaSiamRPN
- DeepSRDCF
- DROL-RPN
- fDSST
- GradNet
- MDNet
- Ocean
- SAOT
- SiamAttn
- SiamBAN
- SiamCAR
- SiamDW
- SiamFC
- SiamFC++_alex
- SiamFC++_googlenet
- SiamGAT
- SiamRPN
- SiamRPN++
- SRDCF
- Staple

### UAV123跟踪结果
- CGACD
- Ocean
- SiamAttn
- SiamBAN
- SiamCAR
- SiamDW
- SiamGAT
- SiamRPN
- SiamRPN++

## 使用说明

1. 下载所需的跟踪结果文件。
2. 使用pysot-toolkit或其他相关工具加载和分析结果文件。
3. 根据需要进行进一步的实验和研究。

## 注意事项

- 所有结果文件均为自测结果，与文献中的原始结果可能存在差异。
- 部分跟踪器在UAV123数据集上的自测结果与文献中的原始结果差距较大，原因尚不明确。

## 贡献

欢迎提交新的跟踪结果文件或改进现有文件。请确保所有提交的文件符合本仓库的标准和格式。

## 许可证

本仓库中的所有内容遵循CC 4.0 BY-SA版权协议。转载请附上原文出处链接和本声明。

## 下载链接

[跟踪基准OTB100UAV123跟踪结果文件TXT](https://pan.quark.cn/s/ddb4e5dc4168)