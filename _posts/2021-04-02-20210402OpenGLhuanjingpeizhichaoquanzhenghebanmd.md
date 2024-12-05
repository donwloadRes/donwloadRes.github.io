---
layout: post
title: "OpenGL环境配置超全整合版"
date:   2023-04-30
tags: [OpenGL,文件夹,glad,配置,Visual]
comments: true
author: admin
---
# OpenGL环境配置（超全整合版）

## 简介
本资源文件提供了一个完整的OpenGL环境配置包，适用于Windows系统下的开发环境搭建。该配置包整合了OpenGL开发所需的所有关键组件，包括库文件、头文件和动态链接库，旨在帮助开发者快速搭建OpenGL开发环境，减少配置过程中的繁琐步骤。

## 配置步骤

### 1. 事前准备
- 一块主流显卡（最好是独显）
- Visual Studio IDE（推荐使用2017以上版本，本人使用的是2019）

### 2. 下载完整配置包
解压后，暂时先仅考虑以下3个文件夹和一个文件：
- `include` 文件夹
- `lib` 文件夹
- `dll` 文件夹
- `glad.c` 文件

### 3. 文件放置
将解压后的文件夹内容分别放入以下路径：
- `include` 文件夹中的内容放入 `C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.25.28610\include`
- `lib` 文件夹中的内容放入 `C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.25.28610\lib\x86`
- `dll` 文件夹中的内容放入 `C:\Windows\SysWOW64`

注意：以上路径适用于64位系统，32位系统请类比放置。

### 4. 创建项目
在Visual Studio中创建一个空项目，然后通过菜单 → 管理 NuGet 程序包，搜索并下载 `glfw`。

### 5. 添加源文件
将 `glad.c` 文件放入项目的源文件中。

### 6. 测试
完成上述步骤后，可以尝试运行一个简单的OpenGL示例代码，验证环境配置是否成功。

## 注意事项
- 如果 `glad` 出现问题，可以自行生成：访问 [glad在线网站](https://glad.dav1d.de/)，选择 `gl` 版本为 `3.3` 以上，生成后下载并使用。
- 关于电脑自带的OpenGL版本，可以通过查看 `C:\Program Files (x86)\Windows Kits\10\Include\10.0.xxxxx.0\um\gl\GL.h` 文件中的 `#define GL_VERSION_1_1 1` 来确定。

## 总结
本资源文件提供了一个完整的OpenGL环境配置解决方案，帮助开发者快速搭建开发环境，减少配置过程中的繁琐步骤。希望这个配置包能够帮助到所有需要进行OpenGL开发的开发者。

## 下载链接

[OpenGL环境配置超全整合版](https://pan.quark.cn/s/63912c3b0086)