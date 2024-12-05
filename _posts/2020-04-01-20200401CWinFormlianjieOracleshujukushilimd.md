---
layout: post
title: "C WinForm 连接 Oracle 数据库示例"
date:   2020-03-17
tags: [Oracle,连接,数据库,示例,C#]
comments: true
author: admin
---
# C# WinForm 连接 Oracle 数据库示例

## 项目描述

本资源文件提供了一个使用 C# WinForm 连接 Oracle 数据库的示例代码。项目中有一个功能需要从 Oracle 数据库获取数据，原本以为只需将原来的 `SqlClient` 换成 `OracleClient` 即可，但实际上远比想象的复杂。需要安装 Oracle 客户端，并且网上相关文章繁多，测试和选择过程非常繁琐。

最终，通过朋友的帮助，他为我编写了一个简单的 Demo，我只需修改连接字符串即可成功连接 Oracle 数据库。这个 DLL 是 Oracle 为 C# 专门提供的，可以在其官方网站下载（虽然查找起来比较麻烦）。

## 代码示例

以下是连接 Oracle 数据库的示例代码：

```csharp
using Oracle.ManagedDataAccess.Client;

public static string ConnectOracle()
{
    try
    {
        string connString = "Data Source=(DESCRIPTION=(ADDRESS=(PROTOCOL=TCP)(HOST=130.147.246.144)(PORT=1521))(CONNECT_DATA=(SERVICE_NAME=ECMS)));Persist Security Info=True;User ID=system;Password=Service01;";
        OracleConnection con = new OracleConnection(connString);
        con.Open();
        return string.Empty;
    }
    catch (Exception ex)
    {
        return ex.ToString();
    }
}
```

## 注意事项

1. **Oracle.ManagedDataAccess.dll**：这是 Oracle 为 C# 提供的 DLL，用于连接 Oracle 数据库。请确保在项目中引用该 DLL。
2. **连接字符串**：请根据实际情况修改连接字符串中的 `HOST`、`PORT`、`SERVICE_NAME`、`User ID` 和 `Password`。
3. **异常处理**：代码中包含了异常处理，以便在连接失败时返回错误信息。

## 使用方法

1. 下载并引用 `Oracle.ManagedDataAccess.dll`。
2. 将上述代码复制到你的项目中。
3. 根据实际的 Oracle 数据库配置修改连接字符串。
4. 运行项目，测试连接是否成功。

## 致谢

特别感谢我的朋友，他为我编写了这段代码，帮助我解决了连接 Oracle 数据库的问题。

## 下载链接

[CWinForm连接Oracle数据库示例](https://pan.quark.cn/s/7f64908c86c3)