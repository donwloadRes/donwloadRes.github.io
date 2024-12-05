---
layout: post
title: "Mac OS下解决matplotlib中文显示问题"
date:   2021-09-29
tags: [matplotlib,中文,Python,Mac,OS]
comments: true
author: admin
---
# Mac OS下解决matplotlib中文显示问题

## 简介

在使用Python的matplotlib库进行数据可视化时，中文显示问题是一个常见的问题。特别是在Mac OS系统下，由于默认字体不支持中文，常常会导致中文显示为方块或乱码。本资源文件提供了一个解决方案，帮助用户在Mac OS系统下正确显示matplotlib绘图中的中文。

## 解决方案步骤

### Step 1: 下载 SimHei 字体

为了在matplotlib中正确显示中文，首先需要下载SimHei字体文件。SimHei是一种支持中文显示的字体，可以确保在绘图中正确显示中文字符。

### Step 2: 找出存放字体的ttf文件夹路径

在Mac OS系统中，matplotlib的字体文件通常存放在特定的文件夹中。可以通过以下Python代码找到该路径：

```python
import matplotlib
print(matplotlib.get_data_path() + '/fonts/ttf')
```

### Step 3: 将SimHei.ttf复制到ttf文件夹下

在终端中运行以下命令，打开ttf文件夹：

```bash
open /Library/Frameworks/Python.framework/Versions/3.12/lib/python3.12/site-packages/matplotlib/mpl-data/fonts/ttf
```

然后将下载的SimHei.ttf文件复制到该文件夹中。

### Step 4: 用vim编辑matplotlibrc文件

通过以下Python代码找到matplotlibrc文件的路径：

```python
import matplotlib
print(matplotlib.matplotlib_fname())
```

在终端中使用vim编辑该文件：

```bash
vim /Library/Frameworks/Python.framework/Versions/3.12/lib/python3.12/site-packages/matplotlib/mpl-data/matplotlibrc
```

在文件中进行以下修改：

1. 去掉`#font.family: sans-serif`这一行开头的`#`。
2. 去掉`#font.sans-serif: DejaVu Sans, Bitstream Vera Sans, Computer Modern Sans Serif, Lucida Grande, Verdana, Geneva, Lucid, Arial, Helvetica, Avant Garde, sans-serif`这一行开头的`#`，并在`font.sans-serif:`后插入`SimHei`（注意有逗号）。
3. 去掉`#axes.unicode_minus: True`开头的`#`，并将`True`改为`False`。

### Step 5: 删除matplotlib文件夹（内有字体缓存）

运行以下Python代码找到matplotlib文件夹的路径：

```python
import matplotlib
print(matplotlib.get_cachedir())
```

在终端中运行以下命令删除该文件夹：

```bash
rm -rf /Users/apple/.matplotlib
```

### Step 6: 测试能否显示中文

运行以下Python代码测试是否能正确显示中文：

```python
import matplotlib.pyplot as plt
plt.plot([1, 2, 3], [2, 3, 4])
plt.title("测试能否显示中文")
plt.show()
```

如果中文能够正确显示，说明配置成功。

## 总结

通过以上步骤，您可以在Mac OS系统下解决matplotlib中文显示问题，确保在绘图中正确显示中文字符。希望本资源文件对您有所帮助！

## 下载链接

[MacOS下解决matplotlib中文显示问题](https://pan.quark.cn/s/798ab5088d2a)