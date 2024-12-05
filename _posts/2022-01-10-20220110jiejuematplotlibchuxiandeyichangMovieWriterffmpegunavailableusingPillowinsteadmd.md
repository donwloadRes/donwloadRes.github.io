---
layout: post
title: "解决matplotlib出现的异常MovieWriter ffmpeg unavailable using Pillow instead"
date:   2022-06-06
tags: [ffmpeg,matplotlib,python,MovieWriter,unavailable]
comments: true
author: admin
---
# 解决matplotlib出现的异常：MovieWriter ffmpeg unavailable； using Pillow instead

## 简介

本资源文件旨在帮助解决在使用matplotlib库时遇到的异常：`MovieWriter ffmpeg unavailable`。该异常通常发生在尝试将动画保存为视频文件时，由于缺少必要的ffmpeg工具或库。本资源提供了一个解决方案，使用Pillow库作为替代方案来保存动画。

## 解决方案步骤

### 1. 下载ffmpeg到本地

#### 1.1 从网页下载

可以从以下链接下载对应版本的ffmpeg压缩包：
[ffmpeg下载链接](https://github.com/FutaAlice/ffmpeg-static-libs/releases)

#### 1.2 从百度网盘下载

如果网页下载速度较慢，可以选择从百度网盘下载：
链接：https://pan.baidu.com/s/1w1vHU7_gWq-T1y8WWlphdA  
提取码：6f89

### 2. 添加到环境变量

#### 2.1 解压文件

将下载到本地的压缩包进行解压，依次打开文件夹，路径为：`D:\ffmpeg_3.4.2\bin\x64`。

#### 2.2 配置环境变量

复制上述路径，打开系统环境变量，将该路径添加到环境变量中。

### 3. 安装ffmpeg和ffmpeg-python

打开命令行，输入以下命令安装ffmpeg和ffmpeg-python：

```bash
pip install ffmpeg ffmpeg-python
```

或者分开安装这两个包：

```bash
pip install ffmpeg
pip install ffmpeg-python
```

### 4. 检查ffmpeg是否连接成功

在Python代码中添加以下代码，检查ffmpeg是否成功连接：

```python
from matplotlib import animation
print(animation.writers.list())
```

注意：如果输出结果中没有ffmpeg，重新打开PyCharm运行代码可能就会有了。

## 结论

通过以上步骤，您可以成功解决matplotlib中`MovieWriter ffmpeg unavailable`的异常，并使用Pillow库作为替代方案来保存动画。希望本资源对您有所帮助。

## 下载链接

[解决matplotlib出现的异常MovieWriterffmpegunavailableusingPillowinstead](https://pan.quark.cn/s/6f30094a854c)