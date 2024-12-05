---
layout: post
title: "PyScada基于Django的开源SCADA系统"
date:   2021-08-15
tags: [PyScada,Django,SCADA,Modbus,系统]
comments: true
author: admin
---
# PyScada：基于Django的开源SCADA系统

## 简介
PyScada是一个使用Django框架构建的开源SCADA系统，具备HTML5 HMI（人机界面）功能。如果您想搭建自己的SCADA系统，PyScada是一个理想的选择。

## 主要特点
- **基于HTML5的HMI**：提供现代化的用户界面，支持多种设备和浏览器。
- **支持多种工业协议**：
  - Modbus TCP/IP
  - Modbus RTU
  - Modbus ASCII
  - Modbus二进制
  - Phant
  - 签证
  - 1线
  - BACNet/IP（正在开发中）
  - 米总线，MBus（正在开发中）
- **低硬件要求**：服务器的硬件要求非常低，适合在资源有限的环境中运行。
- **结构依赖**：
  - 核心/人机界面：
    - Python 2.7
    - Django == 1.11
    - NumPy >= 1.6.0
    - 枕头
  - Python守护进程：
    - ModbusMaster
    - pymodbus >= 1.2
  - HDF5导出：
    - h5py >= 2.1.1
  - 系统统计：
    - psutil
  - 签证：
    - PyVisa >= 1.8
  - BACNet/IP：
    - 杆菌属1线O

## 使用说明
1. **安装依赖**：根据上述结构依赖，安装所需的Python库和Django框架。
2. **配置系统**：根据您的需求配置PyScada系统，包括选择支持的工业协议和设置HMI界面。
3. **运行系统**：启动PyScada服务器，开始监控和管理您的工业设备。

## 贡献
欢迎开发者贡献代码和提出改进建议。请通过GitHub提交您的Pull Request或Issue。

## 许可证
PyScada采用开源许可证，具体许可证信息请参考项目根目录下的LICENSE文件。

---

通过PyScada，您可以轻松搭建一个功能强大且易于扩展的SCADA系统，满足各种工业自动化需求。

## 下载链接

[PyScada基于Django的开源SCADA系统](https://pan.quark.cn/s/e94534e32eb4)