---
layout: post
title: "Modelsim 安装步骤详解"
date:   2021-01-07
tags: [Modelsim,安装,文件,仿真,dll]
comments: true
author: admin
---
# Modelsim 安装步骤详解

## 简介
Modelsim 是由 Mentor Graphics 公司开发的优秀的 HDL 语言仿真软件，广泛应用于数字系统设计、FPGA 开发以及 ASIC 验证领域。它提供友好的仿真环境，采用单内核支持 VHDL 和 Verilog 混合仿真的仿真器，具有编译仿真速度快、跨平台跨版本仿真等特点。

## 版本对比
Modelsim 有几种不同的版本：SE、PE、LE 和 OEM。其中 SE 是最高级的版本，而集成在 Actel、Atmel、Altera、Xilinx 以及 Lattice 等 FPGA 厂商设计工具中的均是其 OEM 版本。SE 版和 OEM 版在功能和性能方面有较大差别，特别是在仿真速度上。

## 安装步骤
1. **下载文件**：从提供的链接下载 Modelsim 安装包。
2. **解压文件**：解压下载的文件。
3. **运行安装程序**：双击运行应用程序，进入安装导向界面。
4. **自定义安装路径**：选择安装路径，建议不要放在 C 盘。
5. **同意许可**：阅读并同意许可协议。
6. **创建快捷方式**：选择是否在桌面创建快捷方式。
7. **等待安装**：等待安装完成。
8. **设置环境变量**：安装完成后，设置相应的环境变量。

## 注册步骤
1. **找到 mgls64.dll 文件**：在软件安装目录中找到 mgls64.dll 文件。
2. **取消只读属性**：右击文件，选择属性，取消只读属性。
3. **拷贝文件**：将 MentorKG.exe 和 patch_dll.bat 文件拷贝到 Modelsim 安装目录的 win32 或 win64 下。
4. **运行 patch_dll.bat**：运行 patch_dll.bat，生成 license 文件。
5. **设置环境变量**：设置环境变量 MGLS_LICENSE_FILE，变量值为 license 文件的路径。

## 总结
本资源文件详细介绍了 Modelsim 的下载、安装和注册步骤，帮助用户顺利完成软件的安装和配置。通过本指南，用户可以快速上手使用 Modelsim 进行 HDL 语言仿真。

## 下载链接

[Modelsim安装步骤详解](https://pan.quark.cn/s/9266fb4636aa)