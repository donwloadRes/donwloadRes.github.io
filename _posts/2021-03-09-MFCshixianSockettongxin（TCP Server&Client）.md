---
layout: post
title: "MFC实现Socket通信（TCP Server&Client）"
date:   2023-08-10
tags: [MFC,Socket,通信,示例,TCP]
comments: true
author: admin
---
# MFC实现Socket通信（TCP Server&Client）

## 项目简介

本项目是一个基于MFC（Microsoft Foundation Classes）的Socket通信示例，实现了TCP协议下的服务器和客户端之间的通信。通过本项目，您可以学习如何在MFC框架下使用Socket进行网络编程，实现简单的TCP通信功能。

## 功能特点

- **支持TCP Server和Client模式**：项目中包含了一个工程，支持同时作为服务器和客户端使用，测试相互通信正常。
- **简单易用**：通过MFC提供的CAsyncSocket类，简化了Socket编程的复杂性，使得网络通信的实现更加直观和易于理解。
- **代码示例**：项目中提供了详细的代码示例，展示了如何创建Socket、绑定端口、监听连接、发送和接收数据等操作。

## 使用步骤

1. **新建工程**：
   - 新建一个基于对话框的简单工程，命名为`SocketNet`。

2. **添加类**：
   - 在类向导中添加一个基于`CAsyncSocket`的类，命名为`MSocket`。

3. **通信实现**：
   - 在`SocketNetDlg.h`和`SocketNetDlg.cpp`中实现服务器和客户端的通信逻辑。
   - 服务器端代码示例：
     ```cpp
     if (AfxSocketInit()) {
         MessageBox("WindowSocket init failed", "Receive", MB_ICONSTOP);
         return;
     }
     if (1 == m_nServer) {
         m_ListenSocket = new MSocket;
         m_ListenSocket->SetDlg(this);
         sIP = "127.0.0.1";
         sPort = 7600;
         m_ListenSocket->Create(sPort, 1, FD_ACCEPT, sIP); // 创建服务器监听Socket
         m_ListenSocket->Listen(20);
     } else {
         m_ClientSocket = new MSocket;
         m_ClientSocket->SetDlg(this);
         sIP = "127.0.0.1";
         sPort = 7600;
         m_ClientSocket->Create();
         m_ClientSocket->Connect(sIP, sPort);
     }
     ```
   - 客户端代码示例：
     ```cpp
     void CSocketNetDlg::OnConnect() {
         // 连接成功
         GetDlgItem(IDC_EDIT_RECV)->SetWindowText("连接服务器成功");
     }
     ```

## 注意事项

- 本项目使用MFC框架，建议在Visual Studio等支持MFC的开发环境中运行。
- 项目中使用了`CAsyncSocket`类，需要对MFC的Socket编程有一定的了解。
- 项目代码仅供参考，实际使用时请根据具体需求进行调整和优化。

## 参考资料

- [MFC实现Socket通信（TCP Server&Client）](https://blog.csdn.net/long00000kid/article/details/122067848)

## 联系作者

如有任何问题或建议，请联系作者：long00000kid。

---

希望本项目能够帮助您更好地理解MFC下的Socket通信实现，祝您学习愉快！

## 下载链接

[MFC实现Socket通信TCPServerClient](https://pan.quark.cn/s/2139d2a2e225)