---
layout: post
title: "银河麒麟V10系统+飞腾CPU交叉编译Qt5.15"
date:   2023-12-24
tags: [dev,编译,sudo,5.15,Qt]
comments: true
author: admin
---
# 银河麒麟V10系统+飞腾CPU交叉编译Qt5.15

## 资源描述

本资源文件提供了在银河麒麟V10系统上，使用飞腾CPU进行Qt 5.15的交叉编译的详细步骤和所需资源。通过本资源，您可以顺利完成Qt 5.15的编译工作，为您的开发环境提供强大的支持。

## 准备工作

### 1. 下载Qt源码包

在任意空闲位置新建文件夹，并将源码包解压到该目录下。建议在`/home`目录下新建名为`Qt_source`的文件夹。请确保该目录所在位置的空闲空间大于等于15G。

在该目录下执行以下命令：

```bash
sudo xz -d qt-everywhere-src-5.15.2.tar.xz
sudo tar -xvf qt-everywhere-src-5.15.2.tar
```

### 2. 安装所依赖的库

#### 1) 安装基础编译环境

执行以下命令安装基础编译环境：

```bash
sudo apt-get install libxcb-xinerama0-dev
sudo apt-get install build-essential perl python git
```

#### 2) 安装编译Libxcb的相关依赖

执行以下命令安装编译Libxcb的相关依赖：

```bash
sudo apt-get install ^libxcb.*-dev libx11-xcb-dev libglu1-mesa-dev libxrender-dev libxi-dev libxkbcommon-dev libxkbcommon-x11-dev
```

## 使用说明

请按照上述步骤进行操作，确保所有依赖库和环境配置正确无误。编译过程中可能会遇到一些问题，建议查阅相关文档或社区支持进行解决。

## 注意事项

- 确保系统空间充足，建议至少预留15G的空闲空间。
- 编译过程中可能会消耗较长时间，请耐心等待。
- 如有任何问题，欢迎在社区中寻求帮助。

## 贡献与反馈

如果您在使用过程中遇到任何问题或有改进建议，欢迎提交反馈。我们期待您的参与，共同完善本资源文件。