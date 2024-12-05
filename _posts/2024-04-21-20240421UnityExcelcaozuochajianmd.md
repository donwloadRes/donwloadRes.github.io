---
layout: post
title: "Unity Excel 操作插件"
date:   2021-11-13
tags: [Excel,插件,Unity,文件,worksheet]
comments: true
author: admin
---
# Unity Excel 操作插件

## 介绍

本仓库提供了一系列用于在Unity中操作Excel文件所需的DLL插件，包括EPPlus、Excel和ICSharpCode.SharpZipLib。这些插件可以帮助开发者轻松地在Unity项目中读取、写入和处理Excel文件。

## 包含的插件

- **EPPlus**: 一个强大的.NET库，用于处理Excel 2007+文件。
- **Excel**: 用于在Unity中操作Excel文件的插件。
- **ICSharpCode.SharpZipLib**: 一个用于压缩和解压缩文件的.NET库。

## 使用方法

1. **下载插件**: 从本仓库下载所需的DLL文件。
2. **导入Unity项目**: 将下载的DLL文件导入到你的Unity项目中。
3. **编写代码**: 使用这些插件编写代码来操作Excel文件。

## 示例代码

以下是一个简单的示例，展示如何在Unity中使用EPPlus读取Excel文件：

```csharp
using OfficeOpenXml;
using System.IO;

public class ExcelReader : MonoBehaviour
{
    void Start()
    {
        var file = new FileInfo("path_to_your_excel_file.xlsx");
        using (var package = new ExcelPackage(file))
        {
            var worksheet = package.Workbook.Worksheets[0];
            for (int row = 1; row <= worksheet.Dimension.Rows; row++)
            {
                for (int col = 1; col <= worksheet.Dimension.Columns; col++)
                {
                    Debug.Log(worksheet.Cells[row, col].Text);
                }
            }
        }
    }
}
```

## 注意事项

- 确保你的Unity项目支持.NET 4.x或更高版本。
- 在使用这些插件时，请遵守相应的许可协议。

## 许可证

请参考各个插件的许可证信息。

## 贡献

欢迎提交问题和拉取请求，共同完善本仓库。

## 联系方式

如有任何问题，请联系 [你的联系方式]。

---

希望本仓库能帮助你在Unity项目中更方便地操作Excel文件！

## 下载链接

[UnityExcel操作插件](https://pan.quark.cn/s/1d73866197eb)