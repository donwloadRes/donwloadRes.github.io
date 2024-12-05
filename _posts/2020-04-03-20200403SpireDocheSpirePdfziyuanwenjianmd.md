---
layout: post
title: "Spire.Doc 和 Spire.Pdf 资源文件"
date:   2022-06-28
tags: [Spire,Doc,文件,Pdf,dll]
comments: true
author: admin
---
# Spire.Doc 和 Spire.Pdf 资源文件

## 简介
本仓库提供了一个包含四个DLL文件的资源文件，这些文件是用于处理Word和PDF文档的Spire.Doc和Spire.Pdf库。具体文件及其版本如下：
- Spire.Common.dll（版本1.2.792.14040）
- Spire.Liscense.dll（版本1.3.6.40）
- Spire.Doc.dll（版本6.8.16.4040）
- Spire.Pdf.dll（版本4.8.15.2040）

## 使用方法
在使用这些DLL文件时，请确保将所有四个文件都引用到您的项目中。以下是一个简单的示例代码，展示了如何在Visual Studio 2015和.NET Framework 4.6.2环境下使用Spire.Doc打开一个Word文档并保存到指定路径：

```csharp
if (openFileDialog.ShowDialog() == true)
{
    ShowOperInfo("正在打开文档……");
    Spire.Doc.Document document = new Spire.Doc.Document(openFileDialog.FileName);
    document.SaveToFile(@"C:\Users\Administrator\Desktop\aa.docx");
}
```

## 注意事项
- 请确保在项目中引用所有四个DLL文件。
- 本资源文件已经过测试，确保在Visual Studio 2015和.NET Framework 4.6.2环境下完全可用。

## 贡献
欢迎大家贡献代码和提出问题，共同完善本仓库。如果您有任何建议或问题，请在GitHub上提交Issue或Pull Request。

## 许可证
本仓库的资源文件遵循相应的开源许可证。具体许可证信息请参考每个文件的许可证声明。

---

希望本仓库的资源文件能对您的工作或学习有所帮助！如果有任何问题，请随时联系我们。

## 下载链接

[Spire.Doc和Spire.Pdf资源文件](https://pan.quark.cn/s/dad620c2507d)