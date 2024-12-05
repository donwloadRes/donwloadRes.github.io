---
layout: post
title: "使用C#在PDF文档上加盖印章和添加文本"
date:   2021-07-12
tags: [PDF,iTextSharp,new,印章,reader]
comments: true
author: admin
---
# 使用C#在PDF文档上加盖印章和添加文本

本教程旨在指导开发者如何运用C#语言结合iTextSharp库，在PDF文档上高效地添加印章及输入文本，以满足办公自动化和公文处理中的特定需求。iTextSharp是一个强大的开源库，专为PDF文档的操作设计，广泛应用于生成、修改PDF文件的场景。

## 简介

在处理PDF文件时，经常需要对文档进行标注或签署，比如添加公司印章确保正式性，或者直接在文档内部添加批注、说明文本。通过C#编程，利用iTextSharp，您可以轻松实现这些功能，保证流程的数字化和规范化。

## 开始之前

- **安装iTextSharp**：首先，确保您的开发环境中已经安装了iTextSharp库。可以通过NuGet包管理器在Visual Studio中搜索“iTextSharp”并安装。

- **基础知识**：建议您对C#编程有一定基础，并了解基本的PDF结构知识。

## 加盖印章

### 示例代码

以下是一个简单的示例，展示如何在PDF页面上添加图像作为印章：

```csharp
using iTextSharp.text;
using iTextSharp.text.pdf;
using System.IO;

public void AddStamp(string src, string dest)
{
    // 读取原始PDF
    PdfReader reader = new PdfReader(src);
    // 创建一个新的PDF编写器
    PdfStamper stp = new PdfStamper(reader, new FileStream(dest, FileMode.Create));
    
    // 印章图像路径（假设是PNG格式）
    Image img = Image.GetInstance("path_to_your_stamp.png");
    img.SetAbsolutePosition(400f, 300f); // 设置印章位置
    
    // 在指定页数上添加印章
    int numberOfPages = reader.NumberOfPages;
    for (int i = 1; i <= numberOfPages; i++)
    {
        PdfContentByte canvas = stp.GetOverContent(i);
        canvas.AddImage(img);
    }
    
    // 关闭写入器和阅读器
    stp.Close();
    reader.Close();
}
```

## 添加文本

### 示例代码

向PDF中添加文本的示例：

```csharp
public void AddTextToPdf(string src, string dest, string text, float x, float y)
{
    PdfReader reader = new PdfReader(src);
    PdfStamper stp = new PdfStamper(reader, new FileStream(dest, FileMode.Create));
    
    BaseFont bf = BaseFont.CreateFont(BaseFont.HELVETICA, BaseFont.CP1252, BaseFont.NOT_EMBEDDED);
    ColumnText.ShowTextAligned(stp.GetOverContent(1), Element.ALIGN_LEFT, new Phrase(text, new Font(bf, 12)), x, y, 0);
    
    stp.Close();
    reader.Close();
}
```

这段代码会在指定的位置（x, y坐标）添加文本。

## 注意事项

- 调用上述函数前，请替换`"path_to_your_stamp.png"`为实际印章图片路径。
- 文本添加和印章位置调整需根据具体PDF页面布局进行微调。
- 不要忘记在生产环境中处理异常，确保程序健壮性。

## 结论

通过以上示例，开发者可以迅速掌握使用C#和iTextSharp来增强PDF文档处理能力的基础技能，无论是用于内部审批流还是对外发送的正式文件，都能有效提升文档的专业性和处理效率。

## 下载链接

[使用C在PDF文档上加盖印章和添加文本](https://pan.quark.cn/s/ff872d5eb342)