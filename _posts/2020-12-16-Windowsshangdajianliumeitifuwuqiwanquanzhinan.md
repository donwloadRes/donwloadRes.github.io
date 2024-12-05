---
layout: post
title: "Windows上搭建流媒体服务器完全指南"
date:   2023-03-22
tags: [Nginx,RTMP,OBS,流媒体,Windows]
comments: true
author: admin
---
# Windows上搭建流媒体服务器完全指南

## 简介

本文档旨在指导您在Windows操作系统环境下快速搭建一套完整的流媒体服务系统。我们将利用Nginx作为基础服务器，结合其强大的RTMP模块来处理流媒体数据，OBS Studio进行高质量的视频推流，以及VLC Media Player实现实时视频播放。这套组合为您提供了一种高效、低成本的流媒体解决方案，适用于直播、点播等多种应用场景。

## 技术栈
- **Nginx**：高性能的HTTP和反向代理服务器。
- **Nginx RTMP Module**：Nginx的扩展模块，用于支持RTMP协议，实现视频流的接收与分发。
- **OBS Studio**：开源软件，常用于视频录制与直播推流。
- **VLC Media Player**：跨平台多媒体播放器，能够直接播放RTMP流。

## 安装步骤概览

### 1. 安装Nginx及RTMP模块

1. **下载Nginx**: 访问[Nginx官方网站](请手动搜索“Nginx官方下载页面”以获取最新版本)，选择适合Windows的版本下载。
2. **编译安装RTMP模块**（或寻找预先编译好的二进制文件）通常需要自行编译Nginx以添加RTMP模块。但为了简化过程，推荐查找已集成RTMP模块的Nginx二进制包。
   
### 2. 配置Nginx

- 找到Nginx的配置文件`nginx.conf`，通常位于安装目录下的`conf`文件夹内。
- 在配置文件中添加或修改RTMP部分，示例：
   ```nginx
   rtmp {
       server {
           listen 1935;
           chunk_size 4096;

           application live {
               live on;
               record off;
           }
       }
   }
   ```
   这段配置指示Nginx监听RTMP连接在1935端口，并定义了一个名为"live"的应用，接受实时流输入且不记录视频。

### 3. 安装OBS Studio

- 访问[OBS Studio官网](请手动搜索“OBS Studio官方下载”以获取最新版)下载并安装。OBS将用作视频流的生成工具。

### 4. 推流至Nginx

- 启动Nginx服务。
- 在OBS中设置输出，目标地址填入`rtmp://你的服务器IP/live/stream_key`，其中stream_key可以自定义，作为识别直播间的标识。

### 5. 使用VLC拉流观看

- 打开VLC媒体播放器，选择“媒体”->“打开网络串流”，输入`rtmp://你的服务器IP/live/stream_key`，点击播放即可观看直播内容。

## 注意事项

- 确保所有软件组件兼容当前的操作系统环境。
- 防火墙设置需允许Nginx监听的端口（如1935）通信。
- 对于生产环境，建议深入学习Nginx高级配置及流量管理。

遵循上述步骤，您便能在Windows平台上成功建立一个基本的流媒体服务器，为观众提供流畅的直播体验。祝您搭建顺利！

## 下载链接

[Windows上搭建流媒体服务器完全指南](https://pan.quark.cn/s/ed2f664e8cc8)