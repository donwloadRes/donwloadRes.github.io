---
layout: post
title: "目录扫描工具dirsearch与御剑的安装与介绍"
date:   2020-10-09
tags: [dirsearch,扫描,目录,御剑,文件]
comments: true
author: admin
---
# 目录扫描工具dirsearch与御剑的安装与介绍

本文将详细介绍两个常用的目录扫描工具：dirsearch和御剑的安装步骤与基本使用方法。

## dirsearch

### 介绍
dirsearch是一个使用Python语言开发的目录扫描工具，主要用于扫描Web应用中的敏感文件和目录，查找潜在的安全漏洞。它支持多线程扫描、多种文件后缀（如ASP、PHP等）、生成报告（纯文本或JSON格式）、暴力扫描、HTTP代理、用户代理随机化等功能。

### 安装步骤
1. 下载dirsearch的最新版本，下载地址为：https://github.com/maurosoria/dirsearch/archive/refs/heads/master.zip。
2. 解压下载的文件，进入dirsearch-master文件夹。
3. 在命令行中输入以下命令安装所需依赖：
   ```
   pip install -r requirements.txt
   ```
4. 安装完成后，即可开始使用dirsearch。

### 使用方法
以下是一些常用的参数和使用示例：
- `-u`：指定要扫描的网址，例如 `http://www.xxx.com/`。
- `-l`：指定URL字典。
- `-e`：指定网站后端开发语言，如PHP、ASP、JSP等。
- `-w`：指定字典文件，如果不指定，默认使用db目录下的dicc.txt。
- `-r`：递归扫描目录。
- `--random-agent`：使用随机User-Agent。
- `-o`：输出扫描报告。
- `-X`：排除特定状态代码，如404、400等。
- `-i`：指定要显示的状态代码，如404、300-399等。
- `-t`：设置线程数。

示例：
```
python dirsearch.py -u http://example.com -e php,asp -r
```

## 御剑

### 介绍
御剑是一个自动扫描网站目录的工具，能够发现隐藏的文件和目录。它具有简洁易懂的GUI界面，并附带强大的字典，用户可以自行修改和增加规则。

### 安装步骤
1. 下载御剑的最新版本，下载地址为：御剑珍藏版。
2. 解压下载的文件。
3. 双击打开御剑后台扫描工具.exe，此时字典是空的。
4. 将御剑配置文件zip中的txt文件解压到配置文件文件夹中。
5. 重新打开御剑，即可正常使用。

### 使用方法
御剑的扫描速度快，字典丰富，适合快速发现网站的敏感目录和文件。

## 总结
dirsearch和御剑都是强大的目录扫描工具，适用于网络安全测试和漏洞挖掘。通过本文的介绍，您可以轻松安装和使用这两个工具，提升您的安全测试能力。

## 下载链接

[目录扫描工具dirsearch与御剑的安装与介绍](https://pan.quark.cn/s/cf5c3bbc9e73)