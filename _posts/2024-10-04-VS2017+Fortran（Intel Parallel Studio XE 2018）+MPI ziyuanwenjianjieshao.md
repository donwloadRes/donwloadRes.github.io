---
layout: post
title: "VS2017+Fortran（Intel Parallel Studio XE 2018）+MPI 资源文件介绍"
date:   2024-09-08
tags: [Studio,Fortran,Intel,Parallel,XE]
comments: true
author: admin
---
# VS2017+Fortran（Intel Parallel Studio XE 2018）+MPI 资源文件介绍

本资源文件提供了在Windows 10操作系统下，使用Visual Studio 2017（VS2017）与Intel Parallel Studio XE 2018集成Fortran编程环境，并配置MPI（Message Passing Interface）进行并行计算的详细步骤和相关文件。

## 资源内容

1. **VS2017安装包**：用于安装Visual Studio 2017，包含C++库，以便与Intel Parallel Studio XE 2018集成。
2. **Intel Parallel Studio XE 2018安装包**：包含Inter Visual Fortran组件，用于Fortran编程。
3. **MPI插件**：用于配置MPI并行环境。

## 安装步骤

1. **安装VS2017**：
   - 解压文件并直接安装。
   - 安装时需选择C++库，以便后续与Intel Parallel Studio XE 2018集成。

2. **安装Intel Parallel Studio XE 2018**：
   - 先关闭VS2017窗口。
   - 安装Intel Parallel Studio XE 2018，选择Inter Visual Fortran组件。
   - 安装过程中选择license注册（五个任选其一即可）。

3. **安装MPI插件**：
   - 配置MPI并行环境。

## 项目MPI并行配置流程

1. **新建Fortran项目**。
2. **设置项目的链接库**：
   - 在“调试——属性——Fortran——General——Additional Inclue Directories”中添加include目录。
   - 在“调试——属性——Linker——General——Additional Library Directories”中添加库目录。
   - 在“调试——属性——Linker——Input——Additional Dependencies”中添加依赖库。
   - 将MPI执行文件放到VS2017项目的目录下。

3. **运行测试程序**：
   - 使用提供的Fortran MPI程序进行测试。

## 参考资料

- 详细配置步骤和示例程序请参考[CSDN博客文章](https://blog.csdn.net/upc_cly/article/details/123782915)。

## 注意事项

- Intel Parallel Studio XE 2018需要安装在C盘。
- 确保所有步骤按照顺序进行，避免集成失败。

通过本资源文件，您可以顺利配置VS2017与Intel Parallel Studio XE 2018的Fortran编程环境，并进行MPI并行计算。

## 下载链接

[VS2017FortranIntelParallelStudioXE2018MPI资源文件介绍](https://pan.quark.cn/s/b9f8b42adef1)