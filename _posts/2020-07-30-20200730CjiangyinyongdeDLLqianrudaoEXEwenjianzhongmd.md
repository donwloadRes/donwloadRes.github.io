---
layout: post
title: "C 将引用的DLL嵌入到EXE文件中
date   20211108
tags DLLEXE资源文件Assembly
comments true
author admin

 C 将引用的DLL嵌入到EXE文件中

 应用场景
在开发C应用程序时为了简化分发过程你可能需要将程序依赖的DLL文件直接集成到最终的可执行文件EXE中这样做的好处是用户只需要拷贝一个单独的EXE文件即可运行应用而不需要担心丢失或遗漏DLL文件

 实现步骤

 1 打开项目属性
 在Visual Studio中找到你的项目然后右键点击该项目在弹出菜单中选择属性

 2 添加资源文件
 转到项目属性设置页面中的资源标签页
 点击添加现有文件按钮浏览并选择你需要嵌入的DLL文件这将会将DLL作为资源添加到你的项目中
 添加后的DLL会自动放置在项目的Resources目录下如果项目中还未创建此目录则系统会自动创建

 3 设置DLL为资源
 一旦DLL被加入到资源中你无需手动进行额外操作来标记其为资源但重要的是理解这个步骤是通过上一步自动完成的

 4 设置DLL属性
 回到解决方案资源管理器找到原DLL引用不是资源里的右键点击属性确保复制到输出目录设置为不复制False这是为了避免编译时的冗余处理

 5 编写加载代码
 在程序的主入口点通常是Programcs中的Main方法你需要编写代码以在运行时动态地从EXE内部提取并加载DLL
    csharp
     引入必要的命名空间
    using SystemReflection
    
     主方法
    static void Mainstring args
    
         获取当前Assembly即exe文件
        Assembly executingAssembly  AssemblyGetExecutingAssembly
        
         定义DLL资源名通常格式为项目名资源名"
date:   2021-11-08
tags: [DLL,EXE,资源,文件,Assembly]
comments: true
author: admin
---
# C# 将引用的DLL嵌入到EXE文件中

## 应用场景
在开发C#应用程序时，为了简化分发过程，你可能需要将程序依赖的DLL文件直接集成到最终的可执行文件(EXE)中。这样做的好处是用户只需要拷贝一个单独的EXE文件即可运行应用，而不需要担心丢失或遗漏DLL文件。

## 实现步骤

### 1. 打开项目属性
- 在Visual Studio中，找到你的项目，然后右键点击该项目，在弹出菜单中选择“属性”。

### 2. 添加资源文件
- 转到项目属性设置页面中的“资源”标签页。
- 点击“添加现有文件”按钮，浏览并选择你需要嵌入的DLL文件。这将会将DLL作为资源添加到你的项目中。
- 添加后的DLL会自动放置在项目的“Resources”目录下（如果项目中还未创建此目录，则系统会自动创建）。

### 3. 设置DLL为资源
- 一旦DLL被加入到资源中，你无需手动进行额外操作来标记其为资源，但重要的是理解这个步骤是通过上一步自动完成的。

### 4. 设置DLL属性
- 回到解决方案资源管理器，找到原DLL引用（不是资源里的），右键点击属性，确保“复制到输出目录”设置为“不复制”（False）。这是为了避免编译时的冗余处理。

### 5. 编写加载代码
- 在程序的主入口点（通常是`Program.cs`中的`Main`方法），你需要编写代码以在运行时动态地从EXE内部提取并加载DLL。
    ```csharp
    // 引入必要的命名空间
    using System.Reflection;
    
    // 主方法
    static void Main(string[] args)
    {
        // 获取当前Assembly（即.exe文件）
        Assembly executingAssembly = Assembly.GetExecutingAssembly();
        
        // 定义DLL资源名，通常格式为"项目名;资源名"
        string resource_name = "YourProjectName.DLLResourceName"; // 替换为实际资源名称
        
        // 从资源中读取字节流
        byte[] assemblyBytes = GetEmbeddedAssembly(executingAssembly, resource_name);
        
        if (assemblyBytes != null)
        {
            // 使用反射加载DLL
            Assembly.Load(assemblyBytes);
            
            // 此后可以正常使用该DLL中的类型和方法
        }
        else
        {
            Console.WriteLine("未能加载嵌入的DLL资源。");
        }
    }
    
    // 辅助方法：从嵌入的资源中获取字节数组
    private static byte[] GetEmbeddedAssembly(Assembly assembly, string resourceName)
    {
        using (Stream stream = assembly.GetManifestResourceStream(resourceName))
        {
            if (stream == null)
                return null;
            
            return ReadFully(stream);
        }
    }
    
    // 辅助方法：读取完整流数据为字节数组
    private static byte[] ReadFully(Stream input)
    {
        using (MemoryStream ms = new MemoryStream())
        {
            input.CopyTo(ms);
            return ms.ToArray();
        }
    }
    ```
    注意替换`YourProjectName.DLLResourceName`为你实际的DLL资源名称。

以上步骤完成后，重新编译你的项目，生成的EXE文件就包含了所需的DLL，使得程序可以在没有额外DLL文件的情况下运行。这种方法特别适用于轻量级部署或者需要简化安装流程的应用场景。

## 下载链接

[C将引用的DLL嵌入到EXE文件中分享](https://pan.quark.cn/s/05ea824671c4)