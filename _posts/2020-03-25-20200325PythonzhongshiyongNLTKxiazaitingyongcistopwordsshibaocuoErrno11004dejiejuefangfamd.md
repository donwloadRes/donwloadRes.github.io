---
layout: post
title: "Python中使用NLTK下载停用词stopwords时报错 Errno 11004 的解决方法"
date:   2022-04-07
tags: [stopwords,NLTK,nltk,用词,下载]
comments: true
author: admin
---
# Python中使用NLTK下载停用词（stopwords）时报错 [Errno 11004] 的解决方法

在使用Python的NLTK库下载停用词（stopwords）时，有时会遇到`[Errno 11004]`错误。本文将详细介绍该错误的常见原因以及解决方法，帮助你顺利完成停用词的下载。

## 错误描述

在使用NLTK下载停用词时，可能会遇到如下错误信息：
```
[Errno 11004] getaddrinfo failed
```
该错误通常是由于网络连接问题或NLTK库无法正确解析域名导致的。

## 解决方法

### 方法一：检查网络连接

首先，确保你的网络连接正常，并且能够访问外部网站。你可以尝试打开其他网页或使用其他网络工具来确认网络连接是否正常。

### 方法二：手动下载停用词

如果网络连接正常，但仍然遇到该错误，可以尝试手动下载停用词文件。具体步骤如下：

1. 打开浏览器，访问NLTK的停用词下载页面：[https://raw.githubusercontent.com/nltk/nltk_data/gh-pages/packages/corpora/stopwords.zip](https://raw.githubusercontent.com/nltk/nltk_data/gh-pages/packages/corpora/stopwords.zip)
2. 下载`stopwords.zip`文件并解压缩。
3. 将解压后的`stopwords`文件夹放置在你的Python项目目录中，或者放置在NLTK的数据目录中（通常位于`C:\nltk_data\corpora\`）。

### 方法三：修改NLTK下载路径

如果手动下载仍然无法解决问题，可以尝试修改NLTK的下载路径。具体步骤如下：

1. 在Python代码中，使用以下代码指定停用词的下载路径：
   ```python
   import nltk
   nltk.data.path.append('/path/to/your/stopwords/directory')
   ```
2. 将`/path/to/your/stopwords/directory`替换为你存放停用词文件夹的实际路径。

### 方法四：使用代理服务器

如果你所在的网络环境需要通过代理服务器访问外部网站，可以尝试配置代理服务器。具体步骤如下：

1. 在Python代码中，使用以下代码配置代理服务器：
   ```python
   import nltk
   import urllib.request

   proxy_support = urllib.request.ProxyHandler({'http': 'http://your_proxy:port', 'https': 'https://your_proxy:port'})
   opener = urllib.request.build_opener(proxy_support)
   urllib.request.install_opener(opener)

   nltk.download('stopwords')
   ```
2. 将`your_proxy`和`port`替换为你的代理服务器地址和端口号。

## 总结

通过以上方法，你应该能够解决在Python中使用NLTK下载停用词时遇到的`[Errno 11004]`错误。如果问题仍然存在，建议检查你的网络配置或联系网络管理员以获取进一步帮助。

## 下载链接

[Python中使用NLTK下载停用词stopwords时报错Errno11004的解决方法](https://pan.quark.cn/s/2c7afc0fdd19)