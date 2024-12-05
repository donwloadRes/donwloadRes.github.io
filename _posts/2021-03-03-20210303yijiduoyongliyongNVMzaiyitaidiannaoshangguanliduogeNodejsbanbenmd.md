---
layout: post
title: "一机多用利用NVM在一台电脑上管理多个Nodejs版本"
date:   2020-04-27
tags: [Node,js,版本,NVM,安装]
comments: true
author: admin
---
# 一机多用：利用NVM在一台电脑上管理多个Node.js版本

## 概述

面对不同项目对Node.js版本的不同需求，开发者常需要在多个版本间自由切换。本文档基于[CSDN博客](https://blog.csdn.net/steven_son/article/details/135151622)提供的指南，旨在教您如何高效管理多个Node.js版本，使用NVM(Node Version Manager)实现在同一台电脑上安装并自由切换不同版本的Node.js。

### 安装准备

确保您的电脑上未安装Node.js，或您已准备好卸载现有版本以便开始全新的多版本管理之旅。

### NVM安装步骤

1. **下载NVM**: 获取NVM安装程序，推荐使用官方网站或官方推荐渠道。
   
2. **卸载原有Node.js**: 完全卸载先前安装的Node.js版本，并从环境变量中移除相关路径。

3. **安装NVM**: 解压下载的NVM安装包，在合适的位置执行安装，记得为Node.js预先创建安装目录。

4. **配置NVM**: 安装完成后，编辑NVM的`settings.txt`文件，使用国内淘宝镜像加速下载，增加以下行（如果需要）：
   ```
   node_mirror: https://registry.npmmirror.com/binary/html/path=node/
   npm_mirror: https://registry.npmmirror.com/binary/html/path/npm/
   ```

5. **查看NVM版本及使用**: 输入`nvm -v`验证安装，接着使用`nvm ls available`查看可安装的Node.js版本。

6. **安装与切换Node.js版本**: 例如，安装Node.js v14.21.3，命令为`nvm install 14.21.3`，安装完成后，通过`nvm use 14.21.3`切换到该版本。

7. **日常使用**: 安装额外版本（如v16.20.0），并根据项目需求用`nvm use`命令轻松切换。

### 高级应用

- 你可以通过创建`.nvmrc`文件在项目根目录固定所需Node.js版本，NVM会自动识别并切换。
  
- 管理npm/yarn版本：确保Node.js版本匹配所需的npm版本，必要时更新或全局安装工具。

### 结论

NVM是前端开发者乃至任何使用Node.js的开发者不可或缺的工具。它简化了多版本管理的复杂性，让开发者能够专注于代码而非环境配置。通过遵循上述步骤，您可以轻松地在多个Node.js版本间游刃有余，提高工作效率。

---

以上内容概括了使用NVM在单机环境下管理多个Node.js版本的核心步骤，适合想要在不同项目间灵活切换Node环境的开发者参考实践。

## 下载链接

[一机多用利用NVM在一台电脑上管理多个Node.js版本](https://pan.quark.cn/s/c628f7894b00)