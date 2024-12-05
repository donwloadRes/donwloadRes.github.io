---
layout: post
title: "freerdp编译文件wfreerdpexe"
date:   2021-01-06
tags: [wfreerdp,exe,freerdp,用户名,bash]
comments: true
author: admin
---
# freerdp编译文件wfreerdp.exe

## 简介
本仓库提供了一个编译后的freerdp可执行文件`wfreerdp.exe`，适用于Windows平台。freerdp是一个基于RDP（Remote Desktop Protocol）协议的开源项目，专门用于实现远程桌面连接。该资源文件包含了适用于win32和win64平台的编译结果，方便用户直接使用，无需自行编译源码。

## 资源文件说明
- **文件名**: `wfreerdp.exe`
- **平台**: 支持win32和win64
- **功能**: 实现基于RDP协议的远程桌面连接

## 常用参数说明
以下是`wfreerdp.exe`的一些常用参数示例：

1. **连接远程电脑**
   ```bash
   wfreerdp.exe /u:用户名 /v:目标主机地址
   ```

2. **连接远程电脑（无需输入密码）**
   ```bash
   wfreerdp.exe /u:用户名 /v:目标主机地址 /p:登陆密码
   ```

3. **设置远程桌面分辨率**
   ```bash
   wfreerdp.exe /u:用户名 /v:目标主机地址 /size:widthxheight
   ```

4. **挂载本地目录到远程电脑**
   ```bash
   wfreerdp.exe /u:用户名 /v:目标主机地址 /p:密码 /f /drive:home/home/用户名
   ```

5. **指定认证方式**
   ```bash
   wfreerdp.exe /u:用户名 /v:目标主机地址 /p:密码 /f /sec:rdp
   ```

## 注意事项
- 请确保目标主机已开启RDP服务。
- 使用时请根据实际情况调整参数。
- 该资源文件为编译后的可执行文件，适用于Windows平台。

## 贡献
如果您有任何改进建议或发现了问题，欢迎提交Issue或Pull Request。

## 许可证
本项目遵循freerdp的开源许可证，具体请参考freerdp项目的官方文档。

## 下载链接

[freerdp编译文件wfreerdp.exe](https://pan.quark.cn/s/516e1bb8b016)