---
layout: post
title: "Word 目录字体设置技巧章节标题与页码字体不同
date   20210819
tags 字体目录页码Word章节
comments true
author admin

 Word 目录字体设置技巧章节标题与页码字体不同

 资源描述

在撰写论文或其他文档时目录的格式要求往往比较严格例如有些论文要求目录中的章节标题中的数字使用 Arial 字体而页码则需要使用 Times New Roman 字体Word 默认情况下目录中的字体是统一的无法直接设置不同部分使用不同的字体本资源文件将详细介绍如何在 Word 中实现这一需求让目录中的章节标题与页码使用不同的字体

 解决方案

 1 手动调整目录字体

虽然 Word 无法直接设置目录中不同部分的字体但可以通过手动调整来实现这一效果具体步骤如下

1 生成目录首先按照常规方法生成目录
2 选择目录中的数字在生成的目录中选择章节标题中的数字部分
3 更改字体将选中的数字字体更改为 Arial
4 选择页码接下来选择目录中的页码部分
5 更改字体将页码的字体更改为 Times New Roman

 2 使用 VBA 宏自动化

如果你需要频繁地进行这种操作手动调整可能会比较繁琐此时可以使用 VBA 宏来自动化这一过程以下是一个简单的 VBA 代码示例

vba
Sub ChangeTOCFont
    Dim toc As TableOfContents
    Dim rng As Range
    Dim i As Integer
    
     选择目录
    Set toc  ActiveDocumentTablesOfContents1
    Set rng  tocRange
    
     遍历目录中的每一项
    For i  1 To rngParagraphsCount
         选择章节标题中的数字
        With rngParagraphsiRange
            FindExecute FindTextd ForwardTrue WrapwdFindStop
            If FindFound Then
                FontName  Arial
            End If
        End With
        
         选择页码
        With rngParagraphsiRange
            FindExecute FindTextd ForwardTrue WrapwdFindStop
            If FindFound Then
                FontName  Times New Roman"
date:   2021-08-19
tags: [字体,目录,页码,Word,章节]
comments: true
author: admin
---
# Word 目录字体设置技巧：章节标题与页码字体不同

## 资源描述

在撰写论文或其他文档时，目录的格式要求往往比较严格。例如，有些论文要求目录中的章节标题中的数字使用 Arial 字体，而页码则需要使用 Times New Roman 字体。Word 默认情况下，目录中的字体是统一的，无法直接设置不同部分使用不同的字体。本资源文件将详细介绍如何在 Word 中实现这一需求，让目录中的章节标题与页码使用不同的字体。

## 解决方案

### 1. 手动调整目录字体

虽然 Word 无法直接设置目录中不同部分的字体，但可以通过手动调整来实现这一效果。具体步骤如下：

1. **生成目录**：首先，按照常规方法生成目录。
2. **选择目录中的数字**：在生成的目录中，选择章节标题中的数字部分。
3. **更改字体**：将选中的数字字体更改为 Arial。
4. **选择页码**：接下来，选择目录中的页码部分。
5. **更改字体**：将页码的字体更改为 Times New Roman。

### 2. 使用 VBA 宏自动化

如果你需要频繁地进行这种操作，手动调整可能会比较繁琐。此时，可以使用 VBA 宏来自动化这一过程。以下是一个简单的 VBA 代码示例：

```vba
Sub ChangeTOCFont()
    Dim toc As TableOfContents
    Dim rng As Range
    Dim i As Integer
    
    ' 选择目录
    Set toc = ActiveDocument.TablesOfContents(1)
    Set rng = toc.Range
    
    ' 遍历目录中的每一项
    For i = 1 To rng.Paragraphs.Count
        ' 选择章节标题中的数字
        With rng.Paragraphs(i).Range
            .Find.Execute FindText:="\d+", Forward:=True, Wrap:=wdFindStop
            If .Find.Found Then
                .Font.Name = "Arial"
            End If
        End With
        
        ' 选择页码
        With rng.Paragraphs(i).Range
            .Find.Execute FindText:="\d+", Forward:=True, Wrap:=wdFindStop
            If .Find.Found Then
                .Font.Name = "Times New Roman"
            End If
        End With
    Next i
End Sub
```

### 3. 使用样式设置

另一种方法是使用 Word 的样式功能。你可以为目录中的不同部分创建自定义样式，并在生成目录时应用这些样式。具体步骤如下：

1. **创建自定义样式**：在 Word 中，创建两个新的样式，一个用于章节标题中的数字（Arial 字体），另一个用于页码（Times New Roman 字体）。
2. **应用样式**：在生成目录后，手动将这些样式应用到相应的部分。

## 总结

通过上述方法，你可以轻松地在 Word 中实现目录中章节标题与页码使用不同字体的需求。无论是手动调整、使用 VBA 宏，还是通过样式设置，都能有效地解决这一问题。希望本资源文件对你有所帮助！

## 下载链接

[Word目录字体设置技巧章节标题与页码字体不同分享](https://pan.quark.cn/s/752eee1deed9)