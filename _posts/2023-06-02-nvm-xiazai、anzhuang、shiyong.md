---
layout: post
title: "nvm-下载、安装、使用"
date:   2020-06-30
tags: [nvm,NVM,安装,bash,Node]
comments: true
author: admin
---
# nvm-下载、安装、使用

## 一、简介

NVM（Node Version Manager）是一个简单且强大的 Node.js 版本管理工具，允许你在同一台机器上安装和切换多个版本的 Node.js。这对于需要在不同项目中使用不同版本的开发者来说非常实用。本文将指导你如何下载、安装 NVM，并介绍基本的使用方法。

## 二、下载

首先，你需要从 NVM 的官方 GitHub 仓库获取最新的脚本。访问 [NVM GitHub 页面](https://github.com/nvm-sh/nvm)，找到并点击 "Clone or download" 按钮，接着选择 “Download ZIP”。解压后，你可以得到包含安装脚本的文件夹。

但是为了简化流程，推荐直接通过命令行安装。在终端或命令提示符中执行以下命令来安装：

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
```

或者，如果你使用的是 Windows，建议通过 PowerShell 使用 `Set-ExecutionPolicy Unrestricted` 命令，然后运行官方提供的 PowerShell 脚本来安装 NVM。

## 三、安装

### 对于 macOS/Linux 用户：

安装脚本会自动完成 NVM 的安装过程。安装完成后，重启你的终端，或者手动运行 `source ~/.bash_profile` （或 `.bashrc`, `.zshrc`，取决于你的 shell 配置）以使环境变量生效。

### 对于 Windows 用户：

Windows 用户可以直接运行下载文件中的批处理脚本进行安装，随后确保将 NVM 的路径添加到系统环境变量中。

## 四、使用

### 检查安装

安装成功后，可以通过运行以下命令来验证 NVM 是否正确安装：

```bash
nvm --version
```

### 安装 Node.js 版本

使用 NVM 安装特定版本的 Node.js，例如安装最新稳定版：

```bash
nvm install stable
```

或者指定版本号安装，如安装 Node.js v14.17.0：

```bash
nvm install 14.17.0
```

### 切换 Node.js 版本

安装了多个版本后，可以轻松切换：

```bash
nvm use 14.17.0
```

### 查看已安装的 Node.js 版本

要查看已经安装的所有 Node.js 版本，输入：

```bash
nvm ls
```

### 卸载 Node.js 版本

如果需要卸载某个版本，可以使用：

```bash
nvm uninstall 14.17.0
```

## 五、总结

NVM 提供了一种简洁的方式来管理和切换不同的 Node.js 环境，极大地便利了开发工作。通过以上步骤，你应该能够顺利地配置好 NVM 并开始根据项目需求自由地使用不同版本的 Node.js 了。记住，合理利用 NVM 可以避免因版本不匹配带来的诸多问题，让你的开发环境更加灵活可控。

## 下载链接

[nvm-下载安装使用](https://pan.quark.cn/s/bbe7ef6cc313)