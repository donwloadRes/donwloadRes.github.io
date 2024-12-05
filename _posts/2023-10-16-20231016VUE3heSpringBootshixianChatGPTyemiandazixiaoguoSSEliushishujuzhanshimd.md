---
layout: post
title: "VUE3和SpringBoot实现ChatGPT页面打字效果SSE流式数据展示"
date:   2020-08-03
tags: [SSE,页面,SpringBoot,打字,ChatGPT]
comments: true
author: admin
---
# VUE3和SpringBoot实现ChatGPT页面打字效果SSE流式数据展示

本项目展示了如何使用Vue3和SpringBoot结合，实现类似ChatGPT页面的打字效果，并通过SSE（Server-Sent Events）协议进行流式数据展示。

## 项目简介

在现代Web应用中，实时数据展示是一个常见的需求。本项目通过Vue3和SpringBoot的结合，模拟了ChatGPT页面的打字效果，并使用SSE协议实现了服务器向客户端的单向数据流传输。相比于WebSocket，SSE更加轻量，适合用于事件流或通知等场景。

## 主要功能

- **打字效果展示**：模拟ChatGPT页面的打字效果，逐字显示文本内容。
- **SSE流式数据传输**：使用SSE协议实现服务器向客户端的单向数据流传输，避免了复杂的WebSocket配置。

## 技术栈

- **前端**：Vue3
- **后端**：SpringBoot
- **通信协议**：SSE（Server-Sent Events）

## 项目结构

- `myserver`：后端SpringBoot项目
- `myweb`：前端Vue3项目

## 使用说明

1. **环境搭建**：
   - 安装LmStudio工具，下载并启动阿里开源的通义千问语言模型。
   - 启动大模型，后端服务端口为1234。

2. **后端服务**：
   - 使用IDEA打开`myserver`项目，直接运行`ServerApplication`类。
   - 关键代码包括构建请求对象、设置模型、流式返回等。

3. **前端页面**：
   - 打开`myweb`项目，执行`npm install`安装依赖。
   - 运行项目，执行`npm run dev`。
   - 前端页面关键代码包括SSE连接、消息处理、滚动条控制等。

## 注意事项

- 在使用SSE时，注意服务器端的配置，确保能够正确推送数据。
- 前端页面需要处理SSE连接的打开、关闭和错误情况，确保用户体验。

## 贡献

欢迎提交Issue和Pull Request，共同完善本项目。

## 许可证

本项目采用MIT许可证，详情请参阅`LICENSE`文件。

## 下载链接

[VUE3和SpringBoot实现ChatGPT页面打字效果SSE流式数据展示](https://pan.quark.cn/s/d620c670b6fc)