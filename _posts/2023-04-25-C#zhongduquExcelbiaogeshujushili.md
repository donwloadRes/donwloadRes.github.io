---
layout: post
title: "C#中读取Excel表格数据实例"
date:   2020-10-27
tags: [Excel,C#,Office,读取,示例]
comments: true
author: admin
---
# C#中读取Excel表格数据实例

在这个资源中，我们提供了一个简洁的C#示例程序，演示如何在不依赖Microsoft Office环境的情况下读取Excel表格数据。这对于那些需要处理Excel数据但不想在目标系统上安装Office套件的开发者来说，是一个非常实用的解决方案。本示例适用于.NET框架或.NET Core环境，采用开源库如EPPlus或NPOI来实现Excel文件的读取，确保了广泛的应用场景和便捷性。

## 示例特点

- **无Office依赖**：代码设计不需要用户安装Office即可运行。
- **易用性**：通过简单的步骤展示如何打开Excel文件并读取数据。
- **兼容性**：支持多种Excel文件格式（如`.xlsx`、`.xls`）。
- **教育性**：适合C#初学者和需要快速集成Excel数据读取功能的开发者。

## 使用技术

- **EPPlus/NPOI**：这两个是常用的.NET库，选择其一用于操作Excel文件，它们都提供了丰富的API接口，且不需Office环境。
- **C#编程语言**：基于现代C#语法，编写清晰、高效的代码。

## 快速入门

1. **添加依赖**：首先，你需要在你的项目中添加EPPlus或NPOI的NuGet包引用。
   
2. **示例代码**：以下是一个基本的使用EPPlus读取Excel数据的例子：

   ```csharp
   using OfficeOpenXml; // 确保已安装EPPlus库

   class Program
   {
       static void Main(string[] args)
       {
           string filePath = @"C:\路径\到\你的\ExcelFile.xlsx"; // Excel文件路径
           using (var package = new ExcelPackage(new FileInfo(filePath)))
           {
               ExcelWorksheet worksheet = package.Workbook.Worksheets[0]; // 选取第一个工作表
               for (int row = 1; row <= worksheet.Dimension.End.Row; row++)
               {
                   for (int col = 1; col <= worksheet.Dimension.End.Column; col++)
                   {
                       Console.Write(worksheet.Cells[row, col].Value + "\t");
                   }
                   Console.WriteLine();
               }
           }
       }
   }
   ```

3. **注意事项**：请根据实际Excel文件的路径替换`filePath`变量的值，并确保文件可访问。

4. **运行程序**：编译并运行上述代码，你将能看到Excel中的数据被逐行打印在控制台。

## 结论

通过本示例，你可以快速学会如何利用C#在没有Office安装的环境中读取Excel数据，这对于自动化处理、数据导入等场景尤其有用。掌握这一技能，将极大提升你在数据处理任务上的灵活性和效率。

请注意，具体实现时可能需要根据实际情况调整代码，比如处理异常、优化性能等。希望这个示例能够为你提供有力的帮助！

## 下载链接

[C中读取Excel表格数据实例](https://pan.quark.cn/s/33e7b2bc5cd9)