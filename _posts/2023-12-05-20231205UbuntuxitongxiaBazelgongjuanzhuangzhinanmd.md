---
layout: post
title: "Ubuntu系统下Bazel工具安装指南"
date:   2021-08-12
tags: [bazel,Bazel,sudo,apt,Ubuntu]
comments: true
author: admin
---
# Ubuntu系统下Bazel工具安装指南

欢迎来到Ubuntu系统下Bazel工具的安装教程。Bazel是一款由Google开发的强大构建与测试工具，广泛应用于多语言项目的自动化构建，尤其在Java、C++、Python和Go等语言的大型项目中表现出色。本指南基于[CSDN博客](https://blog.csdn.net/weixin_49401384/article/details/137423485)提供的内容，为您详述在Ubuntu操作系统上安装Bazel的具体步骤。

## 前提条件

确保您的Ubuntu系统已更新至最新版本，并具备网络连接。此外，根据需要，可能还需要安装C++编译器、unzip和zip工具，以及Java Development Kit (JDK)。

## 安装步骤

### 添加Bazel APT源

1. 打开终端。
2. 更新系统包列表：`sudo apt update`
3. 安装必要工具：`sudo apt install curl gnupg`
4. 添加Bazel的GPG公钥：
   ```
   curl -fsSL https://bazel.build/bazel-release.pub.gpg | gpg --dearmor > bazel.gpg
   sudo mv bazel.gpg /etc/apt/trusted.gpg.d/
   ```

5. 添加Bazel的APT仓库：
   ```
   echo "deb [arch=amd64] https://storage.googleapis.com/bazel-apt stable jdk1.8" | sudo tee /etc/apt/sources.list.d/bazel.list
   ```

### 解决网络问题

如果遇到因网络导致的`curl`访问问题，可考虑下载公钥文件后本地导入。

### 安装Bazel

1. 更新软件包索引：`sudo apt update`
2. 搜索可用的Bazel版本：`sudo apt search bazel`
3. 安装指定版本的Bazel（以`bazel-4.2.0`为例）：`sudo apt install bazel-4.2.0`
4. （可选）创建全局快捷方式：`sudo ln -s /usr/bin/bazel-4.2.0 /usr/bin/bazel`
5. 验证安装：`bazel --version`

## 注意事项

- 根据您的Ubuntu版本和需求，选择适合的Bazel版本进行安装。
- 若系统为ARM架构（如Raspberry Pi），需调整相应的软件源地址中的架构信息。
- 确保所有操作均以具有足够权限的用户账户执行，通常需要使用`sudo`。

## 结语

通过以上步骤，您将能够在Ubuntu系统上成功安装Bazel，从而为您的软件开发项目搭建坚实的自动化构建基础。祝您开发顺利！

## 下载链接

[Ubuntu系统下Bazel工具安装指南分享](https://pan.quark.cn/s/d79ea5be2224)