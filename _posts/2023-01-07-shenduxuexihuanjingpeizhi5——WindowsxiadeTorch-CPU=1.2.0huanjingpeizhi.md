---
layout: post
title: "深度学习环境配置5——Windows下的Torch-CPU=1.2.0环境配置"
date:   2024-08-16
tags: [Anaconda,安装,Torch,Windows,CPU]
comments: true
author: admin
---
# 深度学习环境配置5——Windows下的Torch-CPU=1.2.0环境配置

## 介绍

本资源文件提供了在Windows系统下配置Torch-CPU版本1.2.0的详细步骤和相关依赖库的安装指南。通过本指南，您可以轻松地在Windows环境中搭建一个适合深度学习的开发环境。

## 环境配置步骤

### 1. Anaconda安装

#### 1.1 Anaconda的下载
- 可以选择安装新版Anaconda或旧版的Anaconda。
- 旧版本Anaconda的下载：提供百度网盘链接。
- 新版本Anaconda的下载：登录Anaconda官网下载对应安装包。

#### 1.2 Anaconda的安装
- 选择安装位置，建议不安装在C盘。
- 勾选“Add Anaconda to my PATH environment variable”以自动添加到系统环境变量。

### 2. 配置PyTorch环境

#### 2.1 PyTorch环境的创建与激活
- 使用命令行创建并激活名为`pytorch`的环境。

#### 2.2 PyTorch库的安装
- 使用pip命令安装Torch和TorchVision的CPU版本。

#### 2.3 其他依赖库的安装
- 安装其他必要的依赖库，如scipy、numpy、matplotlib等。

#### 2.4 安装较慢请注意换源
- 配置pip源以加速安装过程。

### 3. 安装VSCODE

#### 3.1 下载安装包安装（推荐）
- 从VSCODE官网下载并安装。

#### 3.2 Anaconda上安装
- 在Anaconda环境中安装VSCODE。

## 注意事项

- 2021/10/8更新：解决部分用户遇到的TypeError: array() takes 1 positional argument but 2 were given错误。
- 学习前言：适用于没有显卡的用户配置深度学习环境。

通过以上步骤，您可以在Windows系统下成功配置Torch-CPU版本1.2.0，并开始您的深度学习项目开发。

## 下载链接

[深度学习环境配置5Windows下的Torch-CPU1.2.0环境配置分享](https://pan.quark.cn/s/85b840705d33)