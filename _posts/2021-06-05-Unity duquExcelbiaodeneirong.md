---
layout: post
title: "Unity 读取Excel表的内容"
date:   2023-10-10
tags: [Excel,Unity,文件,读取,导入到]
comments: true
author: admin
---
# Unity 读取Excel表的内容

## 简介

本资源文件提供了一个在Unity中读取Excel表内容的解决方案。通过使用本资源文件，开发者可以轻松地将Excel表中的数据导入到Unity项目中，以便在游戏中使用。

## 功能特点

- **支持读取Excel文件**：本资源文件支持读取常见的Excel文件格式（如.xlsx和.xls）。
- **数据导入Unity**：将Excel表中的数据导入到Unity中，并生成相应的Asset文件，方便在游戏中使用。
- **自定义数据类**：可以根据Excel表的结构，生成对应的数据类，便于管理和使用数据。

## 使用方法

1. **下载资源文件**：首先，下载本资源文件并导入到你的Unity项目中。
2. **配置Excel文件**：在项目中创建一个Excel文件，并按照需要的格式填充数据。
3. **生成数据类**：根据Excel表的结构，生成对应的数据类。
4. **读取数据**：使用提供的脚本，读取Excel文件中的数据，并将其导入到Unity中。
5. **使用数据**：在游戏中使用导入的数据，例如在商城物品、随机名称等场景中。

## 依赖库

本资源文件依赖以下库文件：
- Excel.dll
- ICSharpCode.SharpZipLib.dll
- System.Data.dll

请确保这些库文件已正确导入到你的Unity项目中。

## 示例代码

以下是一个简单的示例代码，展示如何读取Excel文件中的数据：

```csharp
using UnityEngine;
using System.Data;
using System.IO;
using Excel;

public class ExcelReader : MonoBehaviour
{
    void Start()
    {
        FileStream stream = File.Open("path_to_your_excel_file.xlsx", FileMode.Open, FileAccess.Read);
        IExcelDataReader excelReader = ExcelReaderFactory.CreateOpenXmlReader(stream);
        DataSet result = excelReader.AsDataSet();

        // 遍历数据表
        foreach (DataTable table in result.Tables)
        {
            foreach (DataRow row in table.Rows)
            {
                foreach (var cell in row.ItemArray)
                {
                    Debug.Log(cell);
                }
            }
        }
    }
}
```

## 注意事项

- 请确保Excel文件路径正确，并且在Unity中能够访问。
- 如果Excel文件中包含中文内容，请确保文件编码为UTF-8，以避免乱码问题。

## 贡献

如果你有任何改进建议或发现了bug，欢迎提交issue或pull request。

## 许可证

本资源文件遵循CC 4.0 BY-SA版权协议，转载请附上原文出处声明。

## 下载链接

[Unity读取Excel表的内容分享](https://pan.quark.cn/s/38d0add8427a)