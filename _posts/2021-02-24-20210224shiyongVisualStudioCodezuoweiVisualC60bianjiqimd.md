---
layout: post
title: "使用 Visual Studio Code 作为 Visual C 60 编辑器
date   20200602
tags Code编译器VC6VSVC98
comments true
author admin

 使用 Visual Studio Code 作为 Visual C 60 编辑器

 概述

本文档旨在指导那些希望提升老款 Visual C 60 开发体验的程序员如何配置 Visual Studio Code VS Code 以便用其现代化的功能作为 VC6 的替代编辑器考虑到 VC6 因其历史悠久而不兼容最新的操作系统并且开发环境较为简陋此方法可以让开发者享受VS Code的高级编辑功能同时利用VC6的编译能力

 步骤概览

1 准备编译器首先确保你有一个VC98编译器环境可以从旧版Visual Studio 60提取或找到兼容的编译器资源将其解压缩到一个不含中文和空格的路径如ELibraryVC98

2 安装 VS Code 插件在VS Code中安装必要的插件包括CC和Code Runner这两个插件分别提供了代码高亮和快速运行代码的能力

3 配置工作区创建一个新的工作空间来存放你的VC6项目例如DDesktopVC6C在此工作区内你需要建立一个vscode目录并添加settingsjson文件配置编译器的路径和包含头文件的目录

   json
   
     CCppdefaultincludePath ELibraryVC98INCLUDE
     coderunnerexecutorMap 
       c cd dir  ELibraryVC98VC98BAT CL fileName nologo  dirfileNameWithoutExt
       cpp cd dir  ELibraryVC98VC98BAT CL fileName nologo  dirfileNameWithoutExt"
date:   2020-06-02
tags: [Code,编译器,VC6,VS,VC98]
comments: true
author: admin
---
# 使用 Visual Studio Code 作为 Visual C++ 6.0 编辑器

## 概述

本文档旨在指导那些希望提升老款 Visual C++ 6.0 开发体验的程序员，如何配置 Visual Studio Code (VS Code) 以便用其现代化的功能作为 VC6 的替代编辑器。考虑到 VC6 因其历史悠久而不兼容最新的操作系统，并且开发环境较为简陋，此方法可以让开发者享受VS Code的高级编辑功能，同时利用VC6的编译能力。

## 步骤概览

1. **准备编译器**：首先确保你有一个VC98编译器环境，可以从旧版Visual Studio 6.0提取或找到兼容的编译器资源。将其解压缩到一个不含中文和空格的路径，如`E:/Library/VC98`。

2. **安装 VS Code 插件**：在VS Code中安装必要的插件，包括"C/C++"和"Code Runner"，这两个插件分别提供了代码高亮和快速运行代码的能力。

3. **配置工作区**：创建一个新的工作空间来存放你的VC6项目，例如`D:\Desktop\VC6_C`。在此工作区内，你需要建立一个`.vscode`目录，并添加`settings.json`文件，配置编译器的路径和包含头文件的目录。

   ```json
   {
     "C_Cpp.default.includePath": ["E:/Library/VC98/INCLUDE"],
     "code-runner.executorMap": {
       "c": "cd $dir && E:/Library/VC98/VC98/BAT CL $fileName /nologo && $dir$fileNameWithoutExt",
       "cpp": "cd $dir && E:/Library/VC98/VC98/BAT CL $fileName /nologo && $dir$fileNameWithoutExt"
     }
   }
   ```

4. **编译脚本**：为了使VS Code能够正确调用VC6的编译器，需要创建一个批处理文件，确保编译命令可以找到正确的头文件和库路径。这一步是在外部完成，确保`vc98.bat`脚本设置好`INCLUDE`和`LIB`环境变量。

5. **开始编码与运行**：保存所有设置后，在VS Code中编写或打开您的C++文件，右键点击文件并选择“Run Code”，即可利用VC6的编译器进行编译和执行。

## 注意事项

- 确保所有路径在设置中正确无误，避免空格和非英文字符。
- 编译器版本需与教程提供的相匹配，否则可能遇到兼容性问题。
- 考虑到安全性，使用老旧编译器开发时请注意代码审查和潜在的安全风险。
- 更新系统环境变量或使用批处理脚本是为了保证编译指令可以在命令行环境下正常工作。

通过上述步骤，您可以将VS Code变为一个高效的VC6代码编辑器，结合现代IDE的优点，使古老开发环境焕发新生。

## 下载链接

[使用VisualStudioCode作为VisualC6.0编辑器](https://pan.quark.cn/s/85cda321cb92)