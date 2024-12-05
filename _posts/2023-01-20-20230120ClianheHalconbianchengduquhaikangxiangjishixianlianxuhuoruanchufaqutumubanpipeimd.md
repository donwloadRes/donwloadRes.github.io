---
layout: post
title: "C 联合 Halcon 编程读取海康相机实现连续或软触发取图模板匹配"
date:   2020-09-28
tags: [读取,Halcon,相机,海康,模板]
comments: true
author: admin
---
# C# 联合 Halcon 编程读取海康相机，实现连续或软触发取图模板匹配

## 项目描述

本资源文件提供了一个完整的解决方案，用于在 C# 环境下联合 Halcon 编程，实现对海康威视相机的读取，并进行连续或软触发取图以及模板匹配操作。以下是该资源文件的主要功能和特点：

1. **X64 版本 VS2022 与 Halcon 23.05 联合编程**：
   - 实现了在 64 位环境下，使用 Visual Studio 2022 与 Halcon 23.05 进行联合编程。

2. **VS 调用海康威视类直接读取相机**：
   - 通过 Visual Studio 调用海康威视提供的类库，直接读取海康相机，简化了相机读取的流程。

3. **海康类转换成 Halcon 图像**：
   - 实现了将海康相机读取的图像数据转换为 Halcon 图像格式，便于后续的图像处理操作。

4. **HSmartWindow 缩放、平移、显示、画图功能**：
   - 实现了 Halcon 的 HSmartWindow 控件的缩放、平移、显示和画图功能，方便用户在界面上进行图像操作。

5. **模板匹配算法**：
   - 实现了模板匹配算法，并与直接使用 Halcon 读取相机的方式进行了比较，结果表明该方案速度更快、更稳定。

## 功能实现

- **图像平移缩放**：
  ```csharp
  this.MouseWheel += new System.Windows.Forms.MouseEventHandler(this.my_MouseWheel);
  ```

- **读取相机**：
  ```csharp
  m_pDeviceList = new MyCamera.MV_CC_DEVICE_INFO_LIST();
  ```

- **定义海康威视类，设置相机，读取图像**：
  ```csharp
  m_pMyCamera = new MyCamera();
  ```

- **程序运行后，打开相机即可操作 Halcon**：
  - **连续读取**：开启连续读取图像，并进行模板匹配。
  - **Halcon 读取**：开启软件触发功能，触发一次，读取一次。

  ```csharp
  Thread hReceiveImageThreadHandle = new Thread(ReceiveImage);
  ```

## 使用说明

1. **环境配置**：
   - 确保已安装 Visual Studio 2022（X64 版本）和 Halcon 23.05。
   - 配置好海康威视相机的驱动和相关类库。

2. **运行程序**：
   - 打开相机后，程序会自动读取图像并显示在 Halcon 的 HSmartWindow 控件中。
   - 可以通过界面上的按钮选择连续读取或软触发读取模式。

3. **模板匹配**：
   - 在连续读取模式下，程序会自动进行模板匹配操作，并将匹配结果显示在界面上。

## 注意事项

- 确保相机连接正常，且驱动和类库配置正确。
- 在进行模板匹配时，确保模板图像与实际图像的匹配度较高，以获得更好的匹配效果。

## 贡献

欢迎大家提出改进建议或提交代码，共同完善该项目。

## 下载链接

[C联合Halcon编程读取海康相机实现连续或软触发取图模板匹配](https://pan.quark.cn/s/2d04454be258)