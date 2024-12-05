---
layout: post
title: "解决sklearndatasetsfetch20newsgroups下载报错问题"
date:   2020-02-25
tags: [下载,20newsgroups,path,报错,fetch]
comments: true
author: admin
---
# 解决sklearn.datasets.fetch_20newsgroups下载报错问题

在使用Python的机器学习库scikit-learn（sklearn）时，`fetch_20newsgroups`函数用于下载和加载20个新闻组文本分类数据集。然而，有时在下载过程中可能会遇到报错问题，导致数据集无法正常下载。本文将介绍如何解决这一问题。

## 问题描述

在尝试下载20newsgroups数据集时，可能会遇到以下错误：

```
HTTPError: HTTP Error 403: Forbidden
```

或者下载速度极慢，导致无法正常完成下载。

## 解决方案

### 1. 手动下载数据集

首先，手动下载数据集文件。你可以从以下链接下载：

```
链接：https://pan.baidu.com/s/1a0vQ4OIxpvKtc_rxLVKxvQ
提取码：40m9
```

下载完成后，将文件名修改为：

```
20newsbydate.tar.gz
```

### 2. 将文件放置到指定目录

将下载好的压缩包放置到以下目录：

```
C:\Users\(你的user_name)\scikit_learn_data\20news_home
```

如果目录不存在，请手动创建。

### 3. 修改Python代码

打开Python安装目录下的`_twenty_newsgroups.py`文件，找到`download_20newsgroups`函数。在该函数中，找到以下代码并注释掉：

```python
# logger.info("Downloading dataset from %s (14 MB)", ARCHIVE.url)
```

然后添加以下代码：

```python
archive_path = r'C:\Users\lenovo\scikit_learn_data\20newsbydate.tar.gz'
logger.debug("Decompressing %s", archive_path)
tarfile.open(archive_path, "r:gz").extractall(path=target_dir)
os.remove(archive_path)
```

### 4. 重新运行程序

保存修改后的文件，并重新运行你的程序。此时，程序将不再尝试从网络下载数据集，而是直接使用你手动下载并放置在指定目录中的数据集文件。

## 总结

通过手动下载数据集并修改Python代码，可以有效解决`fetch_20newsgroups`函数在下载过程中遇到的报错问题。希望本文对你有所帮助，祝你在机器学习的学习和实践中取得进步！

## 下载链接

[解决sklearn.datasets.fetch_20newsgroups下载报错问题分享](https://pan.quark.cn/s/7ed3f7949eb8)