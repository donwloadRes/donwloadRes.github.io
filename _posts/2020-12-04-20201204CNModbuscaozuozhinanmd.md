---
layout: post
title: "C# NModbus 操作指南"
date:   2023-11-23
tags: [Modbus,NModbus,C#,TCP,读取]
comments: true
author: admin
---
# C# NModbus 操作指南

---

## 欢迎使用C# NModbus库

### **项目概述**

本开源仓库致力于提供一个简洁、高效的C#实现的NModbus库，用于轻松集成Modbus协议到您的C#应用程序中。Modbus是一种广泛应用于工业自动化领域的通讯协议，支持多种通信模式，包括但不限于RS-485上的Modbus RTU、ASCII以及以太网上的Modbus TCP。利用此库，开发者可以迅速实现对远程I/O设备的控制与数据采集，简化工业自动化系统的开发流程。

### **Modbus协议简介**

Modbus协议涵盖多个变体，支持从串行通信（重点是RS-485）到以太网的不同版本，其中最知名的有Modbus RTU、ASCII和TCP格式。工业场景普遍采用Modbus RTU，它强调效率和简单性。相比之下，Modbus TCP通过添加MBAP报文头，适应网络通信环境，省去了CRC校验，因TCP本身提供了可靠性保障。简而言之，Modbus TCP可视作是在特定结构前缀基础上简化了RTU版本的协议，无需额外CRC。

#### 功能码概览：

- **0x01** - 读取线圈状态
- **0x02** - 读取离散输入状态
- **0x03** - 读取保持寄存器
- **0x04** - 读取输入寄存器

### **如何使用**

1. **引入库**: 将NModbus库添加到您的C#项目中。
2. **初始化**: 创建一个`SerialPortSettings`或`TcpClientSettings`实例，根据您是使用串口还是TCP连接。
3. **建立连接**: 使用所选的设置初始化相应的Modbus Slave/Master对象。
4. **发送命令**: 根据需求构建请求报文，调用相应的方法进行读/写操作。
5. **处理响应**: 解析从设备返回的数据。

### **示例代码片段**

```csharp
using NModbus;
using NModbus.Serial;

// 初始化串口设置
 SerialPortSettings settings = new SerialPortSettings(9600, Parity.None, 8, StopBits.One);
 
 // 实例化Modbus Serial Master
 using (ITransport serialTransport = new SerialPortTransport(settings, "COM1"))
 {
     using (ModbusSerialMaster master = new ModbusSerialMaster(serialTransport))
     {
         master.Transport.Open();
         
         // 发送读取保持寄存器命令
         uint slaveId = 1; // 设备地址
         ushort startAddress = 0; // 寄存器起始地址
        ushort numberOfRegisters = 10; // 要读取的寄存器数量
         ReadHoldingRegistersResponse response = (ReadHoldingRegistersResponse)master.ReadHoldingRegisters(slaveId, startAddress, numberOfRegisters);
         
         // 处理响应数据
         foreach (ushort registerValue in response.Registers)
         {
             Console.WriteLine($"Register Value: {registerValue}");
         }
         
         master.Transport.Close();
     }
 }
```

### **文档与支持**

- **文档**: 请参考仓库的Wiki页面或官方文档获取详细使用方法和配置指南。
- **贡献**: 欢迎提交问题、建议或者通过Pull Requests参与改进。
- **社区**: 加入我们的社区讨论，共同促进项目的成长。

开始您的Modbus之旅，利用C# NModbus库简化您的工业通讯应用开发吧！

---

这个README.md旨在快速引导用户了解并开始使用C# NModbus库，涵盖了基本概念、功能码解释和简单的使用示例。希望这能帮助您高效地整合Modbus协议到您的项目之中。

## 下载链接

[CNModbus操作指南](https://pan.quark.cn/s/c5164bc62fe1)