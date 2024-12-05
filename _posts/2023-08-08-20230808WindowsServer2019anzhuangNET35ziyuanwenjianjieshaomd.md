---
layout: post
title: "Windows Server 2019 安装 NET 35 资源文件介绍"
date:   2022-03-26
tags: [安装,NET,3.5,Windows,Server]
comments: true
author: admin
---
# Windows Server 2019 安装 .NET 3.5 资源文件介绍

本仓库提供了一个用于在 Windows Server 2019 上安装 .NET 3.5 的资源文件。该资源文件包含了安装 .NET 3.5 所需的必要组件和步骤，帮助用户在 Windows Server 2019 上顺利完成 .NET 3.5 的安装。

## 资源文件内容

- **Windows Server 2019 镜像文件**：包含 .NET 3.5 安装所需的源文件。
- **安装指南**：详细说明了如何在 Windows Server 2019 上安装 .NET 3.5。

## 安装步骤

1. **复制镜像文件**：将 Windows Server 2019 镜像文件复制到目标操作系统。
2. **打开服务器管理器**：右键点击“此电脑”，选择“管理”，然后以管理员权限打开服务器管理器。
3. **添加角色和功能**：
   - 点击“添加角色和功能”。
   - 按照向导提示，选择“基于功能或角色的安装”。
   - 在“选择功能”页面中，勾选“.NET Framework 3.5 功能”。
4. **指定备用源路径**：
   - 在安装过程中，设置“指定备用源路径”。
   - 填写源路径为镜像文件中的 `E:\Sources\SxS` 文件夹。
5. **安装**：点击“安装”，开始安装 .NET 3.5。

## 注意事项

- 确保在安装过程中保持稳定的网络连接。
- 如果安装过程中遇到问题，请参考提供的安装指南进行排查。

## 适用场景

本资源文件适用于需要在 Windows Server 2019 上安装 .NET 3.5 的用户，特别是那些无法通过常规方式安装 .NET 3.5 的用户。

## 贡献

如果您在使用过程中遇到问题或有改进建议，欢迎提交 Issue 或 Pull Request。

## 许可证

本资源文件遵循 [CC 4.0 BY-SA 版权协议](https://creativecommons.org/licenses/by-sa/4.0/)。

## 下载链接

[WindowsServer2019安装.NET3.5资源文件介绍](https://pan.quark.cn/s/11782c5ba3df)