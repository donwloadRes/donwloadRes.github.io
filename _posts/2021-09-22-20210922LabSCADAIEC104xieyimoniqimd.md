---
layout: post
title: "LabSCADA IEC 104 协议模拟器"
date:   2024-07-20
tags: [Linux,守护,IEC,104,Windows]
comments: true
author: admin
---
# Lab-SCADA IEC 104 协议模拟器

## 简介
Lab-SCADA IEC 104 主从模拟器是一个开源项目，旨在实现 IEC 60870-5-104 通信协议的主（控制）站和从（受控）站角色。该模拟器支持 Linux 和 Windows 操作系统，并提供了丰富的功能来模拟和测试 IEC 104 协议的通信过程。

## 功能特点
### IEC 104 主站模拟器
- **iec104msd**: Linux 操作系统的服务器守护程序，实现 IEC 60870-5-104 主站协议的核心通信服务。
- **iec104m_ui**: Linux 操作系统的命令行 UI 前端，用于与 `iec104msd` Linux 守护进程进行交互。
- **ls104msgui.exe**: 用于与 `iec104msd` Linux 守护进程通信的 Windows GUI 控制应用程序。

### IEC 104 从站模拟器
- **iec104sld**: Linux 操作系统的服务器守护程序应用程序，实现 IEC 60870-5-104 从站协议的核心通信服务。
- **iec104s**: Linux 操作系统的命令行 UI 前端，用于与 `iec104sld` Linux 守护进程进行通信。
- **ls104slgui.exe**: 用于与 `iec104sld` Linux 守护进程通信的 Windows GUI 控制应用程序。

## 使用说明
### 安装与配置
1. **Linux 环境**:
   - 下载并解压项目文件。
   - 进入项目目录，运行 `make` 命令编译项目。
   - 启动 `iec104msd` 或 `iec104sld` 守护程序。
   - 使用 `iec104m_ui` 或 `iec104s` 命令行工具与守护程序进行交互。

2. **Windows 环境**:
   - 下载并解压项目文件。
   - 运行 `ls104msgui.exe` 或 `ls104slgui.exe` 启动 Windows GUI 控制应用程序。
   - 配置应用程序以连接到 Linux 上的 `iec104msd` 或 `iec104sld` 守护程序。

### 运行与测试
- 启动主站模拟器和从站模拟器。
- 使用命令行工具或 Windows GUI 应用程序进行通信测试。
- 观察和分析通信过程中的数据包和状态信息。

## 贡献
欢迎开发者贡献代码、报告问题或提出改进建议。请通过 GitHub 提交 Pull Request 或 Issue。

## 许可证
本项目采用开源许可证，具体信息请参阅项目根目录下的 `LICENSE` 文件。

## 联系我们
如有任何问题或建议，请通过 GitHub 项目页面联系我们。

## 下载链接

[Lab-SCADAIEC104协议模拟器](https://pan.quark.cn/s/dc4037d6097f)