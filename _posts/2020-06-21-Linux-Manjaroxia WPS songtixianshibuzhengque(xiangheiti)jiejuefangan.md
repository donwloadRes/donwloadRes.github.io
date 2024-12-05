---
layout: post
title: "Linux-Manjaro下 WPS 宋体显示不正确(像黑体)解决方案"
date:   2024-04-17
tags: [宋体,字体,WPS,Linux,Manjaro]
comments: true
author: admin
---
# Linux/Manjaro下 WPS 宋体显示不正确(像黑体)解决方案

## 简介

在Linux/Manjaro系统下使用WPS Office时，可能会遇到宋体显示不正确的问题，表现为宋体字体显示为黑体。本资源文件提供了解决这一问题的方案。

## 解决方案

1. **下载Windows下的宋体字体**：
   - 从Windows系统中下载宋体字体文件（.ttf格式）。

2. **在Linux/Manjaro系统中安装字体**：
   - 将下载的字体文件复制到Linux/Manjaro系统的字体目录中。
   - 通常字体目录为 `/usr/share/fonts/` 或 `~/.fonts/`。

3. **更新字体缓存**：
   - 使用以下命令更新系统字体缓存：
     ```bash
     sudo fc-cache -fv
     ```

4. **重启WPS Office**：
   - 关闭并重新启动WPS Office，检查宋体字体是否显示正常。

## 注意事项

- 确保下载的字体文件是合法且安全的。
- 在安装字体时，可能需要管理员权限。

## 参考文章

本文解决方案参考自CSDN博客文章：[Linux/Manjaro下 WPS 宋体显示不正确(像黑体)解决方案](https://blog.csdn.net/weixin_36349646/article/details/102643110)。

---

通过以上步骤，您应该能够解决Linux/Manjaro系统下WPS Office宋体显示不正确的问题。

## 下载链接

[LinuxManjaro下WPS宋体显示不正确像黑体解决方案分享](https://pan.quark.cn/s/c1e97ccdfb98)