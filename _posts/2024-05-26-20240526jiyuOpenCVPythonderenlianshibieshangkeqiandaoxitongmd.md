---
layout: post
title: "基于 OpenCV  Python 的人脸识别上课签到系统"
date:   2020-04-18
tags: [签到,人脸,人脸识别,图像,采集]
comments: true
author: admin
---
# 基于 OpenCV + Python 的人脸识别上课签到系统

## 项目简介
本项目构建了一个基于 OpenCV 和 Python 的人脸识别上课签到系统。该系统通过人脸识别技术，实现了自动化的课堂签到功能，适用于学校、培训机构等场景。

## 功能特点
1. **人脸图像采集**：通过摄像头采集学生的人脸图像，并保存到本地数据库中。
2. **模型训练**：使用 OpenCV 中的 LBPH 算法对采集到的人脸图像进行训练，生成人脸识别模型。
3. **识别签到**：开启摄像头实时跟踪人脸，将获取的人脸特征信息与训练好的模型进行比对，完成签到功能。
4. **签到记录**：签到结果会自动记录在 Excel 文档中，方便后续查看和管理。

## 使用步骤
1. **安装第三方库**：首先安装项目所需的第三方库，包括 opencv-python、opencv-contrib-python、pillow、tk、xlrd、xlwt、xlutils。
2. **采集人脸图像**：运行 `capture_face.py` 脚本，通过摄像头采集学生的人脸图像，并保存到 `dataset` 文件夹中。
3. **训练模型**：运行 `train.py` 脚本，使用 LBPH 算法对采集到的人脸图像进行训练，生成 `face_model.yml` 文件。
4. **识别签到**：运行 `sign_in.py` 脚本，开启摄像头进行实时人脸识别，完成签到功能，签到结果会自动记录在 `签到表.xls` 文件中。
5. **查看签到结果**：签到成功后，项目目录会生成 `签到表1.xls` 文件，双击打开即可查看签到结果。

## 注意事项
1. 在建立签到表时，务必确保单元格格式设置为文本格式，否则可能导致签到失败。
2. 保存签到表时，保存位置应为当前项目的目录文件夹，文件命名为“签到表”，保存类型选择 xls 格式。

## 项目作者
- 学号：2021520542
- 姓名：蔡徐坤

## 版权声明
本项目为原创作品，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[基于OpenCVPython的人脸识别上课签到系统](https://pan.quark.cn/s/babfd349e725)