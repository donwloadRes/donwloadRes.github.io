---
layout: post
title: "vuedevtools 下载及使用指南"
date:   2020-01-22
tags: [devtools,Vue,chrome,下载,浏览器]
comments: true
author: admin
---
# vue-devtools 下载及使用指南

### 概述
Vue-devtools 是一款专为 Vue.js 应用程序开发的强大调试工具。它允许开发者在浏览器中深入查看和调试Vue组件树，监控数据变化，以及追踪生命周期钩子等，极大地方便了Vue应用的开发和维护。本指南将引导您完成vue-devtools的下载、安装和基本配置步骤。

### 下载步骤
1. 访问 **[GitHub](https://github.com/vuejs/devtools)** 官网，定位到指定版本的仓库。推荐使用的版本为 v6.5.0。
2. 在给出的链接 `https://github.com/vuejs/devtools/tree/v6.5.0` 中，找到“Clone or download”按钮，选择下载ZIP文件，完成下载。
3. 解压缩下载的文件至您想要存放的本地目录。

### 安装与配置
#### 环境准备
- 确保您的计算机已安装 **Node.js**，这是运行devtools脚本的前提条件。如果没有安装，可以从 [Node.js官方网站](https://nodejs.org/) 进行下载安装。

#### 安装步骤
1. 打开解压缩后的文件夹，通过命令行工具（如CMD或Git Bash）进入该目录。
2. 输入命令 `npm install` 来安装项目所需的依赖。请确保网络环境良好，以便顺利完成依赖下载。
3. 安装成功后，继续输入命令 `npm run build` 来编译项目。这一步可能会生成用于浏览器的扩展文件。

#### 配置manifest.json
- 编辑 `shells\chrome` 目录下的 `manifest.json` 文件。
- 找到 `"persistent": false` 行，并将其修改为 `"persistent": true`。这一调整有助于保持扩展的后台持续运行状态。

#### 注意事项
- 如果在构建过程中遇到问题，考虑到可能的开发环境差异，您可以尝试从提供的特定资源中下载预先处理过的 `shells\chrome` 目录，以绕过潜在的构建错误。
- 替换现有 `chrome` 目录后，无需重复编译。

### 使用Vue-devtools
1. 打开Google Chrome浏览器，进入设置 -> 更多工具 -> 扩展程序 或 直接在地址栏输入 `chrome://extensions/`
2. 开启“开发者模式”，点击“加载已解压的扩展程序”选项，选择您之前解压并修改过的 `shells\chrome` 目录。
3. 成功加载后，Vue-devtools即被添加至您的浏览器中，现在，当您访问任何Vue应用时，应该能在浏览器右上角看到Vue图标，表示它可以开始工作了。

通过遵循以上步骤，您就可以高效地利用Vue-devtools来优化您的Vue应用程序开发流程。祝您调试愉快！

## 下载链接

[vue-devtools下载及使用指南](https://pan.quark.cn/s/98fb392d7ddd)