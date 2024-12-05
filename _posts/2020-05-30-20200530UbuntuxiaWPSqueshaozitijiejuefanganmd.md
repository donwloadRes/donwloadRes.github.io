---
layout: post
title: "Ubuntu下WPS缺少字体解决方案"
date:   2020-02-29
tags: [字体,WPS,Office,ttf,Ubuntu]
comments: true
author: admin
---
# Ubuntu下WPS缺少字体解决方案

## 描述
在Ubuntu系统中安装WPS Office后，可能会遇到打开文档时提示缺少字体的错误，例如缺少以下字体：
- MTExtra.ttf
- webdings.ttf
- Wingdings 3.ttf
- symbol.ttf
- Wingdings 2.TTF
- Wingdings.ttf

本仓库提供了解决该问题的资源文件，包含上述缺失的字体文件。

## 使用方法
1. 下载本仓库中的字体文件。
2. 打开终端，进入字体文件所在的目录。
3. 执行以下命令将字体文件复制到WPS Office的字体目录中：
   ```bash
   cd wps-fonts/
   sudo cp * /usr/share/fonts/wps-office/
   ```
4. 重新启动WPS Office，问题应该已经解决。

## 注意事项
- 请确保在执行命令时具有管理员权限（使用`sudo`）。
- 如果WPS Office的字体目录不存在，可以手动创建该目录：
  ```bash
  sudo mkdir -p /usr/share/fonts/wps-office/
  ```

通过以上步骤，您应该能够成功解决Ubuntu下WPS Office缺少字体的问题。

## 下载链接

[Ubuntu下WPS缺少字体解决方案](https://pan.quark.cn/s/ecfc39ab95f8)