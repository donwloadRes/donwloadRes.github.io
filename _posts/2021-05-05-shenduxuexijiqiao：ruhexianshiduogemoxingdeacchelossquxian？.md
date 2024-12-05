---
layout: post
title: "深度学习技巧：如何显示多个模型的acc和loss曲线？"
date:   2022-08-02
tags: [模型,TensorBoard,曲线,plt,csv]
comments: true
author: admin
---
# 深度学习技巧：如何显示多个模型的acc和loss曲线？

## 简介

在深度学习模型的训练过程中，准确率（Accuracy）和损失（Loss）曲线是评估模型性能的重要指标。通过这些曲线，我们可以直观地观察模型在训练过程中的表现，从而判断模型是否过拟合或欠拟合。本文将介绍如何在TensorBoard中同时显示多个模型的准确率和损失曲线，以便于对比分析不同模型的训练效果。

## 方法

### 1. 目录结构

为了在TensorBoard中同时显示多个模型的结果，首先需要确保你的目录结构如下：

```
- logs
  -- 1
    --- events.out.tfevents.1
  -- 2
    --- events.out.tfevents.2
  -- 3
    --- events.out.tfevents.3
```

每个子文件夹下只保存一个tfevents文件。

### 2. 启动TensorBoard

在命令行中进入`logs`文件夹，然后执行以下命令启动TensorBoard：

```bash
tensorboard --logdir=/
```

启动后，打开浏览器并访问TensorBoard的地址（通常为`http://localhost:6006`），你将看到多个模型的准确率和损失曲线。

### 3. 自定义绘图

TensorBoard虽然功能强大，但有时无法满足特定的绘图需求。为了在论文或其他文档中使用，我们可以手动绘制这些曲线。

#### 3.1 获取数据

首先，从TensorBoard中下载你想要的数据。确保你已经选中想要保存的数据，然后点击“CSV”按钮，将数据保存为CSV文件。

#### 3.2 绘制曲线

使用Python的`pandas`和`matplotlib`库，可以轻松绘制这些曲线。以下是一个简单的示例代码：

```python
import pandas as pd
import matplotlib.pyplot as plt

# 读取CSV文件
net2 = pd.read_csv('run_2-tag-loss.csv', usecols=['Step', 'Value'])
plt.plot(net2.Step, net2.Value, lw=1.5, label='Net-2', color='pink')

net3 = pd.read_csv('run_3-tag-loss.csv', usecols=['Step', 'Value'])
plt.plot(net3.Step, net3.Value, lw=1.5, label='Net-3', color='green')

net4 = pd.read_csv('run_4-tag-loss.csv', usecols=['Step', 'Value'])
plt.plot(net4.Step, net4.Value, lw=1.5, label='Net-4', color='yellow')

# 添加图例
plt.legend(loc=0)
plt.show()
```

执行上述代码后，你将看到多个模型的损失曲线在同一图中显示。

## 总结

通过上述方法，你可以在TensorBoard中同时显示多个模型的准确率和损失曲线，并根据需要自定义绘图。这有助于更直观地对比不同模型的训练效果，从而优化模型性能。

## 下载链接

[深度学习技巧如何显示多个模型的acc和loss曲线分享](https://pan.quark.cn/s/f5b312227180)