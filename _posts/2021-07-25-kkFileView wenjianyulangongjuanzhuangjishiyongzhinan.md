---
layout: post
title: "kkFileView 文件预览工具安装及使用指南"
date:   2024-04-12
tags: [预览,kkFileView,文件,在线,script]
comments: true
author: admin
---
# kkFileView 文件预览工具安装及使用指南

## 简介

kkFileView 是一个基于 Spring Boot 的文件文档在线预览解决方案，支持多种主流办公文档的在线预览，如 doc、docx、xls、xlsx、ppt、pptx、pdf、txt、zip、rar 等。它能够帮助用户在不下载文件的情况下直接在线预览文件内容，解决了文件格式兼容性和预览功能复杂性的问题。

## 功能特点

- **支持多种文件格式**：包括但不限于 doc、docx、xls、xlsx、ppt、pptx、pdf、txt、zip、rar 等。
- **易于部署**：使用 Spring Boot 框架搭建，部署简单快捷。
- **兼容性强**：解决了不同文件格式在预览时的兼容性问题。
- **开源免费**：遵循 Apache 2.0 开源协议，用户可以自由使用和修改。

## 安装步骤

### 1. 下载安装包

从本仓库下载 kkFileView 的安装包。

### 2. 解压安装包

将下载的安装包解压到指定目录。

### 3. 启动服务

- **Windows 系统**：
  1. 进入解压后的 `bin` 目录。
  2. 双击 `startup.bat` 启动 kkFileView。
  3. 30 秒后进入 `log` 目录查看日志，确认服务启动成功。

- **Linux 系统**：
  1. 将安装包上传到服务器。
  2. 使用命令 `tar -zxvf kkFileView-4.0.0.tar.gz` 解压。
  3. 进入解压后的 `bin` 目录，执行 `./startup.sh` 启动服务。
  4. 查看日志确认服务启动成功。

### 4. 配置修改

- **修改启动脚本**：如果预览 txt 文件出现乱码，可以在启动脚本中添加 `-Dfile.encoding=UTF-8` 参数。
- **关闭演示页面**：在 `application.properties` 配置文件中设置 `file.upload.disable=false` 以禁用演示首页文件上传。

## 使用方法

只需在 HTML 文件中添加以下代码即可实现文件在线预览：

```html
<html>
<head>
  <script type="text/javascript" src="https://cdn.jsdelivr.net/npm/js-base64@3.6.0/base64.min.js"></script>
</head>
<script>
  var url = '文件URL';
  window.open('http://127.0.0.1:8012/onlinePreview?url=' + encodeURIComponent(Base64.encode(url)));
</script>
</html>
```

## 注意事项

- 确保服务器上安装了必要的字体和 LibreOffice 组件，以避免预览时出现乱码或无法预览的问题。
- 如果遇到端口冲突或其他启动问题，请检查日志并根据提示进行相应处理。

## 结语

kkFileView 是一个功能强大且易于使用的文件在线预览工具，适用于各种需要在线预览文件的场景。通过本指南，您可以轻松完成 kkFileView 的安装和配置，并开始享受其带来的便捷预览体验。

## 下载链接

[kkFileView文件预览工具安装及使用指南](https://pan.quark.cn/s/bd1695b86528)