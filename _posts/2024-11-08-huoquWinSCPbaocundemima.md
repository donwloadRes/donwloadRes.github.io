---
layout: post
title: "获取WinSCP保存的密码"
date:   2020-10-01
tags: [WinSCP,密码,工具,ini,保存]
comments: true
author: admin
---
# 获取WinSCP保存的密码

本资源文件提供了一个工具，用于获取WinSCP中保存的密码。WinSCP是一款常用的SFTP、SCP和FTP客户端，用户在使用过程中可以选择保存密码以便下次登录。然而，保存的密码是经过加密的，如果用户忘记了密码，可以使用本工具来解密并查看保存的密码。

## 使用方法

1. **下载工具**：首先，下载本资源文件中提供的Winscppwd工具。
2. **导出WinSCP配置文件**：在WinSCP中，导出站点信息到`WinSCP.ini`文件。
3. **运行工具**：打开命令提示符（CMD），进入Winscppwd工具所在的目录，输入以下命令：
   ```
   Winscppwd D:\develope\winSCP2\WinSCP.ini
   ```
   其中，`D:\develope\winSCP2\WinSCP.ini`是你的`WinSCP.ini`文件路径。
4. **查看密码**：运行命令后，工具将显示所有保存过的IP地址及其对应的密码。

## 注意事项

- 请确保你拥有合法的权限来访问和解密这些密码。
- 本工具仅供学习和研究使用，请勿用于非法用途。

## 相关资源

- 更多关于WinSCP的使用和配置，请参考WinSCP官方文档。
- 如果你有任何问题或建议，欢迎在评论区留言。

---

希望本工具能帮助你解决忘记WinSCP密码的问题。如果有任何疑问，请随时联系我们。

## 下载链接

[获取WinSCP保存的密码分享](https://pan.quark.cn/s/04bc44634b14)