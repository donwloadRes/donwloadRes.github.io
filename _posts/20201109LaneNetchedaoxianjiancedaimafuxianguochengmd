---
layout: post
title: "LaneNet车道线检测代码复现过程"
date:   2024-10-13
tags: [lanenet,path,LaneNet,sys,lane]
comments: true
author: admin
---
# LaneNet车道线检测代码复现过程

## 简介
本仓库提供了一个用于车道线检测的代码复现过程，基于LaneNet算法。该资源文件包含了复现LaneNet车道线检测效果所需的所有必要文件和步骤。

## 内容概述
- **模型权重文件**：包含了预训练的LaneNet模型权重，用于车道线检测。
- **代码文件**：包括了LaneNet算法的实现代码，以及测试脚本。
- **配置文件**：列出了运行代码所需的相关库及其版本。

## 使用步骤
1. **下载并解压文件**：
   - 下载本仓库提供的压缩包并解压。
   - 注意：解压后的`model`文件夹下包含`New_Tusimple_Lanenet_Model_Weights`权重文件，这是复现效果的关键。

2. **修改路径**：
   - 打开`tools`文件夹下的`test_lanenet.py`文件，根据你的实际路径修改相关路径。
   - 示例：
     ```python
     import sys
     sys.path.append('C:/Users/Lenovo/Desktop/lanenet-lane-detection-master')
     sys.path.append('C:/Users/Lenovo/Desktop/lanenet-lane-detection-master/config')
     sys.path.append('C:/Users/Lenovo/Desktop/lanenet-lane-detection-master/data_provider')
     sys.path.append('C:/Users/Lenovo/Desktop/lanenet-lane-detection-master/lanenet_model')
     sys.path.append('C:/Users/Lenovo/Desktop/lanenet-lane-detection-master/tools')
     ```

3. **运行测试脚本**：
   - 在`lanenet-lane-detection-master`文件夹下运行以下命令：
     ```bash
     python tools/test_lanenet.py --weights_path model/New_Tusimple_Lanenet_Model_Weights/tusimple_lanenet_vgg.ckpt --image_path data/tusimple_test_image/0.jpg
     ```
   - 注意：`pictures`文件夹用于保存检测结果的图片，源码中没有这个文件夹，需要自行创建。

4. **测试效果**：
   - 使用提供的测试图片进行检测，效果良好。
   - 也可以使用自己的图片进行检测，但需注意图片分辨率应为1280X720。

## 注意事项
- 确保Python版本为3.5.2，并安装`requirements_new.txt`中列出的相关库。
- 如果使用自己的数据集进行测试，效果不佳可能是由于图片分辨率不匹配，需调整分辨率至1280X720。

## 更新记录
- **2020年6月11日**：修复了图片分辨率不匹配导致车道线检测效果不佳的问题。
- **2021年10月31日**：新增了一个简单的上位机程序，用于显示检测结果。

## 贡献
欢迎提交问题和改进建议，帮助我们完善这个项目。

## 许可证
本项目遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[LaneNet车道线检测代码复现过程分享](https://pan.quark.cn/s/b0c1bc859165)