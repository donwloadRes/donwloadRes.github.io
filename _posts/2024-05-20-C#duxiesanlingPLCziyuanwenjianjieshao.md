---
layout: post
title: "C#读写三菱PLC资源文件介绍"
date:   2023-08-04
tags: [PLC,Melsu,Net,写入,读取]
comments: true
author: admin
---
# C#读写三菱PLC资源文件介绍

本资源文件提供了一个使用C#语言读写三菱PLC的示例程序。通过该程序，用户可以学习如何使用HslCommunication.dll库连接到三菱PLC设备，并实现数据的读取和写入操作。

## 主要功能

1. **连接PLC**：通过指定IP地址和端口号，程序可以与三菱PLC建立连接。
2. **读取数据**：程序支持从PLC中读取浮点数数据，并返回读取结果。
3. **写入数据**：用户可以将指定的浮点数数据写入PLC的指定地址。

## 使用方法

1. **添加引用**：首先需要添加HslCommunication.dll库的引用。
2. **配置连接**：在代码中配置PLC的IP地址和端口号，并调用连接方法。
3. **读写操作**：通过调用读取和写入方法，实现对PLC数据的读写操作。

## 示例代码

以下是一个简单的示例代码，展示了如何连接PLC并进行读写操作：

```csharp
using HslCommunication;
using HslCommunication.Profinet.Melsec;

public static class Mitsubishi
{
    public static MelsecMcNet Melsu_Net;

    // 创建连接
    public static bool Mitsu(string ipAddress, int port)
    {
        Melsu_Net = new MelsecMcNet(ipAddress, port);
        Melsu_Net.ConnectTimeOut = 2000; // 网络连接的超时时间
        Melsu_Net.NetworkNumber = 0x00; // 网络号
        Melsu_Net.NetworkStationNumber = 0x00; // 网络站号
        OperateResult connect = Melsu_Net.ConnectServer();
        return connect.IsSuccess;
    }

    // 读取数据
    public static bool Read(ref float flo, string address)
    {
        OperateResult<float> tt = Mitsubishi.Melsu_Net.ReadFloat(address);
        if (tt.IsSuccess)
        {
            flo = tt.Content;
            return true;
        }
        else
        {
            return false;
        }
    }

    // 写入数据
    public static bool Write(string address, float Value)
    {
        OperateResult write = Mitsubishi.Melsu_Net.Write(address, Value);
        if (write.IsSuccess)
        {
            return true;
        }
        else
        {
            return false;
        }
    }
}

// 调用连接方法
bool t = Mitsubishi.Mitsu("192.168.27.237", 8005);
if (t)
{
    MessageBox.Show("连接成功");
}
else
{
    MessageBox.Show("连接失败");
}

// 调用读取方法
float flo = 0;
bool Re = Mitsubishi.Read(ref flo, "D100");
if (Re)
{
    MessageBox.Show("读取成功" + flo);
}
else
{
    MessageBox.Show("读取失败");
}

// 调用写入方法
bool Wr = Mitsubishi.Write("M100", 52);
if (Wr)
{
    MessageBox.Show("写入成功");
}
else
{
    MessageBox.Show("写入失败");
}
```

## 注意事项

- 确保PLC设备与计算机在同一网络中，并且IP地址和端口号配置正确。
- 在进行读写操作时，确保PLC的地址和数据类型与程序中的配置一致。

通过本资源文件，用户可以快速上手使用C#与三菱PLC进行通信，实现数据的读取和写入操作。

## 下载链接

[C读写三菱PLC资源文件介绍](https://pan.quark.cn/s/c10d68893095)