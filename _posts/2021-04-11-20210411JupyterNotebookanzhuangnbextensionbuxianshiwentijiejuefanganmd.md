---
layout: post
title: "Jupyter Notebook 安装 nbextension 不显示问题解决方案"
date:   2021-12-27
tags: [Jupyter,Notebook,marked,js,文件]
comments: true
author: admin
---
# Jupyter Notebook 安装 nbextension 不显示问题解决方案

## 简介

本资源文件提供了一个解决方案，用于解决在 Jupyter Notebook 中安装 nbextension 后不显示的问题。该问题通常是由于 `marked.js` 文件未正确加载导致的。通过下载并替换该文件到指定目录，可以修复此问题。

## 问题描述

在安装了 `jupyter_contrib_nbextensions` 后，重新启动 Jupyter Notebook 时，发现 nbextensions 选项未显示。终端输出中显示 `404 GET` 错误，表示获取 `marked.js` 文件失败。

## 解决方案

1. **下载 `marked.js` 文件**：
   - 从提供的资源链接中下载 `marked.js` 文件。

2. **替换文件**：
   - 找到本地 Python 安装目录，将下载的 `marked.js` 文件放入以下目录：
     ```
     C:\Users\<用户名>\Programs\Python\Python39\Lib\site-packages\nbclassic\static\components\marked\lib
     ```

3. **重启 Jupyter Notebook**：
   - 关闭所有 Jupyter Notebook 页面，重新启动 Jupyter Notebook。

## 注意事项

- 确保下载的 `marked.js` 文件版本与 Jupyter Notebook 兼容。
- 如果问题仍然存在，可以尝试在评论区查找其他用户的解决方案。

## 参考

该解决方案参考了 CSDN 博客文章，详细步骤和更多信息可以在文章中找到。

---

通过以上步骤，您应该能够成功解决 Jupyter Notebook 安装 nbextension 不显示的问题。

## 下载链接

[JupyterNotebook安装nbextension不显示问题解决方案分享](https://pan.quark.cn/s/3da27a37dcf0)