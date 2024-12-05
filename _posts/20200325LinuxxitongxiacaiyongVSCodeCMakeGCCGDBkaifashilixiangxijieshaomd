---
layout: post
title: "Linux系统下采用VSCode+CMake+GCC+GDB开发实例详细介绍"
date:   2024-10-10
tags: [CMake,Linux,VSCode,C++,调试]
comments: true
author: admin
---
# Linux系统下采用VSCode+CMake+GCC+GDB开发实例详细介绍

在Linux环境中，集成开发环境的选择对于提高编程效率至关重要。本资源详细介绍了如何在Linux操作系统中搭建一个高效、便捷的C/C++开发环境，主要围绕Visual Studio Code（简称VSCode）作为代码编辑器，CMake作为构建系统，GCC作为编译器，以及GDB用于调试。下面将逐步引导您完成整个开发环境的配置，确保您可以流畅地进行项目开发、编译和调试。

## 环境需求

- **操作系统**: Linux发行版（如Ubuntu、Debian等）
- **Visual Studio Code**: 一款轻量级但功能强大的源代码编辑器。
- **CMake**: 用于管理项目的构建过程。
- **GCC/G++**: GNU Compiler Collection，用于编译C/C++程序。
- **GDB**: GNU Debugger，用于调试C/C++程序。

## 安装步骤

### 1. 安装Visual Studio Code

通过官方网站或Linux包管理器安装VSCode。例如，在Ubuntu上，可以使用命令：

```bash
sudo apt-get install code -y
```

### 2. 安装必要的插件

打开VSCode，进入 Extensions (齿轮图标) -> 搜索并安装以下插件：
- C/C++: 提供语法高亮、智能感知等。
- CodeLLDB 或 CMake Tools: 分别用于调试和CMake项目的支持。

### 3. 安装CMake

通过终端安装CMake：

```bash
sudo apt-get install cmake -y
```

### 4. 安装GCC/G++

通常Linux发行版会预装GCC/G++，如果没有，可以通过包管理器安装：

```bash
sudo apt-get install g++ build-essential -y
```

### 5. 配置VSCode

#### 创建项目文件夹及CMakeLists.txt

在你喜欢的位置创建一个新的目录作为你的项目根目录，并在此目录下创建`CMakeLists.txt`，示例内容如下：

```cmake
cmake_minimum_required(VERSION 3.0)
project(MyProject)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

add_executable(MyProject main.cpp)
```

#### 设置VSCode工作区

1. 在VSCode中打开你刚才创建的项目文件夹。
2. 首次使用CMake Tools可能需要配置`settings.json`，添加以下内容以指定CMake路径：

   ```json
   "cmake.configureSettings": {
       "CMAKE_BUILD_TYPE": "Debug",
       "CMAKE_PREFIX_PATH": "/usr/local"
   },
   ```

3. 使用CMake Tools：点击状态栏上的"CMake: Configure"，然后"CMake: Build"来生成项目文件并编译。

### 6. 调试配置

- 在VSCode中，选择“运行”视图，点击齿轮图标创建 launch.json 文件。
- 根据提示，选择C++（GDB/LLDB）调试配置模板。
- 根据需要调整launch.json中的设置，比如程序的路径和启动参数。

### 开始编码与调试

现在，您的开发环境已搭建完毕，可以在VSCode中编写C++代码，利用CMake进行构建，通过GDB或CodeLLDB插件进行调试。按F5即可启动调试，享受高效的Linux下C/C++开发体验。

---

这个流程覆盖了从环境搭建到实际开发调试的基本步骤，让您能够迅速开始在Linux环境下使用VSCode进行C/C++项目开发。祝您开发愉快！

## 下载链接

[Linux系统下采用VSCodeCMakeGCCGDB开发实例详细介绍分享](https://pan.quark.cn/s/89d102e7911f)