---
layout: post
title: "OpenPose 1.7.0 资源文件下载"
date:   2020-10-03
tags: [关键点,OpenPose,检测,支持,1.7]
comments: true
author: admin
---
# OpenPose 1.7.0 资源文件下载

## 简介
OpenPose 1.7.0 是一个实时多人关键点检测库，能够联合检测人体、手部、面部和足部的关键点（共 135 个关键点）。该库在单幅图像上实现了高效的实时检测，适用于多种应用场景。

## 主要功能
- **2D实时多人关键点检测**：
  - 支持 15、18 或 25 个关键点的身体/脚关键点估计，包括 6 个脚关键点。
  - 运行时对检测到的人数不变。
  
- **手部关键点估计**：
  - 支持 21 个关键点的手部关键点估计。
  - 运行时间取决于检测到的人数。
  - 提供运行时不变的替代方案，请参阅 OpenPose 训练。

- **面部关键点估计**：
  - 支持 70 个关键点的面部关键点估计。
  - 运行时间取决于检测到的人数。
  - 提供运行时不变的替代方案，请参阅 OpenPose 训练。

- **3D实时单人关键点检测**：
  - 支持从多个单一视图进行 3D 三角测量。
  - 已处理 Flir 相机的同步。
  - 兼容 Flir/Point Grey 相机。

- **校准工具箱**：
  - 支持失真、内在和外在相机参数的估计。

- **单人跟踪**：
  - 提供单人跟踪功能，以进一步加速或视觉平滑。

- **输入输出支持**：
  - 输入：支持图像、视频、网络摄像头、Flir/Point Grey、IP 摄像头，并支持添加自定义输入源（如深度摄像头）。
  - 输出：支持基本图像+关键点显示/保存（PNG，JPG，AVI 等），关键点保存（JSON，XML，YML 等），关键点作为数组类。

## 使用说明
1. **下载资源文件**：请从本仓库下载 OpenPose 1.7.0 资源文件。
2. **安装与配置**：按照提供的安装指南进行配置和安装。
3. **运行示例**：参考示例代码进行运行和测试。

## 注意事项
- 请确保系统满足 OpenPose 的运行要求。
- 在使用过程中如遇到问题，请参考官方文档或社区支持。

## 贡献
欢迎对本仓库进行贡献，包括但不限于代码优化、文档改进、新增功能等。请提交 Pull Request 或 Issue 进行讨论。

## 许可证
本资源文件遵循相关开源许可证，具体请参阅 LICENSE 文件。

---

希望 OpenPose 1.7.0 能够帮助您在关键点检测领域取得更好的成果！

## 下载链接

[OpenPose1.7.0资源文件下载](https://pan.quark.cn/s/98f59c4504a1)