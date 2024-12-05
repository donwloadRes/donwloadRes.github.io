---
layout: post
title: "Qt编写网络调试助手TCP客户端TCP服务端UDP服务端终极版"
date:   2023-09-11
tags: [TCP,客户端,服务端,UDP,http]
comments: true
author: admin
---
# Qt编写网络调试助手（TCP客户端+TCP服务端+UDP服务端）终极版

## 项目介绍

时隔半年，对网络调试助手工具进行了彻底的代码重写。新版本不仅目录结构整齐，代码也更加规范和完善。我保证，这次真的是终极版，打死也不再改版了。以下是旧版本的链接：
- 旧版本1：[http://www.qtcn.org/bbs/read-htm-tid-55540.html](http://www.qtcn.org/bbs/read-htm-tid-55540.html)
- 旧版本2：[http://www.qtcn.org/bbs/read-htm-tid-62636.html](http://www.qtcn.org/bbs/read-htm-tid-62636.html)

## 基本功能

1. **16进制数据和ASCII数据收发**：支持16进制和ASCII两种数据格式的收发。
2. **定时器自动发送**：可以设置定时器，实现数据的自动发送。
3. **自动从配置文件加载最后一次的界面设置**：程序启动时自动加载上一次的界面设置。
4. **自动从配置文件加载数据发送下拉框的数据**：可以将经常使用的数据填写在`send.txt`中，程序会自动加载。
5. **可启用设备模拟回复**：当收到某个数据时，模拟设备自动回复数据。对应数据格式填写在`device.txt`中。
6. **可对单个在线连接发送数据，也可勾选全部进行发送**：支持对单个连接或所有连接发送数据。
7. **支持多个客户端连接并发**：可以同时处理多个客户端的连接。
8. **采用单线程**：所有操作都在单线程中完成，确保程序的简洁和高效。
9. **四种模式**：支持TCP服务器、TCP客户端、UDP服务器、UDP客户端四种模式。

## 使用说明

1. **克隆仓库**：
   ```bash
   git clone https://github.com/your-repo/QtNetworkDebugAssistant.git
   ```

2. **编译和运行**：
   - 确保你已经安装了Qt开发环境。
   - 打开项目文件，进行编译和运行。

3. **配置文件**：
   - `send.txt`：用于存储经常使用的数据。
   - `device.txt`：用于存储设备模拟回复的数据格式。

## 贡献

欢迎大家提出问题和建议，或者直接提交Pull Request。让我们一起完善这个工具！

## 许可证

本项目采用[MIT许可证](LICENSE)，欢迎自由使用和修改。

## 下载链接

[Qt编写网络调试助手TCP客户端TCP服务端UDP服务端终极版](https://pan.quark.cn/s/6599694719f4)