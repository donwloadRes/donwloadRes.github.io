---
layout: post
title: "AI识别两张图片是否为同一个人  faceapi  Nodejs"
date:   2024-04-16
tags: [图片,face,api,faceapi,nets]
comments: true
author: admin
---
# AI识别两张图片是否为同一个人 - face-api + Node.js

## 项目描述

本资源文件提供了一个基于`face-api`和`Node.js`的AI识别工具，用于判断两张图片中是否为同一个人。该工具不仅可以识别本地图片，还支持网络图片的比对。此外，它还能估算图片中人物的大致年龄。

## 功能特点

- **人脸识别**：通过`face-api`获取图片中的人脸信息。
- **图片比对**：对比两张图片中的人脸，判断是否为同一个人。
- **年龄估算**：估算图片中人物的大致年龄。
- **本地与网络图片支持**：支持本地图片和网络图片的比对。

## 使用方法

1. **加载模型**：
   - `faceapi.nets.faceRecognitionNet.loadFromDisk(./models)`
   - `faceapi.nets.faceLandmark68Net.loadFromDisk(./models)`
   - `faceapi.nets.ssdMobilenetv1.loadFromDisk(./models)`
   - `faceapi.nets.ageGenderNet.loadFromDisk(./models)`

2. **运行程序**：
   - 根据提供的代码示例，加载模型并运行程序进行图片比对。

## 注意事项

- 确保模型文件路径正确。
- 网络图片比对时，确保图片链接有效。

## 参考资料

本项目参考了`face-api`的相关文档和示例代码，具体实现细节可参考相关文档。

---

希望本资源文件能帮助你快速实现图片中人脸的识别与比对。如有任何问题，欢迎反馈！

## 下载链接

[AI识别两张图片是否为同一个人-face-apiNode.js](https://pan.quark.cn/s/6a8b900b4d7f)