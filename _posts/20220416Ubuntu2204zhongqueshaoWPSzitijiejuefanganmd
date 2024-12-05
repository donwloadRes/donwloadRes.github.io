---
layout: post
title: "Ubuntu 22.04 中缺少 WPS 字体解决方案"
date:   2024-03-12
tags: [字体,WPS,sudo,fonts,文件]
comments: true
author: admin
---
# Ubuntu 22.04 中缺少 WPS 字体解决方案

## 简介

在 Ubuntu 22.04 或其他 Linux 系统下安装 WPS 软件后，每次打开时可能会提示缺少某些字体，如 Symbol、Wingdings 等。本资源文件提供了解决这一问题的详细步骤和所需的字体文件。

## 解决方案

### 1. 下载字体文件

首先，从本仓库下载 `wps_symbol_fonts.zip` 文件，该文件包含了 WPS 所需的所有缺失字体。

### 2. 解压缩字体文件

将下载的 `wps_symbol_fonts.zip` 文件解压缩到任意目录。

### 3. 安装字体

打开终端，执行以下命令将字体文件复制到系统字体目录：

```bash
sudo cp *ttf *TTF /usr/share/fonts
```

### 4. 生成字体索引

继续在终端中执行以下命令，生成字体索引：

```bash
sudo mkfontscale
sudo mkfontdir
```

### 5. 更新字体缓存

最后，更新字体缓存：

```bash
sudo fc-cache
```

### 6. 重启 WPS

完成上述步骤后，重启 WPS Office，此时应该不会再提示缺少字体。

## 注意事项

- 确保在执行命令时具有管理员权限（使用 `sudo`）。
- 如果 WPS 仍然提示缺少字体，请检查字体文件是否正确复制到 `/usr/share/fonts` 目录。

## 参考

本解决方案参考了 CSDN 博客文章，详细步骤和更多信息请参阅原文。

---

通过以上步骤，您可以轻松解决 Ubuntu 22.04 中 WPS Office 缺少字体的问题，确保软件正常运行。

## 下载链接

[Ubuntu22.04中缺少WPS字体解决方案分享](https://pan.quark.cn/s/3d864eb9bef8)