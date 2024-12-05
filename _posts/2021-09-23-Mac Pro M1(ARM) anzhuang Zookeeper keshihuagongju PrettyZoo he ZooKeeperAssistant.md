---
layout: post
title: "Mac Pro M1(ARM) 安装 Zookeeper 可视化工具 PrettyZoo 和 ZooKeeperAssistant"
date:   2021-03-23
tags: [Zookeeper,PrettyZoo,安装,ZooKeeperAssistant,可视化]
comments: true
author: admin
---
# Mac Pro M1(ARM) 安装 Zookeeper 可视化工具 PrettyZoo 和 ZooKeeperAssistant

## 简介

本资源文件提供了在 Mac Pro M1(ARM) 上安装 Zookeeper 可视化工具 PrettyZoo 和 ZooKeeperAssistant 的详细步骤。通过这些工具，用户可以更方便地管理和监控 Zookeeper 集群。

## 安装步骤

### 1. 安装 PrettyZoo

1. **下载**：从 GitHub 选择适合 Mac M1 的版本进行下载。如果访问 GitHub 有困难，可以使用提供的网盘地址下载安装包。
2. **安装**：下载完成后，双击安装包进行安装。
3. **打开 PrettyZoo**：安装完成后，打开 PrettyZoo。可能会提示“PrettyZoo 已损坏，无法打开”。
4. **解决安全提示**：进入系统偏好设置 -> 安全性与隐私 -> 通用，检查是否有“任何来源”选项。如果没有，打开终端，输入以下指令并输入密码：
   ```
   sudo spctl --master-disable
   ```
5. **再次打开 PrettyZoo**：设置为“任何来源”后，再次打开 PrettyZoo，选择“打开”。
6. **新建连接**：点击“New”新建一个连接，输入 Zookeeper 的地址和端口，点击“Save”保存。
7. **连接 Zookeeper**：双击新建的连接，即可连接到 Zookeeper 并查看已注册的服务。

### 2. 安装 ZooKeeperAssistant

1. **下载安装包**：访问提供的下载地址，选择适合的版本进行下载。
2. **安装**：下载后双击安装包进行安装。
3. **打开 ZooKeeperAssistant**：安装完成后，打开软件，输入 Zookeeper 的地址和端口进行连接。
4. **查看服务**：在服务栏中可以清楚地看到已注册的服务数。

## 注意事项

- PrettyZoo 是免费的，而 ZooKeeperAssistant 是收费的，但提供了更好的可视化界面。
- 在安装过程中遇到任何问题，可以参考提供的文章进行解决。

## 总结

通过本资源文件，用户可以轻松地在 Mac Pro M1(ARM) 上安装并使用 PrettyZoo 和 ZooKeeperAssistant 这两款 Zookeeper 可视化工具，提升 Zookeeper 集群的管理效率。

## 下载链接

[MacProM1ARM安装Zookeeper可视化工具PrettyZoo和ZooKeeperAssistant分享](https://pan.quark.cn/s/5b1d4980dcbc)