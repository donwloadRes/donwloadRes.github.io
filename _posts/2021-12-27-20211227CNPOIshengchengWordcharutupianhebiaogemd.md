---
layout: post
title: "C NPOI生成Word插入图片和表格"
date:   2021-06-14
tags: [NPOI,文档,Word,csharp,document]
comments: true
author: admin
---
# C# NPOI生成Word插入图片和表格

## 概述

本文档旨在指导开发者如何利用C#语言结合NPOI库来生成Word文档，并在其中插入图片和表格。NPOI是一个强大的.NET库，它允许用户操作Excel、Word等Office文档格式，无需依赖Microsoft Office软件本身。本教程适合需要批量生成报告或文档的开发场景。

## 技术要求

- **C#**: 作为编程语言基础。
- **NPOI**: 需要安装NPOI库到你的项目中，支持.NET Framework和.NET Core/5及以上版本。
  
## 安装NPOI

1. 使用NuGet包管理器安装`NPOI`：
   ```
   Install-Package NPOI
   ```

2. 或者在`.csproj`文件中添加以下依赖项：
   ```xml
   <ItemGroup>
       <PackageReference Include="NPOI" Version="最新版号"/>
   </ItemGroup>
   ```

## 创建Word文档

### 步骤1: 导入必要的命名空间

```csharp
using NPOI.HWPF;
using NPOI.HWPF.usermodel;
using NPOI.Util;
```

### 步骤2: 初始化Word文档

```csharp
using (var document = new HWPFDocument())
{
    var section = document.CreateSection();
    // 文档内容操作放在此处
}
```

### 插入图片

#### 准备图片

确保图片路径正确且可访问。

#### 插入代码示例

```csharp
// 图片路径
string imagePath = @"C:\path\to\your\image.jpg";
// 加载图片
MemoryStream stream = new MemoryStream(File.ReadAllBytes(imagePath));
// 将图片转换为二进制数据，计算尺寸
PictureData pictureData = document.InsertImage(stream);
int id = pictureData.Id;
Range range = document.Range;
range.InsertAfter("这里是图片");
range.Pictures.Add(pictureData, id);
```

### 插入表格

#### 示例代码

```csharp
Table table = section.CreateTable(3, 4); // 创建3行4列的表格
// 接下来可以设置单元格的内容，如下：
for (int row = 0; row < 3; row++)
{
    for (int col = 0; col < 4; col++)
    {
        Row tRow = table.GetRow(row);
        if (tRow == null)
        {
            tRow = table.CreateRow();
        }
        Cell cell = tRow.Cells[col];
        if (cell == null)
        {
            cell = tRow.CreateCell();
        }
        cell.Text = $"单元格({row + 1},{col + 1})";
    }
}
```

## 保存文档

```csharp
document.Save("example.doc");
```

至此，您已经成功地创建了一个包含图片和表格的Word文档。通过调整上述代码，您可以根据实际需求定制文档内容。

## 结论

使用C#和NPOI生成Word文档并嵌入多媒体元素是一种高效的方式，特别是在自动化办公文档生成场景中。希望这个简短的指南能够帮助您快速上手相关开发工作。如果有更复杂的操作或者特定的需求，建议查阅NPOI的官方文档获取详细信息。

## 下载链接

[CNPOI生成Word插入图片和表格](https://pan.quark.cn/s/9ba184e035de)