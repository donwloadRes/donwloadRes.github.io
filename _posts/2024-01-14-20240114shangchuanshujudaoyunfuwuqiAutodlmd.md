---
layout: post
title: "上传数据到云服务器Autodl"
date:   2022-10-01
tags: [上传,Autodl,服务器,WinScp,数据]
comments: true
author: admin
---
# 上传数据到云服务器Autodl

本文介绍了如何将数据上传到云服务器Autodl，提供了两种上传方法：使用JupyterLab直接上传数据和使用WinScp工具上传。

## 方法一：使用JupyterLab直接上传数据

这种方法只能以压缩包的形式上传数据。具体步骤如下：
1. 打开JupyterLab。
2. 选择要上传的压缩包文件。
3. 上传完成后，解压缩文件即可使用。

## 方法二：使用WinScp工具上传

这种方法可以直接上传文件夹，比较方便。具体步骤如下：
1. 确保云服务器已开机。
2. 复制实例的SSH指令，例如：`ssh -p 18256 root@region-42.seetacloud.com`。
3. 下载并安装WinScp工具。
4. 打开WinScp，点击新建会话，填写相关信息（文件协议选择SFTP）。
5. 点击登录，连接成功后即可上传数据。
6. 找到项目文件夹所在位置，直接拖动到对话框中即可上传成功。

通过以上两种方法，您可以轻松地将数据上传到云服务器Autodl，方便进行后续的数据处理和分析工作。

## 下载链接

[上传数据到云服务器Autodl](https://pan.quark.cn/s/2f2932c040de)