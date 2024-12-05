---
layout: post
title: "基于GD32F130的IAP程序"
date:   2024-09-28
tags: [BootLoader,APP,Flash,GD32F130,固件]
comments: true
author: admin
---
# 基于GD32F130的IAP程序

## 简介

本仓库提供了一个基于GD32F130微控制器的IAP（In-Application Programming）程序，包括BootLoader、APP以及内部Flash的读写操作。通过本程序，用户可以实现固件的在线升级和内部Flash的读写管理。

## 功能特点

- **BootLoader**：负责启动应用程序，并提供固件升级的功能。
- **APP**：用户应用程序，可以进行各种操作和功能实现。
- **内部Flash读写操作**：提供了对GD32F130内部Flash的读写接口，方便用户进行数据存储和固件升级。

## 使用说明

1. **克隆仓库**：
   ```bash
   git clone https://github.com/your-repo-url.git
   ```

2. **编译BootLoader**：
   - 进入BootLoader目录
   - 使用Keil或其他编译工具进行编译

3. **编译APP**：
   - 进入APP目录
   - 使用Keil或其他编译工具进行编译

4. **烧录程序**：
   - 使用ST-Link或其他烧录工具将BootLoader和APP分别烧录到GD32F130的Flash中

5. **固件升级**：
   - 通过BootLoader提供的升级接口，将新的APP固件写入到内部Flash中

## 目录结构

```
├── BootLoader
│   ├── src
│   ├── inc
│   └── Makefile
├── APP
│   ├── src
│   ├── inc
│   └── Makefile
├── Docs
│   └── 使用说明.md
└── README.md
```

## 贡献

欢迎大家贡献代码和提出问题。如果您有任何建议或发现了bug，请在Issues中提出。

## 许可证

本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

---

希望本项目能对您有所帮助，祝您使用愉快！

## 下载链接

[基于GD32F130的IAP程序](https://pan.quark.cn/s/358f0653e997)