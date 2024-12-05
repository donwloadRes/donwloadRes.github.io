---
layout: post
title: "Jupyter Notebook中绘制词云图教程"
date:   2023-03-10
tags: [云图,Jupyter,Notebook,教程,字体]
comments: true
author: admin
---
# Jupyter Notebook中绘制词云图教程

本资源文件提供了一个详细的教程，指导如何在Jupyter Notebook中绘制词云图。教程涵盖了从安装必要的库到生成词云图的完整步骤，适合初学者和有一定基础的用户。

## 内容概述

1. **安装必要的库**：教程首先介绍了如何安装生成词云图所需的Python库，包括`wordcloud`和`matplotlib`。

2. **下载字体文件**：为了确保词云图能够正确显示中文字符，教程提供了下载华文行楷字体的链接，并指导用户如何将字体文件上传到Jupyter Notebook的同级目录下。

3. **生成词云图**：教程详细讲解了如何在Jupyter Notebook中导入库、读取字体文件、指定词语列表，并通过代码生成词云图。

4. **解决常见问题**：针对在生成词云图过程中可能遇到的错误，如“Only supported for TrueType fonts”，教程提供了相应的解决方法，包括升级词云包和相关依赖。

## 使用步骤

1. **安装库**：
   - 关闭所有Jupyter Notebook进程。
   - 打开Anaconda Powershell Prompt命令行窗口。
   - 输入以下命令进行库的升级：
     ```bash
     pip install --upgrade pip
     pip install --upgrade wordcloud
     pip install --upgrade pillow
     ```

2. **下载字体文件**：
   - 下载华文行楷字体文件（`chinese_stxingka.ttf`）。
   - 将字体文件上传到Jupyter Notebook的同级目录下。

3. **生成词云图**：
   - 在Jupyter Notebook中导入必要的库：
     ```python
     from wordcloud import WordCloud
     from matplotlib import pyplot as plt
     ```
   - 读取字体文件并指定词语列表：
     ```python
     font = './chinese_stxingka.ttf'
     new_data = ['挺舒服', '有史以来', '网上', '买', '漂亮', '最舒服', '衣服']
     ```
   - 创建词云图并显示：
     ```python
     wc = WordCloud(font_path=font, background_color='white', width=1000, height=800)
     wc.generate(" ".join(new_data))
     plt.imshow(wc)
     plt.axis('off')
     plt.show()
     ```

## 注意事项

- 确保在升级库时关闭所有Jupyter Notebook进程，以避免进程占用导致的升级失败。
- 生成的词云图会根据词语的频率和数量自动调整大小和排列，每次运行结果可能会有所不同。

通过本教程，您将能够轻松地在Jupyter Notebook中生成美观的词云图，并解决在过程中可能遇到的各种问题。

## 下载链接

[JupyterNotebook中绘制词云图教程](https://pan.quark.cn/s/79a82bdfc4ea)