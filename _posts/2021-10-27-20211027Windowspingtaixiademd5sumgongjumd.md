---
layout: post
title: "Windows 平台下的 md5sum 工具"
date:   2020-03-23
tags: [md5sum,Windows,校验,文件,工具]
comments: true
author: admin
---
# Windows 平台下的 md5sum 工具

## 简介

本仓库提供了一个在 Windows 平台下使用的 `md5sum` 工具。该工具的功能与 Linux 系统中的 `md5sum` 完全一致，能够生成文件的 MD5 校验和，确保文件的完整性和一致性。

## 特点

- **兼容性**：与 Linux 下的 `md5sum` 工具生成的 MD5 校验和完全一致。
- **便捷性**：单文件工具，无需安装，直接在命令行中使用。
- **跨平台**：适用于 Windows 操作系统，方便用户在不同平台间进行文件校验。

## 使用方法

1. **下载**：从本仓库下载 `md5sum.exe` 文件。
2. **使用**：
   - 打开命令提示符（CMD）或 PowerShell。
   - 导航到 `md5sum.exe` 所在的目录。
   - 运行以下命令生成文件的 MD5 校验和：
     ```
     md5sum.exe 文件路径
     ```
   - 例如：
     ```
     md5sum.exe C:\path\to\your\file.txt
     ```

## 注意事项

- 确保文件路径正确，避免因路径错误导致无法生成校验和。
- 该工具仅适用于 Windows 平台，不支持其他操作系统。

## 贡献

欢迎提交问题和建议，帮助改进此工具。

## 许可证

本工具遵循开源许可证，具体信息请查看仓库中的 LICENSE 文件。

## 下载链接

[Windows平台下的md5sum工具](https://pan.quark.cn/s/be6c9f42a759)