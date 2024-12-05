---
layout: post
title: "QT59 与百度地图交互示例"
date:   2024-03-11
tags: [QT,交互,调用,地图,QT5.9]
comments: true
author: admin
---
# QT5.9 与百度地图交互示例

本项目演示了如何在 QT5.9 中利用 `QWebEngineView` 和 `QWebChannel` 调用 JavaScript 实现 QT 与 HTML 网页数据交互，并加载百度地图进行数据交互。通过本示例，您可以学习到如何在 QT 中加载网页、调用 JavaScript 函数以及实现双向数据交互。

## 功能描述

1. **加载百度地图**：QT 通过 `QWebEngineView` 模块加载百度地图。
2. **数据交互**：通过 `QWebChannel` 调用 JavaScript 函数实现 QT 与地图数据的交互。
3. **标注功能**：点击 `pushButton` 按钮，QT 会调用 JavaScript 函数在地图页做标注，通过输入框输入经纬度（C++ 调用 JS）。
4. **坐标回传**：鼠标点击地图页后会提示点的坐标信息，并回传给 QT，通过 `qDebug()` 显示（JS 调用 C++）。

## 详细说明

更多详细说明和实现步骤，请参考我的博客文章：[QT5.9 利用 QWebEngineView / QWebChannel 调用JS程序实现QT与HTML网页数据交互](https://blog.csdn.net/qq_43569273/article/details/88122422)。

## 如何使用

1. **克隆仓库**：
   ```bash
   git clone https://github.com/yourusername/your-repo-name.git
   ```

2. **打开项目**：
   使用 QT Creator 打开项目文件。

3. **编译运行**：
   编译并运行项目，查看效果。

## 贡献

欢迎提交 Issue 和 Pull Request，共同完善本项目。

## 许可证

本项目采用 [MIT 许可证](LICENSE)。

## 下载链接

[QT5.9与百度地图交互示例](https://pan.quark.cn/s/a3d6d7f3ce7a)