---
layout: post
title: "Web端播放RTSP-RTMP视频流Demo"
date:   2021-10-20
tags: [视频流,Web,播放,RTSP,RTMP]
comments: true
author: admin
---
# Web端播放RTSP/RTMP视频流Demo

本仓库提供了一个在Web端播放RTSP/RTMP视频流的示例项目。通过结合FFmpeg、Node.js（使用node-rtsp-stream模块）和jsmpeg，实现了低延迟的视频流播放方案，延迟时间控制在1秒以内。

## 项目描述

本项目旨在展示如何在Web端实现低延迟的RTSP/RTMP视频流播放。通过以下技术栈的组合，我们能够有效地减少视频流的延迟，提供流畅的观看体验：

- **FFmpeg**: 用于视频流的处理和转码。
- **Node.js**: 使用node-rtsp-stream模块来处理RTSP/RTMP流。
- **jsmpeg**: 一个基于JavaScript的MPEG1视频播放器，用于在Web端播放视频流。

## 快速开始

### 环境要求

- Node.js (建议版本: 14.x 或更高)
- FFmpeg

### 安装步骤

1. **克隆仓库**

    ```bash
    git clone https://github.com/your-repo/web-rtsp-rtmp-demo.git
    cd web-rtsp-rtmp-demo
    ```

2. **安装依赖**

    ```bash
    npm install
    ```

3. **配置FFmpeg路径**

    确保FFmpeg已安装并配置好环境变量，或者在项目配置文件中指定FFmpeg的路径。

4. **启动服务器**

    ```bash
    node server.js
    ```

5. **访问Web界面**

    打开浏览器，访问 `http://localhost:3000`，即可看到视频流播放界面。

## 配置说明

在 `config.js` 文件中，您可以配置以下参数：

- **RTSP/RTMP流地址**: 指定要播放的RTSP或RTMP流地址。
- **端口号**: Web服务器的端口号。

## 贡献

欢迎任何形式的贡献，包括但不限于代码改进、问题反馈、文档完善等。请参考 [CONTRIBUTING.md](CONTRIBUTING.md) 了解更多详情。

## 许可证

本项目采用 [MIT 许可证](LICENSE)。

## 联系我们

如有任何问题或建议，请通过 [issues](https://github.com/your-repo/web-rtsp-rtmp-demo/issues) 联系我们。

---

感谢您对本项目的关注和支持！希望本示例能帮助您在Web端实现低延迟的视频流播放。

## 下载链接

[Web端播放RTSPRTMP视频流Demo](https://pan.quark.cn/s/1bfaaedbc93c)