---
layout: post
title: "WebRTC语音视频通话Demo"
date:   2024-08-11
tags: [服务端,客户端,WebRTC,Demo,安卓]
comments: true
author: admin
---
# WebRTC语音视频通话Demo

## 简介

本仓库提供了一个基于WebRTC技术的语音视频通话Demo，包含安卓客户端代码和Node.js服务端代码。通过本Demo，您可以快速了解和体验WebRTC在实时通信中的应用。

## 资源文件说明

### 安卓客户端

- **代码文件**: 包含完整的WebRTC安卓客户端代码。
- **配置文件**: `string.xml` 文件中需要修改服务端的IP地址和端口号，以确保客户端能够正确连接到服务端。

### Node.js服务端

- **代码文件**: 包含完整的WebRTC Node.js服务端代码。
- **运行命令**:
  - 安装依赖: `npm install`
  - 启动服务: `npm start`
  - 服务默认运行在3000端口，您可以在浏览器中访问 `localhost:3000` 进行测试。

## 使用说明

1. **配置安卓客户端**:
   - 打开安卓客户端代码中的 `string.xml` 文件。
   - 修改服务端的IP地址和端口号，确保客户端能够正确连接到服务端。

2. **启动Node.js服务端**:
   - 在终端中进入服务端代码目录。
   - 执行 `npm install` 安装依赖。
   - 执行 `npm start` 启动服务。
   - 服务默认运行在3000端口，您可以在浏览器中访问 `localhost:3000` 进行测试。

3. **视频显示兼容性**:
   - 由于浏览器兼容性问题，视频显示可能会有问题。推荐使用Chrome浏览器以获得最佳体验。

## 注意事项

- 确保安卓客户端和服务端在同一网络环境下运行，以保证通信的稳定性。
- 如果遇到视频显示问题，请尝试使用Chrome浏览器进行测试。

## 贡献

欢迎提交Issue和Pull Request，共同完善本Demo。

## 许可证

本项目采用MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[WebRTC语音视频通话Demo](https://pan.quark.cn/s/444d5b827e06)