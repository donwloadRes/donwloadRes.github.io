---
layout: post
title: "谷歌浏览器中打开IE"
date:   2022-03-05
tags: [浏览器,IE,谷歌,调用,打开]
comments: true
author: admin
---
# 谷歌浏览器中打开IE

## 简介

本资源文件提供了一种在谷歌浏览器中打开Internet Explorer（IE）的方法。通过使用特定的JavaScript代码和注册表设置，用户可以在谷歌浏览器中点击链接时自动调用IE浏览器打开指定的网页。

## 使用方法

### 方法一：注册表设置

1. 将提供的注册表文件导入到系统中。
2. 在HTML页面中使用以下代码调用IE浏览器：
   ```html
   <a href="openIE:www.baidu.com">Chrome调起IE</a>
   ```

### 方法二：使用可执行文件

1. 下载并运行提供的可执行文件（alertIE.exe）。
2. 在HTML页面中使用以下代码调用IE浏览器：
   ```html
   <a href="alert:www.baidu.com">Chrome调起IE</a>
   ```

## 注意事项

- 确保IE浏览器的默认安装路径正确，否则可能导致调用失败。
- 使用方法一时，可能会弹出一个DOS黑窗口，使用方法二则不会出现此问题。

## 适用场景

- 当需要在谷歌浏览器中打开某些仅支持IE浏览器的网页时。
- 适用于需要在不同浏览器之间进行页面展示的项目。

## 参考资料

- 更多详细信息请参考[CSDN博客文章](https://blog.csdn.net/q1424966670/article/details/102663051)。

---

通过以上方法，您可以轻松实现在谷歌浏览器中调用IE浏览器打开网页的功能。

## 下载链接

[谷歌浏览器中打开IE分享](https://pan.quark.cn/s/f987754a965d)