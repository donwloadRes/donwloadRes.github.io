---
layout: post
title: "Faceapijs静态页面版Demo"
date:   2024-08-25
tags: [Demo,IIS,js,摄像头,localhost]
comments: true
author: admin
---
# Face-api.js静态页面版Demo

本仓库提供了一个基于JavaScript人脸识别库Face-api.js的静态页面版Demo。该Demo无需安装Node.js或其他服务器环境，只需在本地IIS服务器上运行即可直接查看效果。

## 主要特点

- **无需Node.js**：直接在IIS上运行，无需安装Node.js环境。
- **本地预览**：支持在本地localhost环境下预览，方便快速测试。
- **摄像头调用**：Demo中包含摄像头调用功能，但请注意，摄像头调用不能通过IP地址访问，必须使用localhost。
- **远程预览**：如果需要在远程服务器上预览，必须使用HTTPS协议。

## 使用说明

1. **下载资源文件**：下载本仓库中的资源文件，并将其放置在IIS服务器的根目录下。
2. **启动IIS**：在本地启动IIS服务器，确保资源文件能够被正确访问。
3. **访问Demo**：在浏览器中输入`http://localhost/`，即可访问Demo页面。

## 注意事项

- **摄像头调用限制**：由于浏览器的安全策略，摄像头调用只能在localhost环境下进行，不能通过IP地址访问。
- **IIS MIME类型配置**：如果IIS中无扩展名文件出现404错误，请在IIS的MIME类型中添加扩展名【.】类型【application/octet-stream】。

## 其他说明

本Demo仅供学习和测试使用，不建议用于生产环境。如有任何问题或建议，欢迎反馈。

## 下载链接

[Face-api.js静态页面版Demo](https://pan.quark.cn/s/aaa809536da4)