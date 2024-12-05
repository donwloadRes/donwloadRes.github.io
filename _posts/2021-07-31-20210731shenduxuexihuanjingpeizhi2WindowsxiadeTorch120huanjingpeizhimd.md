---
layout: post
title: "深度学习环境配置2Windows下的Torch120环境配置"
date:   2023-05-01
tags: [安装,Anaconda,环境,Torch,配置]
comments: true
author: admin
---
# 深度学习环境配置2——Windows下的Torch=1.2.0环境配置

## 介绍

本资源文件提供了在Windows系统下配置Torch 1.2.0深度学习环境的详细步骤和所需文件。通过本资源，您可以轻松地在Windows系统上搭建一个稳定且高效的深度学习开发环境。

## 环境配置步骤

### 1. Anaconda安装

- **下载Anaconda**：可以选择安装新版或旧版的Anaconda。旧版Anaconda包含VSCODE，安装更为方便。
- **安装Anaconda**：选择安装位置，建议不安装在C盘。安装过程中可以选择将Anaconda添加到系统环境变量中，以便更方便地配置环境。

### 2. Cudnn和CUDA的下载和安装

- **下载Cudnn和CUDA**：根据Torch 1.2.0的要求，下载对应的Cuda 10.0和Cudnn 7.4.1版本。
- **安装Cudnn和CUDA**：下载完成后，运行安装程序进行安装。安装完成后，将Cudnn的内容解压并复制到CUDA的安装目录中。

### 3. 配置Torch环境

- **创建并激活环境**：使用Anaconda创建一个名为`pytorch`的环境，并激活该环境。
- **安装Torch库**：在激活的环境中，使用官方推荐的安装方法或手动下载whl文件进行安装。
- **安装其他依赖库**：安装完成后，还需要安装一些其他依赖库，如`scipy`、`numpy`、`matplotlib`等。

### 4. 安装VSCODE

- **下载并安装VSCODE**：可以选择直接下载安装包进行安装，或者通过Anaconda进行安装。
- **配置VSCODE**：安装完成后，配置VSCODE以使用Anaconda创建的环境。

## 注意事项

- **2021/9/11更新**：安装CUDA前需要安装Visual Studio，建议安装Visual Studio 2017。
- **2021/7/8更新**：部分用户反馈遇到`TypeError: array() takes 1 positional argument but 2 were given`错误，可以通过修改Pillow版本解决。

## 总结

通过本资源文件，您可以顺利地在Windows系统上配置Torch 1.2.0的深度学习环境，为后续的深度学习项目开发打下坚实的基础。

## 下载链接

[深度学习环境配置2Windows下的Torch1.2.0环境配置分享](https://pan.quark.cn/s/dc5ff4e39bbb)