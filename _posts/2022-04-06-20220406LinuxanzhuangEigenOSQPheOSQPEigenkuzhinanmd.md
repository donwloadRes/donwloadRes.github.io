---
layout: post
title: "Linux安装EigenOSQP和OSQPEigen库指南"
date:   2021-09-21
tags: [Eigen,OSQP,build,安装,文件夹]
comments: true
author: admin
---
# Linux安装Eigen、OSQP和OSQP-Eigen库指南

本仓库提供了一个详细的指南，帮助你在Linux系统上安装Eigen、OSQP和OSQP-Eigen库。这些库在C/C++编程中广泛用于矩阵运算和二次规划求解。

## 目录

1. [Eigen库的安装](#eigen库的安装)
2. [OSQP库的安装](#osqp库的安装)
3. [OSQP-Eigen库的安装](#osqp-eigen库的安装)
4. [测试安装是否成功](#测试安装是否成功)

## Eigen库的安装

1. 下载Eigen库文件。
2. 将下载的Eigen文件夹拷贝到主目录下。
3. 进入Eigen文件夹，打开终端并执行以下命令：
   ```bash
   mkdir build
   cd build
   cmake ..
   sudo make install
   ```
4. 将头文件拷贝到系统的用户头文件中：
   ```bash
   sudo cp -r /home/你的用户名/eigen-3.4.0 /usr/local/include/eigen3
   ```

## OSQP库的安装

1. 下载OSQP库文件。
2. 将下载的OSQP文件夹拷贝到主目录下。
3. 进入OSQP文件夹，打开终端并执行以下命令：
   ```bash
   mkdir build
   cd build
   cmake ..
   cmake -DCMAKE_INSTALL_PREFIX=/usr/local/osqp ..
   sudo make install
   source ~/.bashrc
   ```

## OSQP-Eigen库的安装

1. 下载OSQP-Eigen库文件。
2. 将下载的OSQP-Eigen文件夹拷贝到主目录下。
3. 进入OSQP-Eigen文件夹，打开终端并执行以下命令：
   ```bash
   mkdir build
   cd build
   cmake ..
   cmake -DCMAKE_INSTALL_PREFIX=/usr/local/osqp-eigen ..
   sudo make install
   source ~/.bashrc
   ```

## 测试安装是否成功

1. 下载测试代码文件。
2. 将测试代码文件夹拷贝到主目录下。
3. 进入测试代码文件夹，打开终端并执行以下命令：
   ```bash
   mkdir build
   cd build
   cmake ..
   make
   ./testqjj
   ```
4. 如果测试代码成功编译并运行，说明Eigen、OSQP和OSQP-Eigen库已成功安装。

通过以上步骤，你可以在Linux系统上成功安装并使用Eigen、OSQP和OSQP-Eigen库。如果在安装过程中遇到任何问题，请参考原始文章或联系相关技术支持。

## 下载链接

[Linux安装EigenOSQP和OSQP-Eigen库指南](https://pan.quark.cn/s/cf1a30d6cc48)