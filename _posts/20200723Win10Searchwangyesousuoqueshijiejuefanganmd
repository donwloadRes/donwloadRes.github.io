---
layout: post
title: "Win10 Search 网页搜索缺失解决方案"
date:   2021-02-12
tags: [搜索,Windows,回车,网页,禁用]
comments: true
author: admin
---
# Win10 Search 网页搜索缺失解决方案

## 简介
本资源文件提供了一个完整的解决方案，用于修复Windows 10系统中搜索功能缺失网页搜索的问题。通过执行提供的脚本和相关步骤，用户可以恢复搜索功能的完整性，确保能够正常进行网页搜索。

## 解决方案步骤

### 准备工作
1. **确保Windows Search服务正在运行**：
   - 快捷键 `Win+R` > 输入 `services.msc`
   - 确认Windows Search服务已启动。

2. **打开组策略**：
   - 快捷键 `Win+R` > 输入 `gpedit.msc`
   - 定位到：计算机配置 > 管理模板 > Windows 组件 > 搜索
   - 在右侧窗口中禁用下列三项：
     - 禁用“不允许Web搜索”
     - 禁用“不允许搜索框建议”
     - 禁用“不允许Cortana”

### 主要操作
1. **下载重置脚本**：
   - 下载 `ResetWindowsSearchBox.ps1` 脚本。

2. **运行脚本**：
   - 打开Windows PowerShell（非管理员模式）。
   - 将下载的 `ResetWindowsSearchBox.ps1` 文件拖入PowerShell窗口，敲两次回车。
   - 如果出现“无法加载文件……”提示，输入以下命令：
     ```powershell
     Get-ExecutionPolicy
     ```
     回车后会出现 `Restricted` 提示，然后输入：
     ```powershell
     Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy Unrestricted
     ```
     回车后选择“全是”即输入 `A` 回车。
   - 再次将 `ResetWindowsSearchBox.ps1` 文件拖入PowerShell窗口，敲两次回车。
   - 等待完成直到出现 `Press any key to continue…`，最后关闭窗口，重启电脑。

## 注意事项
- 如果系统为Windows 10家庭版，可能没有组策略功能，可直接跳过组策略步骤，验证结果是否可行。
- 确保在执行脚本时，系统没有其他重要任务运行，以免影响操作。

## 结论
通过上述步骤，用户可以有效解决Windows 10搜索功能缺失网页搜索的问题，恢复搜索功能的完整性。

## 下载链接

[Win10Search网页搜索缺失解决方案](https://pan.quark.cn/s/497289120da1)