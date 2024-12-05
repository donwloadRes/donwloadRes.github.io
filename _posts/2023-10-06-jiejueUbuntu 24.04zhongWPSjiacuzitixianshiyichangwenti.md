---
layout: post
title: "解决Ubuntu 24.04中WPS加粗字体显示异常问题"
date:   2022-07-26
tags: [WPS,加粗,Office,字体,文件]
comments: true
author: admin
---
# 解决Ubuntu 24.04中WPS加粗字体显示异常问题

本资源文件旨在帮助解决在Ubuntu 24.04系统中使用WPS Office时遇到的加粗字体显示异常问题。该问题表现为WPS中的加粗字体显示为模糊或不清晰，影响文档的阅读和编辑体验。

## 问题描述

在Ubuntu 24.04系统中，WPS Office中的加粗字体可能会显示为模糊或不清晰，尤其是在使用某些字体时，这一问题尤为明显。这不仅影响了文档的美观，还可能对用户的工作效率造成影响。

## 解决方案

本资源文件提供了两种解决方案，用户可以根据自己的需求选择其中一种进行操作。

### 方法一：降级libfreetype6库

1. 下载libfreetype6_2.11.1+dfsg-1build1_amd64.deb文件。
2. 在下载目录中运行以下命令进行安装：
   ```
   sudo dpkg -i libfreetype6_2.11.1+dfsg-1build1_amd64.deb
   ```
3. 此方法的缺点是每次系统更新后可能会失效，需要重新安装。

### 方法二：替换WPS Office中的libfreetype库

1. 解压缩libfreetype6_2.11.1+dfsg-1build1_amd64.deb文件。
2. 在解压缩的文件夹中找到`/usr/lib/x86_64-linux-gnu/`文件夹，该文件夹中应包含两个文件：一个实体文件和一个文件软链接。
3. 将这两个文件拷贝到`/opt/kingsoft/wps-office/office6`目录下。
4. 此方法的缺点是升级WPS Office时可能会失效，需要重新操作。

## 注意事项

- 在进行任何操作之前，建议备份重要数据，以防操作失误导致数据丢失。
- 如果选择方法一，建议在每次系统更新后检查是否需要重新安装libfreetype6库。
- 如果选择方法二，建议在每次WPS Office升级后检查是否需要重新替换libfreetype库。

通过以上方法，用户可以有效解决Ubuntu 24.04中WPS Office加粗字体显示异常的问题，提升文档编辑和阅读的体验。

## 下载链接

[解决Ubuntu24.04中WPS加粗字体显示异常问题](https://pan.quark.cn/s/919b987b106c)