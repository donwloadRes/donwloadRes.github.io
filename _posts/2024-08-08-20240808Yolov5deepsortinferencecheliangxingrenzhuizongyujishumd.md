---
layout: post
title: "Yolov5-deepsort-inference: 车辆行人追踪与计数"
date:   2020-09-24
tags: [self,YOLOv5,Detector,init,行人]
comments: true
author: admin
---
# Yolov5-deepsort-inference: 车辆行人追踪与计数

## 项目简介

本项目基于YOLOv5和Deepsort算法，实现对视频流中的车辆和行人进行实时追踪和计数。代码已封装成一个检测器类，方便用户将其嵌入到自己的项目中。

## 主要功能

- **实时检测**：使用YOLOv5模型对视频流中的车辆和行人进行实时检测。
- **目标追踪**：结合Deepsort算法，对检测到的目标进行持续追踪。
- **计数功能**：自动统计视频流中出现的车辆和行人的数量。

## 代码结构

本项目的主要代码封装在一个名为`Detector`的类中，继承自`baseDet`基类。以下是`Detector`类的初始化方法：

```python
class Detector(baseDet):
    def __init__(self):
        super(Detector, self).__init__()
        self.init_model()
        self.build_config()

    def init_model(self):
        # 初始化模型相关参数
        pass

    def build_config(self):
        # 构建配置参数
        pass
```

## 使用说明

1. **环境配置**：
   - 本项目使用YOLOv5 3.0版本，请确保安装了相应的依赖库。
   - 如果使用YOLOv5 4.0版本，请替换掉`models`和`utils`文件夹。

2. **代码集成**：
   - 将`Detector`类集成到你的项目中，调用相关方法即可实现车辆和行人的检测与追踪。

3. **运行效果**：
   - 运行项目后，系统会实时显示视频流中的检测结果，并统计车辆和行人的数量。

## 注意事项

- 本项目依赖于YOLOv5 3.0版本，如果使用其他版本，请注意模型文件的兼容性。
- 代码中的`init_model`和`build_config`方法需要根据实际需求进行实现。

## 贡献与反馈

欢迎大家提出改进建议或贡献代码。如果你在使用过程中遇到任何问题，请在项目中提交Issue，我们会尽快回复并解决问题。

## 许可证

本项目采用MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[Yolov5-deepsort-inference车辆行人追踪与计数](https://pan.quark.cn/s/bcef1ca0597d)