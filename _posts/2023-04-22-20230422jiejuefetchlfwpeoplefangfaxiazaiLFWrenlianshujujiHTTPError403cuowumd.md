---
layout: post
title: "解决fetchlfwpeople方法下载LFW人脸数据集HTTPError 403错误"
date:   2021-11-07
tags: [lfw,people,fetch,LFW,下载]
comments: true
author: admin
---
# 解决fetch_lfw_people()方法下载LFW人脸数据集HTTPError 403错误

## 问题描述
在使用`fetch_lfw_people()`方法下载LFW（Labled Faces in the Wild）人脸数据集时，可能会遇到HTTP Error 403: Forbidden错误。

## 原因分析
出现403错误的原因是服务器接收到了客户的请求，但是拒绝回应。

## 解决方案
### Step 1: 手动下载数据集
首先，我们可以通过其他途径手动下载LFW数据集。

### Step 2: 指定数据集路径
运行以下命令，指定数据集的下载路径，并将`download_if_missing`参数设置为`False`，以避免再次尝试从源站点下载数据。
```python
from sklearn.datasets import fetch_lfw_people
lfw_people = fetch_lfw_people(data_home="指定路径", download_if_missing=False)
```

### Step 3: 解压数据集
将手动下载的数据集解压到指定路径下的`lfw_home`文件夹中。

### Step 4: 重命名压缩包
找到名为`lfwfunneled.tgz`的压缩包，并将其重命名为`lfw-funneled.tgz`。

### Step 5: 重新运行命令
最后，再次运行Step 2中的命令，确保数据集正确加载。

通过以上步骤，您可以成功解决`fetch_lfw_people()`方法下载LFW人脸数据集时遇到的HTTPError 403错误。

## 下载链接

[解决fetch_lfw_people方法下载LFW人脸数据集HTTPError403错误](https://pan.quark.cn/s/34cca62a723c)