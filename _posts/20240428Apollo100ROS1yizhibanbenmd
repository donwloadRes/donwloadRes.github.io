---
layout: post
title: "Apollo 1.0.0 ROS1 移植版本"
date:   2022-06-01
tags: [Apollo,ROS,版本,移植,仿真]
comments: true
author: admin
---
# Apollo 1.0.0 ROS1 移植版本

## 项目描述

此工程为基于 Apollo 1.0.0 的 ROS1 移植版本。移植的主要目的如下：

- 学习 Apollo 框架设计
- 学习 Apollo 中的控制算法

目前移植版本与原有版本的主要改动点如下：

- 使用原生 ROS（基于 Noetic）替代 Apollo 中更改的 ROS
- 使用 ROS 包（ROS pkg）封装 Apollo 中的每个模块
- 使用 CMake 进行编译
- 将 Protobuf 版本提升到 3.6.0
- 使用 ROS 中的 `std_msgs/String` 替代 Apollo 的 `pd_msgs/xxx` 消息
- 增加 PNC 仿真工具 `apollo_simulator`

此移植版本能够很好地将自己的算法增加到框架中，应用于机器人或者无人驾驶中。同时，由于 Apollo 中的模块抽象，每个模块之间和中间件没有耦合，中间件能很容易从 ROS1 移植到 ROS2、LCM 等。具体开发可根据个人需求进行魔改。

## 使用说明

1. **环境准备**：
   - 确保已安装 ROS Noetic 环境。
   - 安装 Protobuf 3.6.0 版本。

2. **编译**：
   - 使用 CMake 进行编译，具体步骤请参考项目中的 `CMakeLists.txt` 文件。

3. **运行**：
   - 启动 ROS 节点管理器（roscore）。
   - 运行各个模块，具体启动命令请参考项目中的启动脚本。

4. **仿真**：
   - 使用 `apollo_simulator` 进行 PNC 仿真，具体使用方法请参考仿真工具的文档。

## 贡献

欢迎大家贡献代码，提出问题或建议。请通过 GitHub 的 Issues 或 Pull Requests 进行交流。

## 许可证

本项目采用 MIT 许可证，具体内容请参考 `LICENSE` 文件。

## 下载链接

[Apollo1.0.0ROS1移植版本](https://pan.quark.cn/s/6bf9b0076cf5)