---
layout: post
title: "AutoCAD二次开发实现CAD启动时自动加载DLL"
date:   2021-07-15
tags: [AutoCAD,文件,DLL,ACAD,LSP]
comments: true
author: admin
---
# AutoCAD二次开发：实现CAD启动时自动加载DLL

## 简介

在进行AutoCAD的二次开发时，通常会使用C#编写插件，并生成一个DLL文件。为了在AutoCAD启动时自动加载这个DLL文件，而不需要手动输入`NETLOAD`命令，本文将详细介绍如何实现这一功能。

## 实现方法

### 1. 创建ACAD.LSP文件

首先，创建一个名为`ACAD.LSP`的文件。这个文件是AutoCAD启动时自动加载的脚本文件。

### 2. 编写LISP代码

在`ACAD.LSP`文件中，编写以下LISP代码：

```lisp
(defun c:LoadMyPlugin ()
    (vl-load-com)
    (setq acadObj (vlax-get-acad-object))
    (setq acadDoc (vla-get-ActiveDocument acadObj))
    (setq acadApp (vlax-get-or-create-object "AutoCAD.Application"))
    (setq acadDoc (vla-get-ActiveDocument acadApp))
    (setq acadMod (vla-get-Application acadDoc))
    (vla-Load (vla-GetInterfaceObject acadMod "MyPlugin.dll"))
)

(princ "\nLoading MyPlugin.dll...")
(c:LoadMyPlugin)
(princ)
```

### 3. 放置ACAD.LSP文件

将`ACAD.LSP`文件放置在AutoCAD的启动目录中。通常，这个目录位于：

- **Windows**: `C:\Program Files\Autodesk\AutoCAD <版本>\Support`
- **Mac**: `/Applications/Autodesk/AutoCAD <版本>/Contents/Resources/Support`

### 4. 确保DLL文件路径正确

确保`MyPlugin.dll`文件的路径是正确的，并且AutoCAD能够访问到这个文件。如果DLL文件位于不同的目录，可以在LISP代码中指定完整路径。

### 5. 重启AutoCAD

重启AutoCAD，此时`MyPlugin.dll`应该会在启动时自动加载，而不需要手动输入`NETLOAD`命令。

## 注意事项

- 确保`ACAD.LSP`文件的名称和路径正确，否则AutoCAD可能无法自动加载它。
- 如果DLL文件路径发生变化，需要更新`ACAD.LSP`文件中的路径信息。
- 如果AutoCAD版本不同，启动目录可能会有所不同，请根据实际情况进行调整。

## 总结

通过创建并配置`ACAD.LSP`文件，可以实现AutoCAD启动时自动加载C#编写的DLL文件，从而简化插件的使用流程。希望本文能帮助你顺利完成AutoCAD的二次开发工作。

## 下载链接

[AutoCAD二次开发实现CAD启动时自动加载DLL](https://pan.quark.cn/s/262a8d459068)