---
layout: post
title: "解决win10上“RDP Wrapper不支持”的问题"
date:   2022-08-24
tags: [Windows,RDP,Wrapper,ini,版本]
comments: true
author: admin
---
# 解决win10上“RDP Wrapper不支持”的问题

此资源提供了详尽的指南，专门用于解决在Windows 10操作系统中遇到的RDP Wrapper显示“Not supported”错误的情况。RDP Wrapper是一款允许您在非企业版Windows系统上启用多用户远程桌面连接的工具，但经常因版本兼容性问题导致上述错误。以下是修复步骤的概览，基于[CSDN博客](https://blog.csdn.net/sanqima/article/details/117251038)提供的解决方案。

## 步骤概述

### 1. 停止Remote Desktop Services
首先，你需要通过命令行暂停 Remote Desktop Services。打开命令提示符（以管理员身份运行），输入以下命令：
```shell
net stop termservice
```

### 2. 更新rdpwrap.ini文件
问题通常源于`rdpwrap.ini`文件没有列出您当前系统中`termsrv.dll`的正确版本。您需要找到匹配您系统版本的`rdpwrap.ini`更新文件，并将其覆盖原始文件。备份现有`rdpwrap.ini`至`rdpwrap.ini.bk`，然后使用提供的更新文件。注意，更新文件需对应您的Windows 10具体构建版本。

### 3. 重新启动Remote Desktop Services
完成 ini 文件替换后，在命令提示符中执行：
```shell
net start termservice
```
以重新启动服务。

### 4. 验证状态
通过RDPConf.exe检查RDP Wrapper的状态，确保已解决“Not supported”问题，并变为“Fully supported”。

### 注意事项
- **版本兼容性**：确认您的Windows 10版本，并查找对应的`termsrv.dll`版本号。
- **文件版本号**：位于C:\Windows\System32中的`termsrv.dll`文件属性可查看版本号，确保ini文件中有相应的条目。
- **持续更新**：Windows定期更新可能会引入新的版本号，因此保持RDP Wrapper的更新至关重要。

通过以上步骤，您可以成功解决RDP Wrapper显示的“Not supported”错误，从而在您的Win10系统上恢复远程桌面功能。对于不同Windows 10的构建版本，可能需要特定的配置，务必参照最新的文档或更新资源。

## 下载链接

[解决win10上RDPWrapper不支持的问题分享](https://pan.quark.cn/s/51fad318cca3)