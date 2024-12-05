---
layout: post
title: "Wireshark 网络抓包资源文件"
date:   2023-05-16
tags: [Wireshark,抓包,文件,cap,-%]
comments: true
author: admin
---
# Wireshark 网络抓包资源文件

## 资源文件介绍

本仓库提供了一个名为 `Wireshark.rar` 的资源文件，该文件包含了通过 Wireshark 工具抓取的网络数据包。具体抓包命令如下：

```bash
tcpdump port 8080 -i enp3s0 -s0 -G 3600 -w %Y-%m%d-%H.cap &
```

### 抓包参数说明

- **网卡名称**：`enp3s0`
- **端口**：`8080`
- **抓包时长**：每小时生成一个 `.cap` 文件，文件名格式为 `%Y-%m%d-%H.cap`，例如 `2023-1001-14.cap` 表示 2023 年 10 月 1 日 14 时的抓包数据。

## 使用说明

1. **下载资源文件**：
   - 点击仓库中的 `Wireshark.rar` 文件进行下载。

2. **解压文件**：
   - 下载完成后，使用解压工具（如 WinRAR 或 7-Zip）解压 `Wireshark.rar` 文件。

3. **查看抓包数据**：
   - 解压后，您将看到多个 `.cap` 文件，这些文件包含了在指定网卡和端口上抓取的网络数据包。
   - 使用 Wireshark 或其他支持 `.cap` 格式的网络分析工具打开这些文件，即可查看详细的网络流量数据。

## 注意事项

- 请确保您有合法的权限进行网络抓包操作。
- 抓包数据可能包含敏感信息，请妥善保管和处理。

## 联系我们

如果您在使用过程中遇到任何问题或有任何建议，欢迎通过仓库的 Issues 功能联系我们。

## 下载链接

[Wireshark网络抓包资源文件](https://pan.quark.cn/s/e9cce06b2273)