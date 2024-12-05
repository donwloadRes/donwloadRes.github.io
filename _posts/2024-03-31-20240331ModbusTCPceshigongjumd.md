---
layout: post
title: "Modbus TCP 测试工具"
date:   2023-02-23
tags: [Modbus,TCP,bash,com,your]
comments: true
author: admin
---
# Modbus TCP 测试工具

## 简介

本仓库提供了一个用于测试 Modbus TCP 协议的工具集，包含服务器模拟器（Server Sim）和客户端扫描器（Client Scan）。这些工具旨在帮助开发者和测试人员快速验证和调试基于 Modbus TCP 协议的设备和系统。

## 功能特点

- **服务器模拟器（Server Sim）**：
  - 模拟 Modbus TCP 服务器，支持多种寄存器操作。
  - 提供简单的配置界面，便于设置模拟参数。
  - 支持日志记录，方便调试和问题排查。

- **客户端扫描器（Client Scan）**：
  - 实现 Modbus TCP 客户端功能，支持读取和写入操作。
  - 提供批量扫描功能，快速发现网络中的 Modbus TCP 设备。
  - 支持自定义扫描参数，适应不同测试需求。

## 使用方法

### 服务器模拟器（Server Sim）

1. 克隆本仓库到本地：
   ```bash
   git clone https://github.com/your-repo/modbustcp-test-tool.git
   ```
2. 进入服务器模拟器目录：
   ```bash
   cd modbustcp-test-tool/server-sim
   ```
3. 根据需要修改配置文件 `config.yaml`。
4. 启动服务器模拟器：
   ```bash
   ./server-sim
   ```

### 客户端扫描器（Client Scan）

1. 克隆本仓库到本地：
   ```bash
   git clone https://github.com/your-repo/modbustcp-test-tool.git
   ```
2. 进入客户端扫描器目录：
   ```bash
   cd modbustcp-test-tool/client-scan
   ```
3. 根据需要修改配置文件 `config.yaml`。
4. 启动客户端扫描器：
   ```bash
   ./client-scan
   ```

## 贡献

欢迎提交 Issue 和 Pull Request 来改进和扩展本工具集。请遵循以下准则：

- 确保代码风格一致。
- 提供详细的提交信息和文档更新。
- 测试新功能或修复确保其稳定性和兼容性。

## 许可证

本项目采用 [MIT 许可证](LICENSE)。您可以自由使用、修改和分发本项目，但请保留原始许可证声明。

## 联系我们

如有任何问题或建议，请通过以下方式联系我们：

- 邮箱：[your-email@example.com](mailto:your-email@example.com)
- 项目主页：[https://github.com/your-repo/modbustcp-test-tool](https://github.com/your-repo/modbustcp-test-tool)

感谢您的支持和贡献！

## 下载链接

[ModbusTCP测试工具](https://pan.quark.cn/s/69723ea26793)