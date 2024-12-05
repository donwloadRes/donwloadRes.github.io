---
layout: post
title: "行人属性数据集PA100K下载与解析指南"
date:   2024-10-20
tags: [txt,key,name,images,label]
comments: true
author: admin
---
# 行人属性数据集PA100K下载与解析指南

## 简介
行人属性数据集PA100K是迄今为止用于行人属性识别的最大数据集，包含从室外监控摄像头收集的总共100000张行人图像，每张图像都有26个常用属性。本资源文件提供了PA100K数据集的下载链接以及详细的解析方法。

## 数据集介绍
- **数据集大小**：100000张行人图像
- **属性数量**：每张图像包含26个常用属性
- **数据集划分**：随机分为80000个训练图像、10000个验证图像和10000个测试图像

## 下载方法
数据集已上传至百度云盘，请按照需求下载。

## 数据解析
下载数据后，发现标注信息是`annotation.mat`的标注文件，不好直观感受其标注信息。下面将`annotation.mat`解析处理，转化为我们熟悉的格式。

### 解析代码
```python
import pandas as pd
import scipy
from scipy import io

data = scipy.io.loadmat('annotation.mat')

def mat2txt(data, key):
    subdata = data[key]
    dfdata = pd.DataFrame(subdata)
    dfdata.to_csv("%s.txt" % key, index=False)

if __name__ == "__main__":
    data = scipy.io.loadmat("annotation.mat")
    key_list = ["attributes", "test_images_name", "test_label", "train_images_name", "train_label", "val_images_name", "val_label"]
    for key in key_list:
        mat2txt(data, key)
```

运行代码后，`annotation.mat`文件将转化为几个`.txt`文件，如下图所示：

## 文件内容
- `attributes.txt`
- `test_images_name.txt`
- `test_label.txt`
- `train_images_name.txt`
- `train_label.txt`
- `val_images_name.txt`
- `val_label.txt`

## 使用建议
有了这些数据，你就可以进行行人属性识别研究了。如何训练行人属性模型，请参考相关教程。

## 其他资源
- 推荐一个很好的行人属性训练工程
- 另外一个公开数据集介绍PEAT

## 技术交流
如需技术交流，请留言或微信联系。

## 下载链接

[行人属性数据集PA100K下载与解析指南分享](https://pan.quark.cn/s/0bb56890a833)