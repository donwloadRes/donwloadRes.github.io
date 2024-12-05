---
layout: post
title: "C 从内存加载动态链接库"
date:   2021-04-27
tags: [DLL,加载,加壳,Byte,内存]
comments: true
author: admin
---
# C# 从内存加载动态链接库

## 描述

本资源文件提供了一个纯C#实现的从内存加载动态链接库的解决方案。该方案支持加壳的DLL，使用方便，适合在需要动态加载DLL的场景中使用。

## 功能特点

- **纯C#实现**：无需依赖外部库或工具，完全使用C#语言实现。
- **支持加壳DLL**：能够加载经过加壳处理的DLL文件，适用于需要保护代码的场景。
- **使用简单**：通过简单的API调用即可完成DLL的加载和函数调用。

## 示例代码

以下是一个简单的示例代码，展示了如何使用该方案从内存中加载DLL并调用其中的函数：

```csharp
class Program
{
    public delegate Int32 CompressHandle(ref Byte dest, ref Int32 len, Byte[] source, Int32 sourcelen);

    static void Main(string[] args)
    {
        Byte[] source = new byte[10000];
        Byte[] dest = new byte[10000];
        Int32 len = source.Length;
        Byte[] dllBin = File.ReadAllBytes("zlib1.dll");

        using (var dll = new DllLoader())
        {
            if (dll.LoadLibrary(dllBin))
            {
                var Compress = dll.GetProcDelegate<CompressHandle>("compress");
                if (Compress != null)
                {
                    var result = Compress.Invoke(ref dest[0], ref len, source, len);
                    Console.WriteLine(result);
                }
            }
        }
    }
}
```

## 使用说明

1. **加载DLL**：通过`DllLoader`类的`LoadLibrary`方法加载DLL文件的二进制数据。
2. **获取函数委托**：使用`GetProcDelegate`方法获取DLL中的函数委托。
3. **调用函数**：通过委托调用DLL中的函数，并处理返回结果。

## 注意事项

- 确保DLL文件的二进制数据正确无误。
- 加载的DLL文件必须与当前应用程序的架构（32位或64位）匹配。
- 如果DLL文件经过加壳处理，确保加壳工具不会影响DLL的正常加载和使用。

## 适用场景

- 需要动态加载DLL的应用程序。
- 需要保护DLL代码的场景，如加壳处理。
- 需要在内存中直接加载DLL，避免文件系统操作的场景。

## 贡献

欢迎提交问题和改进建议，帮助我们完善这个项目。

## 下载链接

[C从内存加载动态链接库](https://pan.quark.cn/s/b152e831741c)