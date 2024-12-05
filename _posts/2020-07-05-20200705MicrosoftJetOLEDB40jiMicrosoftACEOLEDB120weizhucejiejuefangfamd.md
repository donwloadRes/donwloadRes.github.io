---
layout: post
title: "MicrosoftJetOLEDB40 及 MicrosoftACEOLEDB120 未注册解决方法
date   20210620
tags MicrosoftFilesdll未注册Jet
comments true
author admin

 MicrosoftJetOLEDB40 及 MicrosoftACEOLEDB120 未注册解决方法

 资源文件描述

在使用C开发过程中有时会遇到以下错误提示

 未在本地计算机上注册MicrosoftJetOLEDB40提供程序
 未在本地计算机上注册MicrosoftACEOLEDB120提供程序

这些错误通常是由于系统中缺少相应的OLE DB提供程序导致的本资源文件提供了解决这些问题的详细步骤和所需文件

 解决方法

 1 安装 Microsoft Access Database Engine

首先确保你的系统中安装了Microsoft Access Database Engine你可以从微软官方网站下载并安装适合你系统的版本

 2 注册 OLE DB 提供程序

如果你已经安装了Microsoft Access Database Engine但仍然遇到未注册的错误可以尝试手动注册这些提供程序

 注册 MicrosoftJetOLEDB40

1 打开命令提示符以管理员身份运行
2 输入以下命令并按回车键
   
   regsvr32 CProgram FilesCommon FilesSystemadomsjrodll
   regsvr32 CProgram FilesCommon FilesSystemadomsado15dll
   

 注册 MicrosoftACEOLEDB120

1 打开命令提示符以管理员身份运行
2 输入以下命令并按回车键
   
   regsvr32 CProgram FilesCommon FilesSystemadomsjrodll
   regsvr32 CProgram FilesCommon FilesSystemadomsado15dll"
date:   2021-06-20
tags: [Microsoft,Files,dll,未注册,Jet]
comments: true
author: admin
---
# Microsoft.Jet.OLEDB.4.0 及 Microsoft.ACE.OLEDB.12.0 未注册解决方法

## 资源文件描述

在使用C#开发过程中，有时会遇到以下错误提示：

- 未在本地计算机上注册“Microsoft.Jet.OLEDB.4.0”提供程序
- 未在本地计算机上注册“Microsoft.ACE.OLEDB.12.0”提供程序

这些错误通常是由于系统中缺少相应的OLE DB提供程序导致的。本资源文件提供了解决这些问题的详细步骤和所需文件。

## 解决方法

### 1. 安装 Microsoft Access Database Engine

首先，确保你的系统中安装了Microsoft Access Database Engine。你可以从微软官方网站下载并安装适合你系统的版本。

### 2. 注册 OLE DB 提供程序

如果你已经安装了Microsoft Access Database Engine，但仍然遇到未注册的错误，可以尝试手动注册这些提供程序。

#### 注册 Microsoft.Jet.OLEDB.4.0

1. 打开命令提示符（以管理员身份运行）。
2. 输入以下命令并按回车键：
   ```
   regsvr32 "C:\Program Files\Common Files\System\ado\msjro.dll"
   regsvr32 "C:\Program Files\Common Files\System\ado\msado15.dll"
   ```

#### 注册 Microsoft.ACE.OLEDB.12.0

1. 打开命令提示符（以管理员身份运行）。
2. 输入以下命令并按回车键：
   ```
   regsvr32 "C:\Program Files\Common Files\System\ado\msjro.dll"
   regsvr32 "C:\Program Files\Common Files\System\ado\msado15.dll"
   ```

### 3. 检查注册表

如果上述步骤未能解决问题，可以检查注册表中是否存在相应的注册项。

1. 打开注册表编辑器（运行 `regedit`）。
2. 导航到以下路径：
   ```
   HKEY_CLASSES_ROOT\CLSID\{731F47C6-387A-43ED-97F0-3E653F984F1E}
   HKEY_CLASSES_ROOT\CLSID\{731F47C6-387A-43ED-97F0-3E653F984F1E}\InprocServer32
   ```
3. 确保 `InprocServer32` 键值指向正确的DLL文件路径。

## 资源文件内容

本资源文件包含以下内容：

- `msjro.dll`
- `msado15.dll`
- 注册命令的文本文件

请根据需要下载并使用这些文件。

## 注意事项

- 在执行注册命令时，请确保以管理员身份运行命令提示符。
- 如果系统中已经存在这些DLL文件，请不要重复注册，以免造成冲突。

通过以上步骤，你应该能够解决C#中未注册Microsoft.Jet.OLEDB.4.0 及 Microsoft.ACE.OLEDB.12.0的问题。

## 下载链接

[Microsoft.Jet.OLEDB.4.0及Microsoft.ACE.OLEDB.12.0未注册解决方法](https://pan.quark.cn/s/dd148de27094)