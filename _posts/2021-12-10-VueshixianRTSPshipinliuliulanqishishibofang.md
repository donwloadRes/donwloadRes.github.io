---
layout: post
title: "Vue实现RTSP视频流浏览器实时播放"
date:   2020-02-12
tags: [视频流,js,Vue,RTSP,播放]
comments: true
author: admin
---
# Vue实现RTSP视频流浏览器实时播放

## 简介

本资源文件提供了一个基于Vue.js的解决方案，用于在浏览器中实时播放RTSP视频流。通过本方案，您可以轻松地将监控摄像头或其他设备的实时视频流嵌入到您的Vue.js项目中，实现浏览器端的实时监控。

## 功能特点

- **实时播放**：支持在浏览器中实时播放RTSP视频流。
- **低延迟**：通过WebRTC技术，实现低延迟的视频流播放。
- **易于集成**：提供详细的步骤和代码示例，方便开发者快速集成到Vue.js项目中。

## 使用步骤

### 1. 下载并解压资源文件

首先，下载并解压本资源文件。解压后，您将看到以下文件结构：

```
webrtc-streamer/
├── webrtc-streamer.exe
├── html/
│   ├── webrtcstreamer.js
│   └── libs/
│       └── adapter.min.js
└── README.md
```

### 2. 启动WebRTC服务

双击`webrtc-streamer.exe`文件，启动WebRTC服务。您也可以通过命令行启动服务，以减少CPU占用。

### 3. 配置Vue项目

将`webrtcstreamer.js`和`adapter.min.js`文件复制到您的Vue项目`public`目录下，并在`index.html`文件中引入这两个JS文件：

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
  <meta name="renderer" content="webkit" />
  <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no" />
  <link rel="icon" href="<%= BASE_URL %>favicon.ico" />
  <script src="<%= BASE_URL %>adapter.min.js"></script>
  <script src="<%= BASE_URL %>webrtcstreamer.js"></script>
  <title><%= webpackConfig.name %></title>
</head>
</html>
```

### 4. 编写Vue组件

在您的Vue组件中，编写以下代码以实现RTSP视频流的播放：

```vue
<template>
  <div>
    <video id="video" controls autoplay muted width="100%" height="100%" style="object-fit: fill"></video>
  </div>
</template>

<script>
export default {
  data() {
    return {
      webRtcServer: null,
      camera_ip: '127.0.0.1:8000' // 根据实际情况修改IP和端口
    };
  },
  mounted() {
    this.webRtcServer = new WebRtcStreamer('video', location.protocol + '//' + this.camera_ip);
    this.webRtcServer.connect('rtsp://admin:hk12345678@192.168.0.63:554/cam/realmonitor?channel=101&subtype=0');
  },
  beforeDestroy() {
    this.webRtcServer.disconnect();
    this.webRtcServer = null;
  }
};
</script>
```

### 5. 运行项目

启动您的Vue项目，并在浏览器中访问相应的页面，即可看到实时播放的RTSP视频流。

## 注意事项

- 确保您的RTSP视频流的编码格式为H264，否则可能无法正常播放。
- 如果遇到播放问题，请检查WebRTC服务的启动状态和网络连接。

## 参考资料

- [CSDN博客文章](https://blog.csdn.net/mullerpp/article/details/131741694)

通过以上步骤，您可以轻松地在Vue.js项目中实现RTSP视频流的实时播放。希望本资源文件对您有所帮助！

## 下载链接

[Vue实现RTSP视频流浏览器实时播放分享](https://pan.quark.cn/s/9c031e6a045f)