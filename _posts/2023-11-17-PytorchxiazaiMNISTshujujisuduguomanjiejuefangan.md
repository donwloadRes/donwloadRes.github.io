---
layout: post
title: "Pytorch下载MNIST数据集速度过慢解决方案"
date:   2021-11-02
tags: [MNIST,下载,train,ubyte,gz]
comments: true
author: admin
---
# Pytorch下载MNIST数据集速度过慢解决方案

在使用Pytorch进行深度学习模型训练时，下载MNIST数据集是一个常见的步骤。然而，由于默认下载源在国外，很多用户会遇到下载速度过慢甚至报错的问题。本文将介绍几种解决方案，帮助你快速下载MNIST数据集。

## 解决方案一：手动下载并替换下载源

1. **手动下载数据集**：
   你可以通过浏览器访问MNIST数据集的官方网站，手动下载数据集文件。下载地址如下：
   - `http://yann.lecun.com/exdb/mnist/train-images-idx3-ubyte.gz`
   - `http://yann.lecun.com/exdb/mnist/train-labels-idx1-ubyte.gz`
   - `http://yann.lecun.com/exdb/mnist/t10k-images-idx3-ubyte.gz`
   - `http://yann.lecun.com/exdb/mnist/t10k-labels-idx1-ubyte.gz`

2. **替换下载源**：
   将下载好的数据集文件放置在Pytorch的默认下载路径下，通常是`/mnist/`目录。然后修改代码中的`download`参数为`False`，让程序直接读取本地数据集。

   ```python
   train_data = torchvision.datasets.MNIST(
       root='/mnist/',
       train=True,
       transform=torchvision.transforms.ToTensor(),
       download=False
   )
   ```

## 解决方案二：修改源码中的下载源

1. **找到源码中的下载部分**：
   打开Pytorch源码，找到MNIST数据集的下载部分，通常在`torchvision.datasets.MNIST`类中。

2. **修改下载源**：
   将下载源修改为本地路径，例如：
   ```python
   resources = [
       ("file:///path/to/local/train-images-idx3-ubyte.gz", "f68b3c2dcbeaaa9fbdd348bbdeb94873"),
       ("file:///path/to/local/train-labels-idx1-ubyte.gz", "d53e105ee54ea40749a09fcbcd1e9432"),
       ("file:///path/to/local/t10k-images-idx3-ubyte.gz", "9fb629c4189551a2d022fa330f9573f3"),
       ("file:///path/to/local/t10k-labels-idx1-ubyte.gz", "ec29112dd5afa0611ce80d1b7f02629c")
   ]
   ```

3. **重新运行程序**：
   修改完成后，重新运行程序，程序将从本地路径快速加载数据集。

## 解决方案三：使用已处理好的数据集

如果你不想手动下载和处理数据集，可以直接使用已经处理好的MNIST数据集文件。将这些文件放置在程序的下载路径下，然后将`download`参数设置为`False`。

```python
train_data = torchvision.datasets.MNIST(
    root='/mnist/',
    train=True,
    transform=torchvision.transforms.ToTensor(),
    download=False
)
```

## 总结

通过以上几种方法，你可以有效解决Pytorch下载MNIST数据集速度过慢的问题。选择适合你的方法，快速开始你的深度学习项目吧！

## 下载链接

[Pytorch下载MNIST数据集速度过慢解决方案](https://pan.quark.cn/s/198df9cd2242)