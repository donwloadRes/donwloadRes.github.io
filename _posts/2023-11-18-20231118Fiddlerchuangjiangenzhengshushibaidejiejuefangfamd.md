---
layout: post
title: "Fiddler 创建根证书失败的解决方法"
date:   2024-06-06
tags: [Fiddler,证书,创建,HTTPS,失败]
comments: true
author: admin
---
# Fiddler 创建根证书失败的解决方法

在使用Fiddler进行网络抓包时，有时会遇到创建根证书失败的问题。本文将介绍两种解决方法，帮助你顺利创建根证书，确保Fiddler能够正常捕获HTTPS流量。

## 方法一：命令行

1. 打开命令提示符（CMD）并以管理员身份运行。
2. 进入Fiddler的安装目录。
3. 输入以下命令：
   ```
   makecert.exe -r -ss my -n "CN=DO_NOT_TRUST_FiddlerRoot, O=DO_NOT_TRUST, OU=Created by http://www.fiddler2.com" -sky signature -eku 1.3.6.1.5.5.7.3.1 -h 1 -cy authority -a sha1 -m 120 -b 10/12/2020
   ```
   注意：命令中的日期需要超过你安装软件的日期。

## 方法二：使用fiddlercertmaker.exe

1. 关闭Fiddler。
2. 下载并运行fiddlercertmaker.exe。
3. 重新打开Fiddler。
4. 在Fiddler中，依次点击`Tools` -> `Options` -> `HTTPS` -> `Decrypt HTTPS traffic` -> `Actions` -> `Trust Root Certificate`。

通过以上两种方法，你应该能够成功创建根证书，解决Fiddler创建根证书失败的问题。

## 下载链接

[Fiddler创建根证书失败的解决方法](https://pan.quark.cn/s/f98b9d7f249c)