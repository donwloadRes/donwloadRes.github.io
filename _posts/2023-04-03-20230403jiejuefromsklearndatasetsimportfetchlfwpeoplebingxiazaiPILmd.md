---
layout: post
title: "解决from sklearndatasets import fetchlfwpeople并下载PIL"
date:   2020-01-09
tags: [lfw,people,PIL,Pillow,下载]
comments: true
author: admin
---
# 解决from sklearn.datasets import fetch_lfw_people,并下载PIL

本文档旨在帮助用户解决在使用`from sklearn.datasets import fetch_lfw_people`时遇到的问题，并指导如何下载和安装PIL（Python Imaging Library）。

## 问题背景

在使用`fetch_lfw_people`函数时，该函数会尝试从网络上下载一个名为`lfw-funneled.tgz`的压缩包。由于网络问题，下载过程可能会非常缓慢或失败。此外，在某些情况下，用户可能还需要安装PIL库，但在Python 3中，PIL已经被Pillow库所取代。

## 解决方案

### 1. 手动下载数据集

为了避免网络问题，建议用户手动下载`lfw-funneled.tgz`压缩包。下载地址如下：

```
链接：https://pan.baidu.com/s/1IUTYnPXC2L7YLYymXCdj4Q
提取码：53yx
```

下载完成后，将压缩包移动到以下目录：

```
C:\Users\MK\scikit_learn_data\lfw_home
```

其中，`MK`是用户的用户名。

### 2. 安装Pillow库

在Python 3中，PIL库已经被Pillow库所取代。用户可以通过以下命令安装Pillow：

```bash
pip install pillow -i https://pypi.tuna.tsinghua.edu.cn/simple
```

### 3. 验证安装

完成上述步骤后，重新运行代码，检查是否还会出现错误。如果没有错误，说明问题已解决。

## 注意事项

- 如果用户使用的是虚拟环境，除了环境稍有不同外，其他步骤相同。
- 通过命令行工具（如cmd）也可以安装Pillow库。

## 总结

通过手动下载数据集并安装Pillow库，用户可以顺利解决在使用`fetch_lfw_people`时遇到的问题。希望本文档对您有所帮助。

## 下载链接

[解决fromsklearn.datasetsimportfetch_lfw_people分享](https://pan.quark.cn/s/67ce76d33aba)