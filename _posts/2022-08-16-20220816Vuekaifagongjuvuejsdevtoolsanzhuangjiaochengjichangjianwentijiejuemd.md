---
layout: post
title: "Vue开发工具vuejsdevtools安装教程及常见问题解决"
date:   2022-04-07
tags: [devtools,Vue,vuejs,vue,插件]
comments: true
author: admin
---
# Vue开发工具vuejs-devtools安装教程及常见问题解决

本文详细介绍了如何安装Vue开发工具vuejs-devtools，并提供了常见问题的解决方法。通过本教程，您可以轻松地在浏览器中安装和使用vuejs-devtools，提升Vue应用的开发效率。

## 一、vue.js插件下载

1. **下载地址**：访问Vue官网下载vue.js插件，共有两种版本的插件（开发版本和生产版本）。
2. **建议**：推荐使用开发版本，因为开发版本提供了更多的错误信息提示和调试功能，虽然文件较大，但在开发过程中能更方便地解决bug。

## 二、Vue开发工具vuejs-devtools下载

1. **官网下载**：访问Vue开发工具vuejs-devtools的官网下载页面，下载master分支中的版本，这是最终获得认可的版本。
2. **依赖安装**：下载后需要通过npm安装一些依赖，才能导入到谷歌浏览器中使用。
3. **已安装依赖的包**：提供了一个已经安装好依赖的包，您可以直接下载后解压导入到谷歌浏览器中使用。

## 三、Vue开发工具vuejs-devtools安装+使用

1. **解压导入**：将提供的vuejs-devtools解压后导入谷歌浏览器即可使用。
2. **配置文件**：如果是自己下载的，需要配置manifest.json文件，将persistent状态改成true。
3. **导入插件**：打开谷歌浏览器中的【拓展程序】，勾选【开发者模式】，点击【加载已解压的拓展程序】，选择解压的vuejs-devtools插件文件夹导入。
4. **调试模式**：用谷歌浏览器打开文件进入调试模式（按F12），即可在调试控制台看到vue页签。

## 四、常见问题解决

1. **没有vue页签**：
   - **方法一**：检查是否引入了生产版本的vue插件（vue.main.js），如果是，需要在js文件中的创建vue实例前写入`Vue.config.devtools = true`。
   - **方法二**：确保导入的是开发版本的插件（vue.js）。
   - **其他方法**：在扩展程序中开启允许访问文件网址和在无痕模式下启用两项。

通过以上步骤，您可以顺利安装并使用vuejs-devtools，提升Vue应用的开发效率。

## 下载链接

[Vue开发工具vuejs-devtools安装教程及常见问题解决](https://pan.quark.cn/s/b902d5031398)