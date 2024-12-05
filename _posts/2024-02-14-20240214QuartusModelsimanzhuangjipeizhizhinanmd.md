---
layout: post
title: "Quartus  Modelsim 安装及配置指南"
date:   2021-02-20
tags: [Quartus,Modelsim,安装,配置,路径]
comments: true
author: admin
---
# Quartus & Modelsim 安装及配置指南

本资源文件提供了详细的 Quartus 和 Modelsim 安装及配置步骤，适用于 FPGA 开发初学者和进阶用户。通过本指南，您可以顺利完成 Quartus 和 Modelsim 的安装，并进行相关配置，以便开始您的 FPGA 开发工作。

## 内容概述

1. **Quartus 和 Modelsim 的安装**
   - 下载安装包
   - 安装步骤详解
   - 安装驱动

2. **Quartus 破解**
   - 破解工具的使用
   - 许可证文件的配置

3. **Quartus 配置 Modelsim**
   - 配置路径
   - 运行仿真

4. **USB Blaster 驱动更新**
   - 驱动更新步骤

5. **VScode 联合 Modelsim 检错**
   - VScode 安装拓展
   - 配置环境变量
   - 联合检错设置

## 安装步骤

### 1. Quartus 和 Modelsim 的安装

- 下载 Quartus 和 Modelsim 的安装包。
- 右键点击 `QuartusSetup`，选择以管理员身份运行。
- 按照安装向导的提示，选择安装路径（建议不要使用中文路径）。
- 勾选所需选项，完成安装。

### 2. Quartus 破解

- 打开刚安装好的 Quartus，选择试用 30 天。
- 将破解器放置在指定目录并运行。
- 复制 NIC ID，修改许可证文件并放置在指定路径。
- 在 Quartus 中配置许可证文件，完成破解。

### 3. Quartus 配置 Modelsim

- 在 Quartus 中点击 `Tools -> Options`，选择 `EDA Tools Options`。
- 填入 Modelsim 的安装路径。
- 选择 `Tools -> Run Simulation Tool -> RTL Simulation` 进行波形观测。

### 4. USB Blaster 驱动更新

- 打开设备管理器，右键点击 `Altera USB-Blaster`，选择更新驱动。
- 浏览安装路径，勾选包括子文件夹，完成驱动更新。

### 5. VScode 联合 Modelsim 检错

- 在 VScode 中安装相关拓展。
- 配置环境变量，添加 Modelsim 安装路径。
- 在 VScode 中配置 Verilog 的 Linter，填入 Modelsim 的工作路径。

## 结语

通过本指南，您可以顺利完成 Quartus 和 Modelsim 的安装及配置，为您的 FPGA 开发工作打下坚实的基础。如果在安装过程中遇到任何问题，欢迎参考原文档或联系相关技术支持。

## 下载链接

[QuartusModelsim安装及配置指南分享](https://pan.quark.cn/s/f7027dc9c8d5)