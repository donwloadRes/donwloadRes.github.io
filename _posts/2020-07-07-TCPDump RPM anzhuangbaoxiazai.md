---
layout: post
title: "TCPDump RPM 安装包下载"
date:   2024-11-15
tags: [rpm,tcpdump,安装,安装包,TCPDump]
comments: true
author: admin
---
# TCPDump RPM 安装包下载

本仓库提供了一个适用于 Linux 平台的 TCPDump 和 libpcap 的 RPM 安装包，方便用户在 CentOS 7 系统上快速安装和配置网络抓包工具。

## 资源文件

### 文件名
- `tcpdump rpm安装包.zip`

### 文件内容
- `tcpdump-4.5.1-2.el7.x86_64.rpm`：用于捕获网络上传输的数据包的抓包工具。
- `libpcap-1.5.3-12.el7.x86_64.rpm`：网络数据包捕获函数库，是 TCPDump 的依赖库。

## 安装说明

1. **下载文件**：
   下载 `tcpdump rpm安装包.zip` 文件到本地。

2. **解压缩**：
   使用以下命令解压缩文件：
   ```bash
   unzip tcpdump\ rpm安装包.zip
   ```

3. **安装 RPM 包**：
   依次安装 `libpcap` 和 `tcpdump` 的 RPM 包：
   ```bash
   sudo rpm -ivh libpcap-1.5.3-12.el7.x86_64.rpm
   sudo rpm -ivh tcpdump-4.5.1-2.el7.x86_64.rpm
   ```

4. **验证安装**：
   安装完成后，可以通过以下命令验证 TCPDump 是否安装成功：
   ```bash
   tcpdump --version
   ```

## 注意事项

- 请确保系统已安装 `unzip` 工具，如果没有安装，可以使用以下命令进行安装：
  ```bash
  sudo yum install unzip
  ```

- 安装过程中可能需要管理员权限，请确保以 `root` 用户或使用 `sudo` 执行安装命令。

## 支持与反馈

如果在安装或使用过程中遇到任何问题，欢迎通过仓库的 Issues 功能提出反馈。我们将尽力提供帮助。

## 下载链接

[TCPDumpRPM安装包下载](https://pan.quark.cn/s/37c12e1a3069)