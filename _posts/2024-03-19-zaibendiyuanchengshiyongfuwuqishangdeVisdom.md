---
layout: post
title: "在本地远程使用服务器上的Visdom"
date:   2021-09-06
tags: [Visdom,服务器,可视化,visdom,本地]
comments: true
author: admin
---
# 在本地远程使用服务器上的Visdom

## 简介

本文档详细介绍了如何在本地远程使用服务器上的Visdom进行数据可视化。Visdom是Facebook开发的一款可视化工具，特别适用于PyTorch环境中的数据监控和可视化。通过本文档，您将学习如何在服务器上安装和配置Visdom，并在本地浏览器中实时查看服务器上的可视化结果。

## 主要内容

### 1. Visdom简介

Visdom是一个基于Web的可视化工具，主要用于深度学习模型的训练过程中实时监控和可视化数据，如损失值、准确率等。它支持多种图表类型，并且可以轻松集成到PyTorch项目中。

### 2. 在服务器上安装Visdom

首先，您需要在服务器上安装Visdom。使用以下命令进行安装：

```bash
pip install visdom
```

### 3. 启动Visdom

安装完成后，您可以通过以下命令启动Visdom服务器：

```bash
python -m visdom.server
```

默认情况下，Visdom服务器会在8097端口上运行。

### 4. 可能遇到的问题及解决方法

#### 4.1 启动卡住问题

在启动Visdom时，可能会遇到启动卡住的情况。这通常是因为需要下载相应的脚本，但由于网络问题无法下载。解决方法如下：

1. 找到Visdom的安装位置：

    ```python
    import os
    import visdom
    print(os.path.dirname(visdom.__file__))
    ```

2. 修改`server.py`文件，注释掉`download_scripts()`函数：

    ```python
    def download_scripts_and_run():
        # download_scripts()  # 注释掉这一句
        main()
    ```

3. 手动下载Visdom所需的`static`包，并将其解压到Visdom的安装目录中。

### 5. 在本地浏览器中访问Visdom

在服务器上成功启动Visdom后，您可以在本地浏览器中输入以下地址访问：

```
http://服务器IP:8097
```

### 6. 额外问题：蓝屏

在使用Visdom时，可能会遇到浏览器蓝屏的问题。这通常是因为`static`文件夹中的文件不全。解决方法是重新下载完整的`static`文件夹并替换。

## 总结

通过本文档，您已经了解了如何在本地远程使用服务器上的Visdom进行数据可视化。希望这些步骤能帮助您顺利完成配置，并在深度学习项目中充分利用Visdom的强大功能。

## 下载链接

[在本地远程使用服务器上的Visdom分享](https://pan.quark.cn/s/fe054715724d)