---
layout: post
title: "安装 Vue Devtools 及常见问题指南"
date:   2021-06-04
tags: [Vue,Devtools,安装,下载,常见问题]
comments: true
author: admin
---
# 安装 Vue Devtools 及常见问题指南

本文详细介绍了如何安装 Vue Devtools 以及在安装过程中可能遇到的常见问题及其解决方法。Vue Devtools 是一款用于调试 Vue.js 应用的开发者工具，能够极大地提高开发效率。

## 安装步骤

### 1. 下载 Vue Devtools

你可以通过以下三种方式之一下载 Vue Devtools：

- **Vue2 百度网盘下载**：适用于 Vue2 项目，下载链接中包含 Vue2 的 devtools 安装工具。
- **极简插件下载**：下载完成后，解压可以查看到安装步骤。
- **GitHub 下载**：适用于 Vue3 项目，下载链接中包含 Vue3 的 devtools 安装工具。

### 2. CRX 安装

1. 打开浏览器的管理扩展程序页签。
2. 将得到的 `vue_dev_tools.crx` 文件拖动到扩展程序页面进行安装。

### 3. 手动安装

1. 从 GitHub 下载或通过 Git 克隆 Vue Devtools 源码。
2. 解压并编译：
   - 首先需要安装 Node.js。
   - 在解压目录下启动命令行，执行以下脚本：
     ```bash
     cnpm install -g yarn
     yarn install
     yarn run build:watch
     yarn run dev:chrome
     ```
3. 通过浏览器的管理扩展程序，将编译后的 `shell-chrome` 目录作为解压的扩展程序进行安装。

## 常见问题及解决方法

### 1. Vue2 项目打开浏览器的调试器后看不到 Vue 标签

**解决方法**：显示调试工具的原因是使用了生产环境的版本或是压缩的 Vue 版本。Vue Devtools 只在开发环境生效。需要在项目 `main.js` 中引入以下配置：
```javascript
Vue.config.devtools = true;
```

### 2. 加载失败

**解决方法**：
- 检查是否开启了开发者模式。
- 确保选择正确的文件夹路径。
- 尝试重启 Chrome 浏览器后再次加载。

### 3. 无法查看 Vue 组件

**解决方法**：
- 确认当前页面是否为 Vue 项目。
- 检查是否正确安装了 Vue Devtools。

通过以上步骤和常见问题的解决方法，你应该能够顺利安装并使用 Vue Devtools 进行 Vue.js 应用的调试。

## 下载链接

[安装VueDevtools及常见问题指南](https://pan.quark.cn/s/7a7350d245cd)