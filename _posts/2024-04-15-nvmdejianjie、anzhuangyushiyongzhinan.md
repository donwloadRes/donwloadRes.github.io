---
layout: post
title: "nvm的简介、安装与使用指南"
date:   2023-09-10
tags: [nvm,NVM,Node,安装,版本]
comments: true
author: admin
---
# nvm的简介、安装与使用指南

## 概述

**NVM（Node Version Manager）** 是一款强大的 Node.js 版本管理工具，让开发者能够轻松地在不同版本的 Node.js 之间切换。这对于需要处理多种项目，每个项目可能依赖于不同 Node.js 版本的开发者来说极为便捷。本 README 将简明扼要地介绍如何安装、配置及使用 NVM。

## 安装步骤

### 对于Windows用户:

1. **下载安装包**: 访问 [NVM for Windows](https://github.com/coreybutler/nvm-windows/releases) 下载适合的版本。
2. **默认安装**: 解压缩并运行安装程序，安装过程将自动配置环境变量，无需额外配置。
3. **验证安装**: 打开命令提示符，输入 `nvm --version`，如果显示出NVM版本号，则表示安装成功。

### 对于macOS/Linux用户:

1. **利用Homebrew安装（macOS推荐）**: 如果已安装Homebrew，运行 `brew install nvm`。
2. **手动安装**: 可根据官方文档，在用户的bash配置文件（如`.bashrc`, `.bash_profile`）中加入NVM的初始化脚本。

## 配置与使用

### 镜像配置（中国用户建议）

- 在NVM安装目录下找到`settings.txt`，配置国内镜像以加快下载速度：
  
    ```
    node_mirror: https://npm.taobao.org/mirrors/node/
    npm_mirror: https://npm.taobao.org/mirrors/npm/
    ```

### 安装Node.js版本

1. 列出可安装的Node.js版本：`nvm list available`。
2. 安装特定版本：`nvm install 14.17.0`（以14.17.0为例）。

### 切换Node.js版本

- 使用某个已安装版本：`nvm use 14.17.0`。

### 日常使用命令

- 查看已安装的Node.js版本：`nvm list`。
- 显示当前使用的版本：`nvm current`。
- 卸载版本：`nvm uninstall 14.17.0`。
- 列出可切换的所有版本：`nvm ls`。
- 更多功能，请查阅 `nvm help`。

## 结论

掌握NVM的基本使用方法能极大地提高开发效率，特别是在管理多项目环境时。通过本指南，你应该能够顺利安装NVM，并在不同Node.js版本间灵活切换。记得定期检查NVM和Node.js的更新，以维持最优的开发体验。

开始管理你的Node.js版本吧，让你的开发工作更加高效！

## 下载链接

[nvm的简介安装与使用指南](https://pan.quark.cn/s/49635264efa4)