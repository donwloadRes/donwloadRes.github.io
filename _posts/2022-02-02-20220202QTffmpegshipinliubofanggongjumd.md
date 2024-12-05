---
layout: post
title: "QT  ffmpeg 视频流播放工具"
date:   2020-12-10
tags: [视频流,播放,QT,ffmpeg,项目]
comments: true
author: admin
---
# QT + ffmpeg 视频流播放工具

## 项目简介

本项目是一个基于 **VS2017 + QT + ffmpeg** 开发的视频播放工具，旨在提供一个简单易用的界面来播放 **RTSP**、**RTMP** 和 **UDP** 视频流。该工具的核心功能是实现视频流的播放，适用于需要快速集成视频播放功能的开发者或项目。

## 功能特点

- **支持多种视频流协议**：
  - RTSP（Real-Time Streaming Protocol）
  - RTMP（Real-Time Messaging Protocol）
  - UDP（User Datagram Protocol）

- **简单易用**：
  - 提供直观的用户界面，方便用户输入视频流地址并进行播放。
  - 代码结构清晰，易于理解和二次开发。

## 环境要求

- **开发环境**：
  - Visual Studio 2017
  - QT 框架
  - ffmpeg 库

- **运行环境**：
  - Windows 操作系统

## 使用说明

1. **克隆仓库**：
   ```bash
   git clone https://github.com/your-repo-url.git
   ```

2. **打开项目**：
   - 使用 Visual Studio 2017 打开项目文件。

3. **配置环境**：
   - 确保已安装 QT 和 ffmpeg 库，并在项目中正确配置相关路径。

4. **编译运行**：
   - 编译项目并运行，输入视频流地址即可开始播放。

## 示例

以下是一个简单的使用示例：

```bash
# 输入 RTSP 流地址
rtsp://example.com/stream

# 输入 RTMP 流地址
rtmp://example.com/live/stream

# 输入 UDP 流地址
udp://@:1234
```

## 贡献

欢迎大家贡献代码或提出改进建议。如果您有任何问题或建议，请在 GitHub 上提交 Issue 或 Pull Request。

## 许可证

本项目采用 MIT 许可证，详情请参阅 [LICENSE](LICENSE) 文件。

---

希望这个项目能帮助您快速实现视频流的播放功能！

## 下载链接

[QTffmpeg视频流播放工具](https://pan.quark.cn/s/2ca1c3359137)