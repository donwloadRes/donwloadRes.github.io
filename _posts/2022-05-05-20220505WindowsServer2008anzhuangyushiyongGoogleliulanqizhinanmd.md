---
layout: post
title: "Windows Server 2008 安装与使用 Google 浏览器指南
date   20230716
tags Google浏览器WindowsServer2008
comments true
author admin

 Windows Server 2008 安装与使用 Google 浏览器指南

本文档详细介绍了在 Windows Server 2008 操作系统上安装和使用 Google 浏览器的过程并记录了在此过程中遇到的问题及其解决方法

 内容概述

1 安装前的准备
    由于 Windows Server 2008 系统较老大多数版本的 Google 浏览器已不再适配因此在安装前需要找到一个合适的版本
    作者通过询问 ChatGPT 并尝试下载了较低版本的 Google 浏览器版本 39 和 40但均遇到安装后无法正常启动的问题

2 问题与解决
    问题描述安装好的 Google 浏览器在启动时提示已停止工作
    解决方法通过修改快捷方式的目标参数解决了时钟快了的问题具体操作是将目标参数修改为
     
     CUsersAdministratorDesktopGoogleChromePortableAppGoogle Chromechromeexe ignorecertificateerrors allowrunninginsecurecontent diskcachedirCUsersADMINI1AppDataLocalTemp2ChromePortable"
date:   2023-07-16
tags: [Google,浏览器,Windows,Server,2008]
comments: true
author: admin
---
# Windows Server 2008 安装与使用 Google 浏览器指南

本文档详细介绍了在 Windows Server 2008 操作系统上安装和使用 Google 浏览器的过程，并记录了在此过程中遇到的问题及其解决方法。

## 内容概述

1. **安装前的准备**
   - 由于 Windows Server 2008 系统较老，大多数版本的 Google 浏览器已不再适配，因此在安装前需要找到一个合适的版本。
   - 作者通过询问 ChatGPT 并尝试下载了较低版本的 Google 浏览器（版本 39 和 40），但均遇到安装后无法正常启动的问题。

2. **问题与解决**
   - **问题描述**：安装好的 Google 浏览器在启动时提示“已停止工作”。
   - **解决方法**：通过修改快捷方式的目标参数，解决了时钟快了的问题。具体操作是将目标参数修改为：
     ```
     "C:\Users\Administrator\Desktop\GoogleChromePortable\App\Google Chrome\chrome.exe" --ignore-certificate-errors --allow-running-insecure-content --disk-cache-dir="C:\Users\ADMINI~1\AppData\Local\Temp\2\ChromePortable"
     ```

3. **总结**
   - 本文档提供了一个在 Windows Server 2008 上成功安装和使用 Google 浏览器的解决方案，特别是针对时钟快了的问题进行了详细说明。

## 使用说明

- 下载并安装 Google 浏览器时，请确保选择合适的版本。
- 如果遇到启动问题，请按照上述方法修改快捷方式的目标参数。

## 注意事项

- 由于 Windows Server 2008 系统较老，部分新版本的 Google 浏览器可能无法正常运行，建议使用较旧的稳定版本。
- 修改快捷方式参数时，请确保路径和参数正确无误。

希望本文档能帮助您在 Windows Server 2008 上顺利安装和使用 Google 浏览器。

## 下载链接

[WindowsServer2008安装与使用Google浏览器指南](https://pan.quark.cn/s/ef8152eaa086)