---
layout: post
title: "NVM下载安装及使用Node环境变量的配置"
date:   2024-06-05
tags: [Node,js,NVM,版本,bash]
comments: true
author: admin
---
# NVM下载安装及使用、Node环境变量的配置

本文详细介绍了如何下载、安装NVM（Node Version Manager）以及配置Node环境变量。通过NVM，用户可以轻松管理多个Node.js版本，并在不同项目中切换使用不同的Node.js版本。

## 1. NVM简介

NVM是一个用于管理多个Node.js版本的工具。它允许用户在同一台机器上安装和切换不同的Node.js版本，非常适合开发者在不同项目中使用不同版本的Node.js。

## 2. NVM的下载与安装

### 2.1 下载NVM

首先，访问NVM的官方GitHub仓库，下载最新版本的NVM安装脚本。

### 2.2 安装NVM

在终端中运行下载的安装脚本，按照提示完成NVM的安装。安装完成后，可以通过以下命令验证NVM是否安装成功：

```bash
nvm --version
```

## 3. 使用NVM安装Node.js

### 3.1 列出可用的Node.js版本

使用以下命令列出所有可用的Node.js版本：

```bash
nvm ls-remote
```

### 3.2 安装指定版本的Node.js

选择一个版本号，使用以下命令安装该版本的Node.js：

```bash
nvm install <version>
```

例如，安装Node.js 14.17.0版本：

```bash
nvm install 14.17.0
```

### 3.3 切换Node.js版本

安装完成后，可以使用以下命令切换到指定版本的Node.js：

```bash
nvm use <version>
```

例如，切换到Node.js 14.17.0版本：

```bash
nvm use 14.17.0
```

## 4. 配置Node环境变量

### 4.1 设置默认Node.js版本

为了确保每次打开终端时都使用指定的Node.js版本，可以设置默认版本：

```bash
nvm alias default <version>
```

例如，设置默认版本为Node.js 14.17.0：

```bash
nvm alias default 14.17.0
```

### 4.2 验证环境变量

在终端中输入以下命令，验证Node.js版本是否正确：

```bash
node -v
```

## 5. 总结

通过NVM，开发者可以轻松管理多个Node.js版本，并在不同项目中灵活切换。本文详细介绍了NVM的下载、安装、使用以及Node环境变量的配置，希望能帮助开发者更好地管理Node.js环境。

## 下载链接

[NVM下载安装及使用Node环境变量的配置](https://pan.quark.cn/s/95126f5a80d7)