---
layout: post
title: "C 必备技能篇 VS2019 使用 CC 生成 DLL 文件并用 CCC 调用 DLL"
date:   2020-10-05
tags: [DLL,C++,C#,调用,示例]
comments: true
author: admin
---
# C# 【必备技能篇】 VS2019 使用 C/C++ 生成 DLL 文件，并用 C/C++、C# 调用 DLL

在C#应用程序开发中，集成由C或C++编写的底层库是非常常见的需求，这通常通过调用DLL（动态链接库）来实现。本资源旨在指导开发者如何使用Visual Studio 2019（VS2019）环境，详细步骤演示如何创建和生成DLL文件，以及如何在C/C++和C#项目中正确引用并调用这些DLL中的函数。此教程适合希望增强跨语言编程能力的开发者。

**目录**

- **环境配置**
- **C/C++ DLL 创建**
    - 步骤一：新建DLL项目
    - 步骤二：编写导出函数
    - 步骤三：生成DLL
- **C/C++ 中调用 DLL**
    - 实例解析
- **C# 中调用 DLL**
    - 添加引用
    - 调用DLL函数
- **示例代码片段**
    - C/C++ DLL 导出函数示例
    - C# 中调用DLL的示例
- **常见问题与解决方法**

**环境配置**

确保您已安装Visual Studio 2019，并且包含了C++和C#开发的相关工作负载。

**C/C++ DLL 创建**

1. **新建DLL项目**：在VS2019中选择“新建” -> “项目” -> 找到“DLL”模板，为其指定合适的名称和位置。
2. **编写导出函数**：使用`__declspec(dllexport)`关键字标记你要从DLL导出的函数。
3. **生成DLL**：构建解决方案后，会在项目的输出目录找到生成的DLL文件。

**C/C++ 和 C# 中调用 DLL**

- 对于C/C++，直接#include对应的头文件，并链接到生成的DLL即可调用函数。
- 在C#中，则需使用`DllImport`属性来导入DLL，并定义对应的函数签名以调用。

**示例代码片段**

**C/C++ DLL 导出函数示例:**

```cpp
extern "C" __declspec(dllexport) void HelloWorld() {
    std::cout << "Hello from DLL!" << std::endl;
}
```

**C# 中调用DLL的示例:**

```csharp
using System.Runtime.InteropServices;

public class Program {
    [DllImport("YourDLLName.dll")]
    public static extern void HelloWorld();

    static void Main(string[] args) {
        HelloWorld();
    }
}
```

请替换`YourDLLName.dll`为实际生成的DLL文件名。

**学习与实践**

跟随上述步骤，您可以有效掌握在不同场景下如何利用VS2019高效地创建和调用DLL，加强您的跨语言开发能力。实践中可能会遇到路径问题、命名约定差异等挑战，细致阅读错误信息并参考官方文档将有助于快速解决问题。祝您学习顺利，编程愉快！

## 下载链接

[C必备技能篇VS2019使用CC生成DLL文件并用CCC调用DLL](https://pan.quark.cn/s/b536f20c0986)