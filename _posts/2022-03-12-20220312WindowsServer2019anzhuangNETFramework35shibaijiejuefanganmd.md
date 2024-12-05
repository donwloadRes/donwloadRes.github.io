---
layout: post
title: "Windows Server 2019 安装 NET Framework 35 失败解决方案"
date:   2021-01-29
tags: [Windows,安装,NET,Framework,3.5]
comments: true
author: admin
---
# Windows Server 2019 安装 NET Framework 3.5 失败解决方案

## 简介
本资源文件提供了解决 Windows Server 2019 安装 NET Framework 3.5 失败的问题。当您在安装 NET Framework 3.5 时遇到错误提示“安装一个或多个角色、角色服务或功能失败”，本文将为您提供详细的解决方案。

## 问题描述
在 Windows Server 2019 中，尝试安装 NET Framework 3.5 时，可能会遇到以下错误提示：
- “安装一个或多个角色、角色服务或功能失败”

## 解决方案
以下是解决该问题的步骤：

1. **使用离线安装包**：
   - 下载 NET Framework 3.5 的离线安装包。
   - 将安装包放置在服务器上，并使用命令行工具进行安装。

2. **修改注册表**：
   - 打开注册表编辑器（regedit）。
   - 导航到 `HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate\AU`。
   - 删除 `AUOptions` 键值。

3. **使用 DISM 工具**：
   - 打开命令提示符（以管理员身份运行）。
   - 输入以下命令并执行：
     ```
     DISM /Online /Enable-Feature /FeatureName:NetFx3 /All /LimitAccess /Source:C:\sources\sxs
     ```
   - 确保 `C:\sources\sxs` 路径正确，并包含所需的安装文件。

4. **检查系统更新**：
   - 确保 Windows Server 2019 已安装所有可用的系统更新。
   - 运行 Windows Update 并安装所有推荐的更新。

5. **重启服务器**：
   - 完成上述步骤后，重启服务器以确保更改生效。

## 结论
通过以上步骤，您应该能够成功解决 Windows Server 2019 安装 NET Framework 3.5 失败的问题。如果问题仍然存在，请检查系统日志以获取更多详细信息，并根据日志提示进行进一步的故障排除。

## 下载链接

[WindowsServer2019安装NETFramework3.5失败解决方案](https://pan.quark.cn/s/bea19936a44d)