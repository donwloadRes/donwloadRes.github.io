---
layout: post
title: "Eigen库下载安装并配置到VS"
date:   2021-04-21
tags: [Eigen,头文件,VS,官网,include]
comments: true
author: admin
---
# Eigen库下载安装并配置到VS

## 简介
Eigen是一个用于线性代数的高效C++库，适用于多种矩阵操作和数值分析。本文介绍了如何在无法访问官网的情况下，通过GitHub和百度云盘下载Eigen，接着在VS2010中进行安装和配置，并提供了简单的测试步骤。

## 下载
1. **Eigen官网下载**：（不知为什么，我电脑一只打不开官网）
2. **GitHub上下载**
3. **百度云盘下载**：提取码：d0jk

## 安装
1. 将压缩包解压到本地随意一个盘中。
2. 打开VS，我安装的是VS2010，新建一个工程，鼠标放到工程名上点击右键，选择属性。
3. 配置包含目录，确保编译器能够找到Eigen的头文件。

## 测试
```cpp
#include <iostream>
#include <Eigen/SVD>
#include <Eigen/Core>
using namespace std;

// 利用Eigen库，采用SVD分解的方法求解矩阵伪逆，默认误差er为0
Eigen::MatrixXd pinv_eigen_based(Eigen::MatrixXd & origin, const float er = 0) {
    // 进行svd分解
    // ...
}
```

## 注意事项
- Eigen是一个纯头文件的库，因此你不需要担心库文件的链接问题，只需确保你的编译器能够找到Eigen的头文件即可。
- 如果项目需要链接到Eigen的库文件，尽管通常Eigen是纯头文件的，你可以在“链接器”->“输入”->“附加依赖项”中添加相应的库文件名。

## 参考
本文参考了CSDN博客文章，详细介绍了Eigen库的下载、安装和配置过程。

## 下载链接

[Eigen库下载安装并配置到VS分享](https://pan.quark.cn/s/90734ca4b772)