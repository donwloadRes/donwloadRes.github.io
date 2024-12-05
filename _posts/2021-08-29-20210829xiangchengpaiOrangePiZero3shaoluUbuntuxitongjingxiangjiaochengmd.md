---
layout: post
title: "香橙派 Orange Pi Zero 3 烧录 Ubuntu 系统镜像教程"
date:   2021-12-17
tags: [烧录,香橙,Ubuntu,镜像,Orange]
comments: true
author: admin
---
# 香橙派 Orange Pi Zero 3 烧录 Ubuntu 系统镜像教程

本资源文件提供了如何在香橙派 Orange Pi Zero 3 上烧录 Ubuntu 系统镜像的详细教程。无需使用 HDMI 数据线，即可完成系统的安装。

## 资源内容

- **Ubuntu 系统镜像**：适用于香橙派 Orange Pi Zero 3 的 Ubuntu 系统镜像文件。
- **balenaEtcher 软件**：用于烧录镜像的工具。
- **USB 转 TTL 模块**：用于调试和查看系统输出信息。

## 安装步骤

1. **下载 Ubuntu 镜像**：
   - 从提供的链接下载适用于香橙派 Orange Pi Zero 3 的 Ubuntu 系统镜像。
   - 解压下载的压缩包，生成 `.img` 文件。

2. **下载 balenaEtcher 软件**：
   - 下载并安装 balenaEtcher 软件。
   - 以管理员身份运行 balenaEtcher。

3. **烧录镜像**：
   - 打开 balenaEtcher，选择“从文件烧录”。
   - 选择解压后的 `.img` 文件，并选择 TF 卡作为目标磁盘。
   - 点击“现在烧录”，等待烧录完成。

4. **启动系统**：
   - 烧录完成后，弹出 TF 卡并插入香橙派 Orange Pi Zero 3 开发板。
   - 使用 USB 转 TTL 模块连接开发板和电脑，查看调试输出信息。

## 注意事项

- 确保 TF 卡容量至少为 8GB，并且是 class10 级或以上的高速卡。
- 如果使用 USB 转 TTL 模块查看调试信息，请确保正确连接并安装相关驱动。

## 参考资料

- 本教程参考了香橙派官方开发手册的相关步骤。

通过以上步骤，您可以成功在香橙派 Orange Pi Zero 3 上烧录并启动 Ubuntu 系统。

## 下载链接

[香橙派OrangePiZero3烧录Ubuntu系统镜像教程](https://pan.quark.cn/s/8b925044197b)