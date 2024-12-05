---
layout: post
title: "Kinetics400数据集简介及下载"
date:   2020-12-23
tags: [400,Kinetics,compress,下载,tar]
comments: true
author: admin
---
# Kinetics-400数据集简介及下载

## 数据集简介
Kinetics-400是一个大规模、高质量的YouTube视频网址数据集，其中包含各种以人为本的行动。该数据集包含400个人类动作类，每个动作至少有400个视频剪辑，每个剪辑持续大约10秒，并且取自不同的YouTube视频。这些动作以人类为中心，涵盖广泛的类别，包括演奏乐器等人与物体的交互，以及握手等人与人的交互。

## 数据集下载
该资源文件提供了Kinetics-400数据集的下载链接。下载文件流程如下：

1. 下载label和raw-part中的文件，label里面存储的是标记信息，raw-part里面是视频分块的文件。
2. 在git bash命令行中进入raw-part目录，依次执行以下命令：
   ```bash
   cat compress.tar.gz.* > compress.tar.gz
   tar zxvf compress.tar.gz
   ```
3. 执行完上述命令后，可以得到compress目录，该目录包含了所有视频文件。

该版本的Kinetics数据集是压缩版本，包含了234619个训练集和19761个验证集。视频的尺寸高度保证256个像素，宽度随原始长宽比scale。下载之后，compress目录中有两个子目录：train_256和val_256，您可以直接用这个目录划分train和val两部分。

## 注意事项
- 标注文件中只包含了文件前缀（例如：z2kMVJWpGxU），请您用的时候判断“标记中的前缀”是否和“文件名的前11位字符串”是否一致。
- 这里所有的youtube_id都是11位。

通过以上步骤，您可以顺利下载并使用Kinetics-400数据集进行相关研究和开发工作。

## 下载链接

[Kinetics-400数据集简介及下载分享](https://pan.quark.cn/s/aa5e2ab8b934)