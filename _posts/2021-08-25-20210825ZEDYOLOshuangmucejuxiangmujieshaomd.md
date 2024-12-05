---
layout: post
title: "ZED + YOLO 双目测距项目介绍"
date:   2022-02-25
tags: [ZED,测距,numpy,YOLO,zedceju]
comments: true
author: admin
---
# ZED + YOLO 双目测距项目介绍

## 项目概述

本仓库提供了一个使用ZED摄像头和YOLO进行双目测距的资源文件，主要代码文件为`zedceju.py`。通过结合ZED摄像头的高精度深度感知能力和YOLO的目标检测算法，本项目能够实现对目标物体的实时测距功能。

## 资源文件说明

- **zedceju.py**: 这是本项目的主要运行代码，负责调用ZED摄像头和YOLO模型进行目标检测和测距。

## 使用说明

1. **环境配置**:
   - 首先，你需要从ZED官方网站下载并安装ZED SDK。
   - 确保你的开发环境中已经安装了必要的Python库，如`numpy`、`opencv-python`等。

2. **运行代码**:
   - 在配置好环境后，直接运行`zedceju.py`文件即可启动测距程序。

3. **注意事项**:
   - 在配置过程中，可能会遇到由于`numpy`版本问题导致无法正常调用`import pyzed.sl as sl`的情况。请确保你的`numpy`版本与ZED SDK兼容。

## 常见问题

- **无法导入pyzed.sl**: 请检查你的`numpy`版本是否与ZED SDK兼容，必要时可以尝试降级或升级`numpy`版本。

## 贡献与反馈

如果你在使用过程中遇到任何问题或有改进建议，欢迎提交Issue或Pull Request。我们非常乐意与你一起完善这个项目。

---

希望这个README能够帮助你顺利使用本项目进行双目测距。祝你使用愉快！

## 下载链接

[ZEDYOLO双目测距项目介绍](https://pan.quark.cn/s/6459451f09c5)