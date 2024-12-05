---
layout: post
title: "图片标注工具LabelImg使用教程"
date:   2020-10-03
tags: [标注,LabelImg,labelImg,保存,快捷键]
comments: true
author: admin
---
# 图片标注工具LabelImg使用教程

## 简介
LabelImg是一款开源的图形图像注释工具，广泛用于创建边界框（矩形框）和多边形注释，适用于深度学习和计算机视觉中的数据标注工作。该工具支持Windows、Linux和macOS等多个平台，并且能够将标注信息直接转化为XML文件，与PASCAL VOC和ImageNet使用的XML格式兼容。

## 功能特点
- **全图形界面**：使用Python和Qt编写，操作简便。
- **多种标注格式**：支持生成PASCAL VOC和YOLO格式的标注文件。
- **自动保存**：支持自动保存标注结果，避免数据丢失。
- **快捷键支持**：提供多种快捷键，方便快速标注。

## 安装与使用
### 安装步骤
1. **Python环境**：确保系统中已安装Python（版本2.6以上）。
2. **依赖库**：安装PyQt和lxml库。
   ```bash
   sudo apt-get install pyqt4-dev-tools
   sudo pip install lxml
   ```
3. **源码安装**：从GitHub克隆LabelImg仓库并安装。
   ```bash
   git clone https://github.com/tzutalin/labelImg.git
   cd labelImg
   make qt4py2
   python labelImg.py
   ```

### 使用方法
1. **打开软件**：在命令行中输入`python labelImg.py`启动软件。
2. **设置保存路径**：使用快捷键`Ctrl+R`设置标注文件的保存路径。
3. **开始标注**：点击`Open Dir`选择图片文件夹，点击`Create RectBox`开始标注。
4. **保存标注**：标注完成后，点击`Save`保存标注文件。

## 快捷键
- **W**：创建矩形框
- **A**：上一张图片
- **D**：下一张图片
- **Ctrl+S**：保存标注

## 注意事项
- 确保图片质量良好，以便更准确地标注感兴趣的区域。
- 对于大型图像或复杂的标注任务，可能需要花费一些时间来完成标注工作，建议耐心进行。

## 贡献
感谢原作者在GitHub上的贡献，软件一直在更新，各位小伙伴可以关注其最新版本。

## 版权声明
本文为博主原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[图片标注工具LabelImg使用教程分享](https://pan.quark.cn/s/31cdfc8b31ab)