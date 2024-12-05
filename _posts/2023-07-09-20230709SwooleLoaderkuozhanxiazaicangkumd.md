---
layout: post
title: "Swoole Loader 扩展下载仓库"
date:   2020-10-25
tags: [swoole,so,php,zts,loader]
comments: true
author: admin
---
# Swoole Loader 扩展下载仓库

本仓库提供了一系列 Swoole Loader 扩展文件的下载，适用于 Linux 和 Windows 平台的 64 位系统，包括非线程安全和线程安全版本。这些扩展文件主要用于支持不同版本的 PHP 运行环境。

## 资源文件列表

### Linux 64位 (非线程安全)
- `swoole_loader56.so`
- `swoole_loader70.so`
- `swoole_loader71.so`
- `swoole_loader72.so`
- `swoole_loader73.so`
- `swoole_loader74.so`

### Linux 64位 (线程安全)
- `swoole_loader56_zts.so`
- `swoole_loader70_zts.so`
- `swoole_loader71_zts.so`
- `swoole_loader72_zts.so`
- `swoole_loader73_zts.so`

### Windows 64位 (非线程安全)
- `php_swoole_loader_php56_nzts_x64.dll`
- `php_swoole_loader_php70_nzts_x64.dll`
- `php_swoole_loader_php71_nzts_x64.dll`
- `php_swoole_loader_php72_nzts_x64.dll`
- `php_swoole_loader_php73_nzts_x64.dll`

### Windows 64位 (线程安全)
- `php_swoole_loader_php56_zts_x64.dll`
- `php_swoole_loader_php70_zts_x64.dll`
- `php_swoole_loader_php71_zts_x64.dll`
- `php_swoole_loader_php72_zts_x64.dll`
- `php_swoole_loader_php73_zts_x64.dll`

## 使用说明

1. **选择合适的扩展文件**：根据你的 PHP 版本和系统环境（Linux 或 Windows）选择对应的扩展文件。
2. **下载扩展文件**：从本仓库中下载所需的扩展文件。
3. **安装扩展**：将下载的扩展文件放置到 PHP 的扩展目录中，并在 `php.ini` 文件中添加相应的扩展配置。

## 注意事项

- 请确保下载的扩展文件与你的 PHP 版本和系统环境完全匹配，否则可能会导致 PHP 无法正常运行。
- 如果你不确定应该选择哪个版本的扩展文件，请参考 PHP 官方文档或咨询相关技术人员。

## 贡献

如果你有新的扩展文件或发现任何问题，欢迎提交 Issue 或 Pull Request。

## 许可证

本仓库中的所有资源文件遵循相应的开源许可证，具体请参考每个文件的许可证声明。

## 下载链接

[SwooleLoader扩展下载仓库](https://pan.quark.cn/s/22d8b6691b56)