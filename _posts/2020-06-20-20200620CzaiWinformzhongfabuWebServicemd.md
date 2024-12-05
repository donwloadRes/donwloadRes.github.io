---
layout: post
title: "C# 在Winform中发布WebService"
date:   2021-11-13
tags: [double,Winform,WebService,服务,示例]
comments: true
author: admin
---
# C# 在Winform中发布WebService

本仓库提供了一套完整的示例，演示如何在Windows窗体（Winform）应用中发布和调用WebService，特别适用于使用Visual Studio 2015在Windows 7环境下开发的项目。此资源包含从创建服务端代码至客户端调用的全过程指导。

## 一、说明

### 创建与实现步骤

1. **创建Winfrom应用程序** 或选择控制台项目作为起点。
2. **添加WCF服务**：
   - 定义服务接口，如`ICalculator`，使用`[ServiceContract]`和`[OperationContract]`属性标记。
   - 实现该服务接口，例如创建`CalculatorService`类。
3. **配置服务**：修改应用程序配置文件中的服务端点，确保指定正确的绑定(`basicHttpBinding`)和服务地址。

### 关键代码示例

#### 定义服务接口
```csharp
[ServiceContract(Namespace = "http://Microsoft.ServiceModel.Samples")]
public interface ICalculator
{
    [OperationContract]
    double Add(double n1, double n2);
}
```

#### 实现服务
```csharp
public class CalculatorService : ICalculator
{
    public double Add(double n1, double n2)
    {
        return n1 + n2;
    }
}
```

#### 配置及启动服务
- 更新配置文件以指定服务地址和接口。
- 在Winform的加载事件中启动`ServiceHost`以监听服务请求。
```csharp
private void frmMain_Load(object sender, EventArgs e)
{
    try
    {
        ServiceHost serviceHost = new ServiceHost(typeof(CalculatorService));
        serviceHost.Open();
        label1.Text = "服务启动正常";
    }
    catch (Exception ex)
    {
        label1.Text = ex.Message;
    }
}
```

#### 客户端调用
利用服务地址进行远程调用，完成WebService的基本交互流程。

## 二、注意事项

- 确保在实际部署时调整服务地址(`http://xxx.xxx.xxx.xx:8733/test/Service1/`)以匹配您的网络环境。
- 本示例基于特定版本的VS和操作系统，但核心概念适用于其他版本的Visual Studio和.NET框架。
- 安全性和性能优化不在本次示例的讨论范围内，实际应用中需额外考虑。

通过遵循以上步骤，您可以轻松地在Winform应用中集成和发布WebService功能，便于本地或网络环境下的数据交换与处理。

## 下载链接

[C在Winform中发布WebService](https://pan.quark.cn/s/08238310d286)