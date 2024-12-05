---
layout: post
title: "Linux下MKL库的安装部署与使用"
date:   2021-02-12
tags: [MKL,cmake,安装,Intel,Linux]
comments: true
author: admin
---
# Linux下MKL库的安装部署与使用

本文详细介绍了在Linux系统下如何安装和部署Intel Math Kernel Library (MKL)，并通过cmake编译器调用MKL库来提升eigen库的计算速度。

## 1. 安装MKL库

首先，确保你的系统已经安装了Intel Parallel Studio XE或Intel oneAPI Base Toolkit，因为MKL库通常包含在这些工具包中。如果没有安装，可以从Intel官方网站下载并安装。

### 1.1 下载与安装

1. 访问Intel官方网站，下载适合你系统的Parallel Studio XE或oneAPI Base Toolkit。
2. 按照安装向导进行安装，确保选择安装MKL库。

### 1.2 环境变量配置

安装完成后，需要配置环境变量以便系统能够找到MKL库。编辑你的`~/.bashrc`或`~/.zshrc`文件，添加以下内容：

```bash
export MKLROOT=/opt/intel/oneapi/mkl/latest
export LD_LIBRARY_PATH=$MKLROOT/lib/intel64:$LD_LIBRARY_PATH
export CMAKE_PREFIX_PATH=$MKLROOT:$CMAKE_PREFIX_PATH
```

保存并退出，然后运行`source ~/.bashrc`或`source ~/.zshrc`使配置生效。

## 2. 使用cmake调用MKL库

在CMakeLists.txt文件中，添加以下内容以确保cmake能够找到并使用MKL库：

```cmake
find_package(MKL REQUIRED)
include_directories(${MKL_INCLUDE_DIRS})
target_link_libraries(your_target_name ${MKL_LIBRARIES})
```

## 3. 提升eigen库的计算速度

Eigen是一个高效的C++模板库，用于线性代数计算。通过与MKL库结合使用，可以显著提升Eigen的计算速度。

### 3.1 配置Eigen使用MKL

在编译Eigen项目时，确保链接MKL库。可以在CMakeLists.txt中添加以下内容：

```cmake
set(EIGEN_USE_MKL_ALL ON)
```

### 3.2 编译与运行

完成上述配置后，使用cmake生成Makefile并进行编译：

```bash
mkdir build
cd build
cmake ..
make
```

编译完成后，运行生成的可执行文件，即可体验到MKL库带来的性能提升。

## 4. 总结

通过本文的介绍，你已经学会了如何在Linux系统下安装和部署MKL库，并通过cmake调用MKL库来提升eigen库的计算速度。希望这些内容对你有所帮助。

## 下载链接

[Linux下MKL库的安装部署与使用](https://pan.quark.cn/s/0658b1386acc)