---
layout: post
title: "Win10 离线安装 .NET Framework 3.5 的方法及离线安装包"
date:   2022-12-26
tags: [NET,离线,Framework,3.5,NetFx3.5]
comments: true
author: admin
---
# Win10 离线安装 .NET Framework 3.5 的方法及离线安装包

## 简介

在某些情况下，您可能需要在 Windows 10 系统中离线安装 .NET Framework 3.5。本文将详细介绍如何在 Windows 10 中离线安装 .NET Framework 3.5，并提供离线安装包 `NetFx3.5.cab` 供您下载使用。

## 安装方法

### 1. 下载离线安装包

首先，您需要下载 `NetFx3.5.cab` 文件。您可以从本仓库的 `resources` 目录中找到并下载该文件。

### 2. 安装 .NET Framework 3.5

1. **打开“控制面板”**：
   - 按 `Win + R` 键，输入 `control`，然后按回车键打开控制面板。

2. **进入“程序和功能”**：
   - 在控制面板中，点击“程序”，然后选择“启用或关闭 Windows 功能”。

3. **勾选 .NET Framework 3.5**：
   - 在弹出的窗口中，找到并勾选 `.NET Framework 3.5 (包括 .NET 2.0 和 3.0)` 选项。
   - 点击“确定”按钮。

4. **指定离线安装包路径**：
   - 系统会提示您需要下载并安装 .NET Framework 3.5。此时，点击“从 Windows 更新下载文件”旁边的“指定备用源路径”链接。
   - 在弹出的窗口中，输入 `NetFx3.5.cab` 文件的路径，例如 `C:\path\to\NetFx3.5.cab`。
   - 点击“确定”按钮，系统将开始安装 .NET Framework 3.5。

5. **完成安装**：
   - 安装完成后，系统会提示您重启计算机。重启后，.NET Framework 3.5 将成功安装并启用。

## 注意事项

- 确保您下载的 `NetFx3.5.cab` 文件路径正确，否则安装过程可能会失败。
- 如果您在安装过程中遇到任何问题，请检查系统日志或尝试重新下载 `NetFx3.5.cab` 文件。

## 资源下载

您可以从本仓库的 `resources` 目录中下载 `NetFx3.5.cab` 文件。

## 贡献

如果您有任何改进建议或发现了问题，欢迎提交 Issue 或 Pull Request。

## 许可证

本项目采用 MIT 许可证。有关更多信息，请参阅 [LICENSE](LICENSE) 文件。

---

希望本文对您有所帮助！如果您有任何问题，请随时联系我们。

## 下载链接

[Win10离线安装.NETFramework3.5的方法及离线安装包](https://pan.quark.cn/s/3143e3441964)