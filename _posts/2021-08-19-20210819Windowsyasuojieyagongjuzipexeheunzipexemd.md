---
layout: post
title: "Windows 压缩解压工具zipexe 和 unzipexe"
date:   2021-09-18
tags: [zip,exe,解压,unzip,压缩]
comments: true
author: admin
---
# Windows 压缩解压工具：zip.exe 和 unzip.exe

## 简介

本仓库提供了一个在 Windows 环境下使用的压缩解压工具：`zip.exe` 和 `unzip.exe`。这两个工具可以帮助你在 Windows 系统中执行压缩和解压操作，支持通过脚本或命令行直接调用。

## 功能特点

- **压缩功能**：使用 `zip.exe` 可以将文件或文件夹压缩为 `.zip` 格式的压缩包。
- **解压功能**：使用 `unzip.exe` 可以将 `.zip` 格式的压缩包解压到指定目录。
- **命令行支持**：支持在 Windows 命令提示符（cmd）或 PowerShell 中直接调用，方便集成到脚本中进行自动化操作。

## 使用方法

### 压缩文件或文件夹

```bash
zip.exe -r output.zip input_folder
```

- `-r`：递归压缩文件夹及其子文件夹。
- `output.zip`：生成的压缩包文件名。
- `input_folder`：需要压缩的文件夹路径。

### 解压文件

```bash
unzip.exe input.zip -d output_folder
```

- `input.zip`：需要解压的压缩包文件名。
- `-d output_folder`：指定解压后的文件存放目录。

## 注意事项

- 请确保在执行命令时，当前目录或系统路径中包含 `zip.exe` 和 `unzip.exe`，否则命令可能无法识别。
- 建议在使用前备份重要数据，以防操作失误导致数据丢失。

## 贡献

如果你在使用过程中遇到问题或有改进建议，欢迎提交 Issue 或 Pull Request。

## 许可证

本仓库中的资源文件遵循相应的开源许可证，具体请参考文件中的许可证声明。

## 下载链接

[Windows压缩解压工具zip.exe和unzip.exe](https://pan.quark.cn/s/31083e2e97ed)