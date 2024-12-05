---
layout: post
title: "在matplotlib中使用中文字体"
date:   2021-08-30
tags: [font,matplotlib,manager,中文字体,plt]
comments: true
author: admin
---
# 在matplotlib中使用中文字体

## 简介

本资源文件旨在帮助用户在Kaggle环境中使用matplotlib绘图时，解决中文字符显示乱码的问题。通过上传自定义的中文字体文件，并配置matplotlib使用该字体，用户可以在图表中正常显示中文字符。

## 使用方法

### 1. 上传字体文件

首先，在Kaggle上上传你自己的中文字体文件。你可以从提供的资源链接中下载字体文件，并将其上传到Kaggle的Notebook环境中。

### 2. 设置matplotlib的字体

在Notebook中，使用以下代码设置matplotlib的字体为上传的中文字体：

```python
import matplotlib.font_manager as font_manager

myfont = font_manager.FontProperties(fname="/input/droid-sans-fallbackttf/DroidSansFallback.ttf")
plt.rcParams['axes.unicode_minus'] = False  # 用来正常显示正负号
```

### 3. 局部使用

如果你只想在特定的图表中使用中文字体，可以使用以下代码：

```python
import pandas as pd
import matplotlib.pyplot as plt

pd.DataFrame({'中分': stroke_1, '正常': stroke_0}).plot(kind='bar')
plt.title('各个性别中分情况', fontproperties=myfont)
plt.xlabel('性别', fontproperties=myfont)
plt.ylabel('中分人数', fontproperties=myfont)
```

### 4. 全局使用

如果你想在整个Notebook中全局使用中文字体，可以使用以下代码：

```python
import matplotlib.font_manager as font_manager

font_dirs = ['/my/custom/font/dir']
font_files = font_manager.findSystemFonts(fontpaths=font_dirs)
font_list = font_manager.createFontList(font_files)
font_manager.fontManager.ttflist.extend(font_list)

plt.rcParams['font.family'] = 'My Custom Font'
```

## 注意事项

- 确保上传的字体文件路径正确。
- 如果你在其他环境中使用matplotlib，可能需要根据实际情况调整字体路径。

通过以上步骤，你可以在Kaggle的Notebook中顺利使用matplotlib绘制包含中文字符的图表。

## 下载链接

[在matplotlib中使用中文字体分享](https://pan.quark.cn/s/5fe7ad7bf0d7)