---
layout: post
title: "Unity PC端内嵌网页插件Embedded Browser使用指南"
date:   2021-04-13
tags: [Unity,插件,Browser,网页,Embedded]
comments: true
author: admin
---
# Unity PC端内嵌网页插件：Embedded Browser使用指南

## 概述
本文档旨在为Unity开发者提供详细的指南，解释如何使用Embedded Browser插件在PC平台上内嵌网页视图。Embedded Browser是一款强大且易用的Unity插件，允许你在Unity应用中无缝集成网页浏览功能，支持HTML、CSS和JavaScript的交互，并且便于与Unity场景进行数据交换。

### 版本信息
本文基于插件版本3.1.0编写，适用于Unity 5.6.3及以上版本。

### 插件获取
- **官方渠道**：可在Unity Asset Store购买，售价$75。
- **经济选项**：亦可在中国淘宝平台以极低价格购得，甚至通过分享获得免费的老版本资源。

### 快速入门

#### 安装步骤
1. **下载插件**: 通过购买或上述提及的方式获取`EmbeddedBrowser.unitypackage`文件。
2. **导入Unity**: 在Unity中，右键选择Import Package，导入下载的包文件。

#### 基础使用
- **公网网址**: 新建场景，向Canvas添加Raw Image，通过“Add Component”添加GUI Browser UI，设定URL为网页地址，如百度搜索。
- **本地HTML**: 创建名为BrowserAssets的文件夹，并放置你的HTML文件。在Unity中通过`localGame://路径.html`访问。

### Unity与HTML交互
- **Unity调用JS**: 注册C#方法到浏览器，供JavaScript调用。
- **JS调用Unity**: 在HTML中通过指定的函数名称触发Unity中的事件，实现双向数据传递。

#### 注意事项
- **兼容性**: 确保使用正确的组件，避免使用已被淘汰的GUI Browser。
- **视频播放**: 由于版权原因，默认不支持MP4格式，推荐使用WebM格式。
- **Vue.js开发**: 若使用Vue框架，需确保交互函数为全局可访问。

### 文档和学习资源
虽然文档不易查找，但从Unity商店页面可以获取或尝试社区讨论和教程。遇到特定问题时，社区和论坛是宝贵的知识来源。

### 结论
Embedded Browser提供了在Unity项目中内嵌网页的强大能力，无论是用于UI扩展还是复杂的应用逻辑交互，都能极大地丰富游戏或应用程序的功能。掌握其基本使用和高级交互，能够提升项目的灵活性和用户体验。开始探索，解锁更多的创意可能性吧！

---

请根据实际需要调整和补充细节，以确保文档的完整性和准确性。

## 下载链接

[UnityPC端内嵌网页插件EmbeddedBrowser使用指南](https://pan.quark.cn/s/d2d13c63ceed)