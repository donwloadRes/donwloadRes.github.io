---
layout: post
title: "Chrome 安装 React DevTools 详细教程"
date:   2022-04-13
tags: [React,Chrome,DevTools,解压,安装]
comments: true
author: admin
---
# Chrome 安装 React DevTools 详细教程

本资源文件提供了在 Chrome 浏览器中安装 React DevTools 的详细教程。React DevTools 是一个非常有用的工具，可以帮助开发者调试和检查 React 应用程序的组件层次结构、状态和属性。

## 内容概述

1. **下载安装包**：提供了 React DevTools 扩展安装包的下载链接，无需 npm install 安装依赖，开箱即用。
2. **添加扩展程序**：详细说明了如何在 Chrome 浏览器中加载已解压的扩展程序。
3. **解决报错**：针对安装过程中可能出现的错误，提供了具体的解决方法。

## 使用步骤

### 1. 下载安装包

- 下载 React DevTools 扩展安装包。
- 注意：该安装包无需 npm install 安装依赖，直接解压即可使用。

### 2. 添加扩展程序

- 解压下载的 zip 文件到目标文件夹。
- 打开 Chrome 浏览器的扩展程序页面（chrome://extensions/）。
- 加载已解压的扩展程序，选择解压后的文件夹。

### 3. 解决报错

- 如果在安装后遇到项目报错，可以尝试以下步骤：
  - 删除项目的 `node_modules` 文件夹，重新安装项目依赖。
  - 找到项目中依赖文件夹下的 `node_modules/@pmmmwh/react-refresh-webpack-plugin/client/ReactRefreshEntry.js` 文件，注释掉 `RefreshRuntime.injectIntoGlobalHook(safeThis)` 这行代码。
  - 重新启动项目。

通过以上步骤，您可以顺利在 Chrome 浏览器中安装并使用 React DevTools，提升 React 应用程序的开发效率。

## 下载链接

[Chrome安装ReactDevTools详细教程](https://pan.quark.cn/s/05acd7a8575f)