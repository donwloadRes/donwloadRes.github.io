---
layout: post
title: "解决Windows Server 2016无法安装NET 35"
date:   2022-02-28
tags: [Windows,NET,3.5,Framework,Name]
comments: true
author: admin
---
# 解决Windows Server 2016无法安装.NET 3.5

本文介绍如何解决在Windows Server 2016上无法安装.NET Framework 3.5的问题。通过以下步骤，您可以成功安装.NET 3.5，从而解决相关依赖问题。

## 方法一：通过命令行安装

1. 打开PowerShell并以管理员身份运行。
2. 输入以下命令并执行：
   ```powershell
   Set-ItemProperty -Path 'HKLM:\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate\AU' -Name UseWUServer -Value 0
   Restart-Service -Name wuauserv
   Install-WindowsFeature Net-Framework-Core
   Set-ItemProperty -Path 'HKLM:\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate\AU' -Name UseWUServer -Value 1
   Restart-Service -Name wuauserv
   ```

**注意**：此方法可能会失败，建议使用方法二。

## 方法二：离线安装

1. 下载.NET 3.5的cab包。
2. 将下载的文件拷贝到本地C:\Windows文件夹下。
3. 以管理员身份运行命令提示符，输入以下命令：
   ```cmd
   dism.exe /online /enable-feature /all /featurename:netfx3 /Source:c:\Windows
   ```
4. 出现成功提示后，重新在服务器管理器中安装.NET Framework 3.5。

通过以上步骤，您应该能够成功在Windows Server 2016上安装.NET Framework 3.5。如果仍有问题，请参考相关文档或寻求技术支持。

## 下载链接

[解决WindowsServer2016无法安装.NET3.5分享](https://pan.quark.cn/s/7e9e3ed5479d)