---
layout: post
title: "Vue CLI 下载仓库失败解决办法"
date:   2021-12-12
tags: [webpack,templates,vue,vuejs,离线]
comments: true
author: admin
---
# Vue CLI 下载仓库失败解决办法

## 概述
在使用 Vue CLI 工具创建 Vue 项目时，可能会遇到 `vue-cli Failed to download repo vuejs-templates/webpack` 的错误。该错误通常是由于网络连接问题或需要翻墙导致的。本文将介绍如何通过离线方式解决此问题。

## 问题描述
在执行 `vue init webpack 项目名称` 命令时，可能会出现以下错误信息：
```
vue-cli · Failed to download repo vuejs-templates/webpack: connect ETIMEDOUT
```
这通常是因为在下载某个包时，网络连接超时或需要翻墙。

## 解决办法
### 1. 离线创建项目
为了避免网络问题，可以通过离线方式创建 Vue 项目。具体步骤如下：

1. **下载模板文件**：
   - 从 GitHub 仓库中下载 `vuejs-templates/webpack` 模板文件。
   - 下载地址：[vuejs-templates/webpack](https://github.com/vuejs-templates/webpack)

2. **解压模板文件**：
   - 将下载的压缩包解压到本地用户目录下。
   - 例如，解压到 `C:\Users\你的用户名\.vue-templates\webpack` 目录下。

3. **修改文件夹名称**：
   - 确保文件夹名称正确，即 `.vue-templates` 和 `webpack`。

4. **执行命令**：
   - 使用以下命令创建项目，并添加 `--offline` 参数以离线模式运行：
     ```
     vue init webpack 项目名称 --offline
     ```

### 2. 检查网络设置
如果离线方式无法解决问题，可以尝试检查网络设置，确保网络连接正常，或者设置代理以翻墙访问。

## 总结
通过上述步骤，可以有效解决 `vue-cli Failed to download repo vuejs-templates/webpack` 的问题。离线创建项目是一种可靠的解决方案，尤其适用于网络环境不稳定的场景。

## 下载链接

[VueCLI下载仓库失败解决办法分享](https://pan.quark.cn/s/25537892a138)