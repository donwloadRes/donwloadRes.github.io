---
layout: post
title: "解决GitHub打不开问题FastGithub支持MAC"
date:   2020-09-20
tags: [FastGithub,GitHub,IP,访问,双击]
comments: true
author: admin
---
# 解决GitHub打不开问题（FastGithub，支持MAC）

## 简介

本仓库提供了一个解决方案，帮助用户解决GitHub无法访问的问题。通过使用FastGithub工具，用户可以在Windows、Linux和Mac操作系统上顺畅访问GitHub。

## 工作原理

FastGithub通过从公共DNS服务器获取GitHub的大量IP数据，检测哪些IP可用且访问速度最佳，然后编写一个本地版的DNS服务。当用户尝试解析GitHub相关域名时，FastGithub会返回最佳IP，从而解决GitHub访问不稳定的问题。

## 使用方法

### 1. 下载FastGithub

从本仓库下载FastGithub工具。

### 2. 安装与配置

#### Windows
- 解压后直接双击运行`FastGithub UI.exe`，自带图形界面。

#### Mac
- 双击运行`fastgithub`，安装`cacert/fastgithub.cer`并设置信任。
- 设置系统自动代理为`http://127.0.0.1:38457`，或手动代理HTTP/HTTPS为`127.0.0.1:38457`。

### 3. 验证安装

运行FastGithub后，打开浏览器访问GitHub，确认是否能够正常访问。

## 注意事项

- FastGithub不具备“翻墙”功能，也没有相关的计划。
- FastGithub不支持加速其他软件或游戏。

## 贡献

欢迎提交问题和建议，帮助改进本解决方案。

## 许可证

本项目遵循CC 4.0 BY-SA版权协议。

## 下载链接

[解决GitHub打不开问题FastGithub支持MAC](https://pan.quark.cn/s/0044c5807b58)