---
layout: post
title: "UE4 TCP通信指南"
date:   2023-08-09
tags: [socket,服务端,TCP,客户端,UE4]
comments: true
author: admin
---
# UE4 TCP通信指南

本资源文件提供了一个详细的指南，帮助开发者实现UE4客户端与网络调试助手服务端以及Python服务端的TCP通信。通过本指南，您将学习如何在UE4中建立TCP客户端，并实现与不同服务端的通信。

## 目录

1. **使用UE4建立TCP客户端**
2. **使用网络调试助手建立服务端**
3. **基于网络调试助手的服务端与UE客户端通信**
4. **基于Python的TCP服务端与UE客户端通信**

## 1. 使用UE4建立TCP客户端

### 步骤

1. 在虚幻商城中搜索并下载TCP Socket Plugin插件。
2. 安装插件到引擎，支持的版本包括4.22-4.27和5.0。
3. 打开工程，找到编辑->插件。
4. 启用插件并重启虚幻编辑器。
5. 新建蓝图，选择继承自TCPSocketConnection类。
6. 在事件图表中建立节点，设置服务端IP和端口。
7. 添加自定义事件，分别命名为断开连接、建立连接和接收信息。
8. 建立连接时打印“建立连接”，断开连接时打印“断开连接”，接收到信息时将其转为string类型并打印。

## 2. 使用网络调试助手建立服务端

### 步骤

1. 下载并打开网络调试助手。
2. 协议类型选择TCP Server，IP使用本机地址，端口号与客户端一致。
3. 点击打开，启动服务端。

## 3. 基于网络调试助手的服务端与UE客户端通信

### 步骤

1. 首先运行服务端。
2. 将TCPTest_BP拖入视口中。
3. 播放游戏，可以看到右上角打印了建立连接，说明UE与网络调试助手建立了TCP通信。
4. 使用网络调试助手发送信息，可以看到UE4接收到了发送的信息。
5. 点击关闭，可以看到UE打印了断开连接。

## 4. 基于Python的TCP服务端与UE客户端通信

### 代码示例

```python
import socket

def main():
    # 创建套接字
    tcp_server_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    # 绑定端口和ip
    tcp_server_socket.bind(("", 6666))
    # 设置套接字为被动监听模式，128为允许接收的最大连接数
    tcp_server_socket.listen(128)
    # 接收客户端连接
    new_client_socket, client_ip_port = tcp_server_socket.accept()
    new_client_socket.send("test".encode())
    tcp_server_socket.close()

if __name__ == '__main__':
    main()
```

### 效果

可以看到当运行游戏后，接收到了服务端发送的信息。

通过本指南，您将能够成功实现UE4客户端与不同服务端的TCP通信，为您的游戏开发提供强大的网络功能支持。

## 下载链接

[UE4TCP通信指南分享](https://pan.quark.cn/s/07ce2496ac8b)